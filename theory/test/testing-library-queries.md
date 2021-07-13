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

---

<div align="center">

### Типы запросов

</div>

---

Запросы делятся на следующие типы:
- Один элемент:
  - `getBy...` — возвращает найденный элемент. Если элемент не найден или найдено больше одного элемента — выкидывает ошибку.
  - `queryBy...` — возвращает найденный элемент. Если элемент не найден — возвращает `null`. Если найдено больше одного элемента — выкидывает ошибку.
  - `findBy...` — возвращает промис. Если в результате будет найден один элемент — сработает `resolve`. Если элемент не будет найден или будет найдено больше одного элемента — сработает `reject`.

- Множество элементов:
  - `getAllBy...` — возвращает массив найденных элементов. Если не найдено ни одного элемента — выкидывает ошибку.
  - `queryAllBy...` — возвращает массив найденных элементов. Если не найдено ни одного элемента — возвращает `null`.
  - `findAllBy...` — возвращает промис. Если в результате будут найдены элементы — сработает `resolve`. Если элементов не найдено — сработает `reject`.

Итого:
- `getBy...`, `getAllBy...` — используются в большинстве ситуаций, стоит отдавать предпочтение этим методам.
- `queryBy...`, `queryAllBy...` — используются, если необходимо проверить на отстуствие элементов.
- `findBy...`, `findAllBy...` — используются, чтобы найти элементы, который недоступны сразу.

---

<div align="center">

### Приоритет запросов

</div>

---

Запросы, в порядке приоритета использования:

`getByRole` — находит элемент по атрибуту `role` ([список ролей](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles))
```js
const { getByRole } = render(<input id="login" />);

const input = await getByRole('textbox');
```


`getByLabelText` — находит элемент на который указывает `<label>`

```js
const { getByLabelText } = render(
  <div>
    <label htmlFor="login">Enter login</label>
    <input id="login" />
  </div>
);

const input = await getByLabelText(/enter login/i);
```


---

- [Testing Library — About Queries](https://testing-library.com/docs/queries/about)
- [WAI-ARIA Roles](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles)
