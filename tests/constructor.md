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

phone.getModel()
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

burn.buy()
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

sayHi()
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

##### 6. Какой будет вывод при запуске скрипта в браузере?

```javascript
const phone = {
  model: 'Samsung',
  getModel: function() {
    const getInfo = () => {
      console.log(this)
    }

    getInfo()
  }
}

phone.getModel()
```

1. `Window`
2. `{ model: 'Samsung', getModel: ƒ }`
3. `{ getInfo: ƒ }`
4. `{}`

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 2**

  Стрелочные функции не имеют своего контекста выполнения, поэтому this в них берется из внешней функции.  
  В нашем случае, `this` будет браться у функции `getModel`.

</p>
</details>

---

##### 7. Какой будет вывод при запуске скрипта в браузере?

```javascript
function getGood() {
  console.log(this)
}

getGood.call({ cost: 17.50 }, 'Orbit', 'London')
```

1. `Window`
2. `{ cost: 17.50, 'Orbit', 'London' }`
3. `{ cost: 17.50, ['Orbit'] }`
4. `{ cost: 17.50 }`

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 4**

   Метод `call(this, arg1, arg2, ...)` — сразу вызывает функцию с указанным `this` и набором параметров через запятую.  
   В нашем примере в `this` попадет только объект `{ cost: 17.50 }`, остальные параметры должны быть записаны в аргументы функции.

</p>
</details>

---

##### 8. Какой будет вывод при запуске скрипта в браузере?

```javascript
function getGood(args) {
  console.log(this, args)
}

getGood.apply({ cost: 17.50 }, 'Orbit', 'London')
```

1. `Window`
2. `{ cost: 17.50, 'Orbit', 'London' }`
3. `{ cost: 17.50, ['Orbit'] }`
4. `TypeError`

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 4**
 
   Метод `apply(this, [args])` — сразу вызывает функцию с указанным `this` и набором параметров через запятую.  
   Вторым параметром должен быть массив, мы же передаем строку, что и приводит к ошибке.

</p>
</details>

---

##### 9. Какой будет вывод при запуске скрипта в браузере?

```javascript
function showInfo(args) {
  console.log(this, args)
}

showInfo.call({ cost: 17.50 }, 'Orbit', 'London')
```

1. Вывода в консоль не произойдет
2. `{ cost: 17.50 } 'Orbit' 'London'`
3. `{ cost: 17.50 } 'Orbit'`
4. `{ cost: 17.50 } ['Orbit', 'London']`

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 3**
 
  Метод `call(this, arg1, arg2, ...)` — сразу вызывает функцию с указанным `this` и набором параметров через запятую.  
  Первый переданный параметр `'Orbit'` присваивается в переменную `args`, для второго параметра мы не указали переменную, поэтому он никуда не попадет.

</p>
</details>

---

##### 10. Какой будет вывод при запуске скрипта в браузере?

```javascript
function showInfo(args) {
  console.log(this, args)
}

showInfo.apply({ cost: 17.50 }, ['Orbit', 'London'])
```

1. Вывода в консоль не произойдет
2. `{ cost: 17.50 } 'Orbit' 'London'`
3. `{ cost: 17.50 } 'Orbit'`
4. `{ cost: 17.50 } ['Orbit', 'London']`

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 3**
 
  Метод `apply(this, [args])` — сразу вызывает функцию с указанным `this` и параметрами в виде массива.  
  Хотя параметр и передается в виде массива, в самой функции элементы массива присваиваются отдельным переменным.

  В нашем примере, в параметр `args` попало значение `'Orbit'`, а значение `'London'` мы никуда не записываем.

</p>
</details>

---

##### 11. Какой будет вывод при запуске скрипта в браузере?

```javascript
function setMessage(text) {
  console.log(this, text)
}

setMessage.bind({ person: 'John' }, 'Hello, user')
```

1. Вывода в консоль не произойдет
2. `{ person: 'John' } 'Hello, user'`
3. `{ person: 'John' }`
4. `'Hello, user'`

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 1**

  Метод `bind(this, arg1, arg2, ...)` — создает новую функцию, которая в качестве контекста выполнения `this` устанавливает первое переданное значение. В метод также передаётся набор аргументов, которые будут установлены перед переданными в привязанную функцию аргументами при её вызове.
 
  Сама по себе функция не вызывается, поэтому вывода в консоль не произойдет.

</p>
</details>

---


