<div align="center">

# Классы

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

**Класс** — это шаблон для создания объектов.

---

Объявление класса:
```js
class Person {
  constructor() {}
}
```

В теле класса мы можем записывать свойства и методы:
```js
class Person {
  name = 'John'
  age = 33

  constructor() {}

  greet() {
    return `${this.name} ${this.age}`
  }
}
```

Метод `constructor()` — обязателен для любой функции (а класс — это просто "специальная" функция). Если его пропустить — Javascript автоматически добавит пустой метод `constructor()`.

---

Создание объекта по шаблону класса:
```js
class Person {
  name = 'John'
  age = 33

  constructor() {}

  greet() {
    return `${this.name} ${this.age}`
  }
}

const person = new Person

console.log(person)
/*
  {
    age: 33,
    name: 'John',
    __proto__: {
      constructor: Person,
      greet: greet()
    }
  }
*/
```
