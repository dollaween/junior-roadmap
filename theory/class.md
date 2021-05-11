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

---

Для задания индивидуальных значений свойств для каждого объекта, используется конструктор:

```js
class Person {
  kind = 'human'

  constructor(name, age) {
    this.name = name
    this.age = age
  }
}

const person1 = new Person('John', 33)
const person2 = new Person('Brad', 25)

console.log(person1)  // { kind: 'human', name: 'John', age: 33 }
console.log(person2)  // { kind: 'human', name: 'Brad', age: 25 }
```












