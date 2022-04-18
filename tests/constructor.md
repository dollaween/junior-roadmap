<div align="center">

# Конструктор

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

##### 1. Какой будет вывод при запуске скрипта в браузере?

```javascript
function Person() {
  console.log(this)
}

new Person()
```

1. Вывода в консоль не произойдет
2. `{}`
3. `{ functionName: 'Person' }`
4. `Window`

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 2**

  Конструктор — это функция, с помощью которой мы можем создавать несколько экземпляров объектов. Функция-конструктор должна быть вызвана с помощью оператора `new`.

  Когда мы вызываем функцию через оператор `new`, происходит следующее:
  1. Создается новый пустой объект и присваивается в `this`
  2. Выполняется код функции
  3. После завершения работы функции, возвращается значение `this`
 
  Буквально произошло следующее:
  ```js
  function Person() {
    // this = {} (неявно)
    console.log(this)  // {}
    // return this (неявно)
  }

  new Person()
  ```

</p>
</details>

---

##### 2. Какой будет вывод при запуске скрипта в браузере?

```javascript
function Person(name, age) {
  this.name = name
  this.age = age
}

const result = new Person('John', 23)
console.log(result)
```

1. `{ name: 'John', age: 23 }`
2. `Window`
3. `undefined`
4. `{}`

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 1**

  Буквально произошло следующее:
  ```js
  function Person(name, age) {
    // this = {} (неявно)
    this.name = name   // this = { name: 'John' }
    this.age = age     // this = { name: 'John', age: 23 }
    // return this (неявно)
  }

  const result = new Person('John', 23)
  console.log(result)  // { name: 'John', age: 23 }
  ```

</p>
</details>

---

##### 3. Какой будет вывод при запуске скрипта в браузере?

```javascript
function Book(title, year) {
  this.title = title
  this.year = year
  
  return {}
}

const result = new Book('Clean Code', 2008)
console.log(result)
```

1. `{}`
2. `{ title: 'Clean Code', year: 2008 }`
3. `undefined`
4. `SyntaxError`

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 1**
  
  Если в функции-конструкторе через `return` мы возвращаем объект — в итоге будет возвращен этот объект, а не `this`.

</p>
</details>

---

##### 4. Какой будет вывод при запуске скрипта в браузере?

```javascript
function Summary(name, birthday) {
  this.name = name
  this.birthday = birthday

  return birthday
}

const result = new Summary('Lion', 1437)
console.log(result)
```

1. `{}`
2. `{ name: 'Lion', birthday: 1437 }`
3. `1437`
4. `SyntaxError`

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 2**
  
  Если в функции-конструкторе через `return` мы возвращаем примитивное значение — в итоге оно будет отброшено, а возвращен будет `this`.

</p>
</details>

---

##### 5. Какой будет вывод при запуске скрипта в браузере?

```javascript
function User() {
  return {}
}

console.log(new User)
console.log(new User())
```

1. `undefined`, `{}`
2. `{}`, `undefined`
3. `undefined`, `undefined`
4. `{}`, `{}`

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 4**
  
  При вызове функции-конструктора без аргументов, нет разницы между `new User` и `new User()`.  
  *Но вызова без круглых скобок считается плохой практикой.*

</p>
</details>
