<div align="center">

# Testing Library — советы

[Главная](https://github.com/dollaween/junior-roadmap/)
|
[Карта](/roadmap/README.md)
|
[Теория](/theory/README.md)
|
[Тесты](/tests/README.md)
|
[Задачи](/tasks/README.md)

</div>

---

<div align="center">

### Используйте `screen`

</div>

---

```js
// ❌
import { render } from '@testing-library/react'

const { getByRole } = render(<Example />)
const errorMessageNode = getByRole('alert')

// ✅
import { render, screen } from '@testing-library/react'

render(<Example />)
const errorMessageNode = screen.getByRole('alert')
```

Преимущество `screen` в том, что больше не нужно держать зависимости в деструктуризации, добавляя/удаляя их каждый раз при надобности.

---

<div align="center">

### Используйте семантические утверждения в `expect`

</div>

---

```js
const button = screen.getByRole('button', { name: /disabled button/i })

// ❌
expect(button.disabled).toBe(true)
// error message:
//  expect(received).toBe(expected) // Object.is equality
//
//  Expected: true
//  Received: false

// ✅
expect(button).toBeDisabled()
// error message:
//   Received element is not disabled:
//     <button />
```

В семантических утверждениях типа `toBeDisabled()` и подобных — сообщения об ошибках прописаны лучше и понятнее.

---

<div align="center">

### Используйте `userEvent` вместо `fireEvent` где это возможно

</div>

---

```js
// ❌
fireEvent.change(input, { target: { value: 'hello world' } })

// ✅
userEvent.type(input, 'hello world')
```

Библиотека `userEvent` написана поверх `fireEvent`, но предоставляет некоторые методы, которые более близки к тому, как с компонентом работал бы пользователь.

Например:  
`fireEvent.change` — вызывает только одно событие у `input`.  
`userEvent.type` — вызывает события `keyDown`, `keyPress` и `keyUp` для каждого написанного символа, что больше соответствует реальному поведению пользователя.

---

<div align="center">

### Используйте `query*` только для проверки на отсутствие элемента

</div>

---

```js
// ❌
expect(screen.queryByRole('alert')).toBeInTheDocument()

// ✅
expect(screen.getByRole('alert')).toBeInTheDocument()
expect(screen.queryByRole('alert')).not.toBeInTheDocument()
```

`get*` — выбрасывает ошибку, если элемент не найден.  
`query*` — возвращает `null`, если элемент не найден.

---

<div align="center">

### Используйте `find*` для того чтобы найти элемент, который недоступен прямо сейчас

</div>

---

```js
// ❌
const submitButton = await waitFor(() =>
  screen.getByRole('button', { name: /submit/i }),
)

// ✅
const submitButton = await screen.findByRole('button', {name: /submit/i})
```

Эти два примера эквиваленты, но второй проще и сообщение об ошибке будет более конструктивное.

> `find*` использует под капотом `waitFor`.

---

<div align="center">

### Всегда заполняйте колбэк в `waitFor`

</div>

---

```js
// ❌
await waitFor(() => {})
expect(window.fetch).toHaveBeenCalledWith('foo')
expect(window.fetch).toHaveBeenCalledTimes(1)

// ✅
await waitFor(() => expect(window.fetch).toHaveBeenCalledWith('foo'))
expect(window.fetch).toHaveBeenCalledTimes(1)
```

Пустой колбэк в `waitFor` означает — "подожди один тик". Такой тест является хрупким, потому что при изменении асинхронной логики в компоненте тест может быть сломан.

---

<div align="center">

### Не обрабатывайте логику с побочными эффектами в `waitFor`

</div>

---

```js
// ❌
await waitFor(() => {
  fireEvent.keyDown(input, { key: 'ArrowDown' })
  expect(screen.getAllByRole('listitem')).toHaveLength(3)
})

// ✅
fireEvent.keyDown(input, { key: 'ArrowDown' })
await waitFor(() => {
  expect(screen.getAllByRole('listitem')).toHaveLength(3)
})
```

`waitFor` предназначен для тестов, у которых есть некоторый промежуток времени между действием и утверждением. Колбэк `waitFor` может вызываться (или проверяться на наличие ошибок) множество раз (он вызывается как по определенному интервалу, так и при наличии изменений в DOM). Это означает, что логика с побочными эффектами может быть вызвана множество раз.

Это так же означает, что снэпшоты делать в `waitFor` нельзя.

---

<div align="center">

### Не используйте `cleanup`

</div>

---

```js
// ❌
import { render, screen, cleanup } from '@testing-library/react'
afterEach(cleanup)

// ✅
import {render, screen} from '@testing-library/react'
```

`cleanup` автоматически встроен в современные фреймворки, поддерживающие функцию `afterEach` (Jest, Jasmine, Mocha).

---

<div align="center">

### Не используйте запросы непосредственно на контейнере

</div>

---

```js
// ❌
const { container } = render(<Example />)
const button = container.querySelector('.btn-primary')
expect(button).toHaveTextContent(/click me/i)

// ✅
render(<Example />)
screen.getByRole('button', { name: /click me/i })
```

Тесты, с запросами на контейнере, сложнее читать и они будут чаще ломаться.

---

<div align="center">

### Отдавайте преимущество поискам `*ByRole`

</div>

---

```js
// Предположим, структура нашего DOM такая:
// <button><span>Hello</span> <span>World</span></button>

screen.getByText(/hello world/i)
// ❌ такой вызов упадет со следующей ошибкой:
// Unable to find an element with the text: /hello world/i. This could be
// because the text is broken up by multiple elements. In this case, you can
// provide a function for your text matcher to make your matcher more flexible.

screen.getByRole('button', { name: /hello world/i })
// ✅ такой вызов найдет элемент!
```

Скринридеры различают элементы по их свойству `role`. Использование правильных `role`-элементов в коде — уже хорошая практика.

К тому же, `*ByRole` найдет элемент, если его содержимое разделено на части (как в примере выше).

> Список доступных ролей: [WAI-ARIA Roles](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles)

---

<div align="center">

### Используйте поиск по тексту

</div>

---

```js
// ❌
screen.getByTestId('submit-button')

// ✅
screen.getByRole('button', { name: /submit/i })
```

Наибольшая проблема с поиском по тексту — это изменение текста в компоненте, от чего тест сломается. Но:
1. Тест легко и быстро восстановить.
2. Изменение текста с `Username` на `Email` — это весомое изменение. И поломка теста — это даже хорошо, потому что мы будем в курсе о таких изменениях.

---

<div align="center">

### Избегайте ненужной абстракции

</div>

---

Зачастую можно встретить подобный код:

```js
describe('Login', () => {
  let user,
    utils,
    handleSubmit,
    clickSubmit

  beforeEach(() => {
    handleSubmit = jest.fn()
    utils = render(<Login onSubmit={handleSubmit}>)
    user = { username: 'John', password: '12345' }
    clickSubmit = () => userEvents.click(utils.getByText(/submit/i))
  })

  describe('when the submit button is clicked', () => {
    beforeEach(() => {
      clickSubmit()
    })

    it('should call onSubmit with the username and password', () => {
      expect(handleSubmit).toHaveBeenCalledTimes(1)
      expect(handleSubmit).toHaveBeenCalledWith(user)
    })
  })

  // ...
})
```

У такого кода сразу несколько проблем:
1. Появляется излишняя абстрактность, усложняющая чтение кода.
2. На строке `expect` не понятно откуда взялись `handleSubmit` и `user`. Чтобы узнать о них — нужно перейти к их объявлениям. А после еще необходимо проверить, не были ли эти переменные изменены во вложенных `beforeEach`.

Решение — использовать инлайновые тесты:

```js
test('calls onSubmit with the username and password when submit is clicked', () => {
  const handleSubmit = jest.fn()
  render(<Login onSubmit={handleSubmit} />)
  const user = { username: 'John', password: '12345 }
  
  userEvent.type(screen.getByLabelText(/username/i), user.username)
  userEvent.type(screen.getByLabelText(/password/i), user.password)
  userEvent.click(screen.getByText(/submit/i))

  expect(handleSubmit).toHaveBeenCalledTimes(1)
  expect(handleSubmit).toHaveBeenCalledWith(user)
})
```

Так код становится понятнее, все сразу на виду. Появление некоторой дублируемости кода — не большая цена за простоту чтения тестов. Но если все же хочется избежать излишнего дублирования кода, то можно использовать самые обычные Javascript-функции.

```js
function setup() {
  const handleSubmit = jest.fn()
  const utils = render(<Login onSubmit={handleSubmit}>)
  const user = { username: 'John', password: '12345' }
  const clickSubmit = () => userEvents.click(utils.getByText(/submit/i))
  return { ...utils, user, handleSubmit, clickSubmit }
}

test('calls onSubmit with the username and password when submit is clicked', () => {
  // вот таким образом мы явно понимаем откуда берутся handleSubmit и user
  const { handleSubmit, user } = setup()
  // ...
})
```

Подробнее про проблему здесь: [Avoid Nesting when you're Testing](https://kentcdodds.com/blog/avoid-nesting-when-youre-testing)

---

<div align="center">

###  Не оборачивайте `render` и `fireEvent` в `act`

</div>

---

```js
// ❌
act(() => {
  render(<Example />)
})
const input = screen.getByRole('textbox', {name: /choose a fruit/i})
act(() => {
  fireEvent.keyDown(input, {key: 'ArrowDown'})
})

// ✅
render(<Example />)
const input = screen.getByRole('textbox', {name: /choose a fruit/i})
fireEvent.keyDown(input, {key: 'ArrowDown'})
```

`render` и `fireEvent` внутри уже обернуты в `act`.

Исправить ошибку `not wrapped in ac(...)` можно по следующей инструкции:  
[https://kentcdodds.com/blog/fix-the-not-wrapped-in-act-warning](https://kentcdodds.com/blog/fix-the-not-wrapped-in-act-warning)

---

<div align="center">

###  Используйте конкретные значения или константы в качестве ожидаемого значения

</div>

---

В качестве ожидаемого значения (в часть где пишут `.toBe()` и т.п.) нужно устанавливать конкретное значение или константу, чтобы избежать побочных эффектов.

Пример побочного эффекта:
```js
// Устанавливает страну у person2 такую же, как и у person1
function changeCountry(person1, person2) {
  person1.country = person2.country  // ❌ здесь допущена ошибка! должно было быть person2.country = person1.country
}

it('should move person2 to person1', function () {
  const person1 = { country: 'Spain' }
  const person2 = { country: 'Italy' }

  changeCountry(person1, person2)

  expect(person2.country).toBe(person1.country)
})
```

Мы допустили ошибку, но тест все равно пройден. Сейчас тест не проверяет, что именно в `person2` мы устанавливаем новое значение. Это надо исправить.

Правильное решение:
```js
// Устанавливает страну у person2 такую же, как и у person1
function changeCountry(person1, person2) {
  person1.country = person2.country  // ❌ все еще присутствует ошибка!
}

it('should move person2 to person1', function () {
  const PERSON1_COUNTRY = 'Spain'

  const person1 = { country: PERSON1_COUNTRY }
  const person2 = { country: 'Italy' }

  changeCountry(person1, person2)

  expect(person2.country).toBe(PERSON1_COUNTRY)
})
```

Теперь наш тест упадет и действительно отобразит ошибку.


---

Источники:
- [Common mistakes with React Testing Library](https://kentcdodds.com/blog/common-mistakes-with-react-testing-library)
- [Avoid Nesting when you're Testing](https://kentcdodds.com/blog/avoid-nesting-when-youre-testing)
- [Fix the "not wrapped in act(...)" warning](https://kentcdodds.com/blog/fix-the-not-wrapped-in-act-warning)
