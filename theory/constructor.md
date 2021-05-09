<div align="center">

# Конструкторы и оператор `new`

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

Конструктор — это функция, с помощью которой мы можем создавать несколько экземпляров объектов.

Есть два соглашения:
1. Функции-конструкторы должны быть названы с большой буквы
2. Функция-конструктор должна быть вызвана через оператор `new`

```js
function User(name) {
  this.name = name
}
const user = new User('Gimli')
```

Когда мы вызываем функцию через оператор `new`, происходит следующее:
1. Создается новый пустой объект и присваивается в this
2. Выполняется код функции
3. После завершения работы функции, возвращается значение this

Итого, наша функция `User()` будет иметь такой код внутри себя:
```js
function User(name) {
  // this = {} (неявно)
  this.name = name
  // return this (неявно)
}
const user = new User('Gimli')

console.log(user)  // { name: 'Gimli' }
```

---

<div align="center">

### Пример использования

</div>

---

С помощью функции-конструктора, мы можем создавать множество объектов. Например:
```js
function User(login, password) {
  this.login = login
  this.password = password
}

const user1 = new User('Frodo', '123')
const user2 = new User('Gandalf', 'Sauron')
const user3 = new User('Aragorn', '777')

console.log(user1)  // { login: 'Frodo', password: '123' }
console.log(user2)  // { login: 'Gandalf', password: 'Sauron' }
console.log(user3)  // { login: 'Aragorn', password: '777' }
```

---
