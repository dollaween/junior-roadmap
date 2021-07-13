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

# `rerender`

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

`rerender` — перерисовывает тот же самый компонент.

Полезно, чтобы проверить компонент на корректное изменение передаваемых параметров.

```js
import { render } from '@testing-library/react'

const { rerender } = render(<Example number={1} />)

// Перерендеривает тот же самый компонент, но с другими параметрами
rerender(<Example number={2} />)
```

---

- [React Testing Library — API](https://testing-library.com/docs/react-testing-library/api)
