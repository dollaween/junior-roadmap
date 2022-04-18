<div align="center">

# Конструктор, прототипы, `this`

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
console.log(this)
```

1. `Window`
2. `Global`
3. `{}`
4. `ReferenceError`

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 1**
  
  В глобальной области видимости `this` будет указывать на глобальный объект (в браузере это объект `Window`).

</p>
</details>

---

##### 2. Какой будет вывод при запуске скрипта в браузере?

```javascript
const person = {
  name: 'John',
  getInfo: () => {
    console.log(this)
  }
}

person.getInfo()
```

1. `Window`
2. `{ name: 'John', getInfo: ƒ }`
3. `{}`
4. `{ getInfo: ƒ }`

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 1**

  Стрелочные функции не имеют своего контекста выполнения, поэтому `this` в них берется из внешней функции.

</p>
</details>

---

##### 3. Какой будет вывод при запуске скрипта в браузере?

```javascript
const phone = {
  model: 'Samsung',
  getModel: function() {
    function getInfo() {
      console.log(this)
    }
    
    getInfo()
  }
}
```

1. `Window`
2. `{ model: 'Samsung', getModel: ƒ }`
3. `{ getInfo: ƒ }`
4. `{}`

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 1**

  В пределах функции значение `this` зависит от того, каким образом вызвана функция.  
  При обычном способе вызова функции `this` будет ссылаться на глобальный объект.

</p>
</details>

---

##### 4. Какой будет вывод при запуске скрипта в браузере?

```javascript
const burn = {
  buy: function() {
    console.log(this)
  },
  cost: 99.00
}
```

1. `Window`
2. `{ buy: ƒ, cost: 99.00 }`
3. `{ buy: ƒ }`
4. `{}`

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 2**

  При вызове функции, как метода объекта, `this` будет ссылаться на этот объект.

</p>
</details>

---

##### 5. Какой будет вывод при запуске скрипта в браузере?

```javascript
function sayHi() {
  console.log(this)
}
```

1. `Window`
2. `{ sayHi: ƒ }`
3. `{}`
4. `undefined`

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 1**
  
  В пределах функции значение `this` зависит от того, каким образом вызвана функция.  
  При обычном способе вызова `this` будет ссылаться на глобальный объект.

</p>
</details>

---


