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

### Отдавайте преимущество поиску по тексту

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

Источники:
- [Common mistakes with React Testing Library](https://kentcdodds.com/blog/common-mistakes-with-react-testing-library)
