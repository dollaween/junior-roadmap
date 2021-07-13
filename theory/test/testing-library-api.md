<div align="center">

# Testing Library — API

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

### `render`

</div>

---

Метод `render` — рендерит компонент, оборачивает его в `div` и помещает в `document.body`.

```js
import { render } from '@testing-library/react'

render(<Example />)
```

`render` возвращает объект, содержащий:
- `container` — `div`, в который будет обернут ваш компонент.
- `baseElement` — по-умолчанию, это ссылка на `document.body`.
- `debug` — выводит в консоль содержимое `baseElement`.
- `rerender` — перерисовывает текущий компонент еще раз.
- `unmount` — размонтирует текущий компонент.
- `...queries` — `getByRole`, `getByTestId` и другие (подробнее в главе про "Запросы").
- `asFragment`


---

<div align="center">

### `rerender`

</div>

---

Метод `rerender` — перерисовывает тот же самый компонент.

Полезно, чтобы проверить компонент на корректное изменение передаваемых параметров.

```js
import { render } from '@testing-library/react'

const { rerender } = render(<Example number={1} />)

// Перерендеривает тот же самый компонент, но с другими параметрами
rerender(<Example number={2} />)
```


---

<div align="center">

### `debug`

</div>

---

Метод `debug` — выводит в консоль содержимое `baseElement`.

Этот метод — обертка над `console.log(prettyDOM(baseElement))`.

```js
import React from 'react'
import { render } from '@testing-library/react'

const { debug } = render(<h1>Hello World</h1>)
debug()
// <body>
//   <div>
//     <h1>
//       Hello World
//     </h1>
//   </div>
// </body>
```

---

<div align="center">

### `unmount`

</div>

---

Метод `unmount` — размонтирует текущий компонент.

Этот метод полезен для проверки, что все обработчики событий будут очищены после удаления компонента.

```js
const { container, unmount } = render(<Example />)
unmount()
```



---

- [React Testing Library — API](https://testing-library.com/docs/react-testing-library/api)
