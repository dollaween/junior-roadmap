<div align="center">

# Jest — `expect`

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

`expect` — это набор правил, которые проверяют, что значения соответствуют определенным условиям.

Пример:
```js
expect(1 + 1).toBe(2)               // true
expect('Hello').toHaveLength(5)     // true
expect({ a: 1 }).toEqual({ a: 1 })  // true (для проверки объектов нужно использовать toEqual, вместо toBe)
```

Для проверки, что результат не равен какому-либо значению, необходимо использовать `.not.`:
```js
expect(1 + 1).not.toBe(11)              // true
expect('Hello').not.toHaveLength(10)    // true
expect({ a: 1 }).not.toEqual({ b: 1 })  // true
```

Список доступных правил проверок:
- [Jest](https://jestjs.io/ru/docs/expect)
- [JestDOM](https://github.com/testing-library/jest-dom)


