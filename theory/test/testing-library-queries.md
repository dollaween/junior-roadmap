<div align="center">

# Testing Library — Запросы

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

Запросы — это набор методов, с помощью которых мы находим элементы на странице.

```js
const { getByText } = render(
  <div>
    <h1>Hello World</h1>
    <p>Description</p>
  </div>
);

const h1 = getByText('Hello World')
// Теперь в константе h1 содержится элемент h1
```

Запросы деляться на несколько типов:
- Запросы, возвращающие первый найденный элемент:
  - `getBy...` —
  - `queryBy...` —
  - `findBy...` —
- Запросы, возвращающие все найденные элементы:
  - `getAllBy...` —
  - `queryAllBy...` —
  - `findAllBy...` —


---

- [Testing Library — About Queries](https://testing-library.com/docs/queries/about)
