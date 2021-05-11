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

Создание объекта по шаблону класса (созданные объекты называются **экземплярами класса**):

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

---

<div align="center">

### Статические свойства и методы

</div>

---

Свойства и методы класса с ключевым словом `static` — становятся статическими. Статические свойства недоступны в экземплярах класса, но могут быть использованы при работе с самим классом.

```js
class Person {
  static displayName = 'Пользователь'

  constructor(name) {
    this.name = name
  }
  
  static getClassInfo() {
    console.log('Имя класса: ' + this.displayName)
  }
}

const person = new Person('John')

console.log(person.displayName)     // undefined
console.log(person.getClassInfo)    // undefined
console.log(Person.displayName)     // 'Пользователь'
console.log(Person.getClassInfo())  // 'Имя класса: Пользователь'
```

Статические свойства и методы в основном используются для:
1. Хранения служебных свойств и методов
2. Кэширования (например, чтобы только класс хранил свойство `displayName`, не задействуя это свойство во всех экземплярах класса).

---

<div align="center">

### Приватные свойства и методы

</div>

---

Свойство, перед которым находится символ `#` — становится приватным. Приватные свойства можно использовать только внутри класса (и его экземпляров). За пределами класса приватные свойства будут недоступны.

```js
class Person {
  #name
  age

  constructor(name, age) {
    this.#name = name
    this.age = age
  }
  
  getInfo() {
    console.log(`${this.#name} — ${this.age} года`)
  }
}

const person = new Person('John', 33)

// Выводя объект person мы видим внутри поля age и #name
console.log(person)
// { age: 33, #name: 'John' }

// Но к приватному свойству #name вне класса у нас доступа нет, в отличии от age
console.log(person.name)  // undefined
console.log(person.age)   // 33

// Внутри методов класса мы можем пользоваться приватными свойствами
console.log(person.getInfo())  // 'John — 33 года'
```




