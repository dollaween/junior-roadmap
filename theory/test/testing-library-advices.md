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
const {getByRole} = render(<Example />)
const errorMessageNode = getByRole('alert')

// ✅
import {render, screen} from '@testing-library/react'

render(<Example />)
const errorMessageNode = screen.getByRole('alert')
```

Преимущество `screen` в том, что больше не нужно держать зависимости в деструктуризации, добавляя/удаляя их каждый раз при надобности.

---

Источники:
- [Common mistakes with React Testing Library](https://kentcdodds.com/blog/common-mistakes-with-react-testing-library)
