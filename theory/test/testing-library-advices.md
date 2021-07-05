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
`userEvent.type` — вызывает события `keyDown`, `keyPress` и `keyUp` для каждого написанного символа.

---

Источники:
- [Common mistakes with React Testing Library](https://kentcdodds.com/blog/common-mistakes-with-react-testing-library)
