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

### Используйте `screen`

---

```js
// ❌
const {getByRole} = render(<Example />)
const errorMessageNode = getByRole('alert')
// ✅
render(<Example />)
const errorMessageNode = screen.getByRole('alert')
```
