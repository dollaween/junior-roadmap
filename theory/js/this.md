<div align="center">

# Ключевое слово `this`

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

`this` — это ссылка на некоторый объект. На какой именно объект будет указывать ссылка, зависит от того, где и как была вызвана функция, в котором он содержится.

В глобальной области видимости `this` будет указывать на глобальный объект (в браузере это объект `Window`):
```js
console.log(this)
// Window
```

В пределах функции значение `this` зависит от того, каким образом вызвана функция.  
При обычном способе вызова `this` будет ссылаться на глобальный объект:
```js
function globalFunction() {
  console.log(this)
}
globalFunction()
// Window
```

При вызове функции, как метода объекта, `this` будет ссылаться на этот объект:
```js
const person = {
  name: 'John',
  age: 33,
  speak: function() {
    console.log(this)
  }
}

person.speak()
// { name: "John", age: 33, fn: ƒ }

// this будет ссылаться на объект только если был вызван как метод.
// если вывести speak в отдельную переменную и вызвать как функцию — this потеряет связь с объектом
const speak = person.speak
speak()
// window
```

Обратите внимание, что если внутри метода вызвать функцию обычным способом, то `this` будет указывать, как и положено, на глобальный объект:
```js
const person = {
  method: function() {
    console.log('method', this)
    function basic() {
      console.log('basic', this)
    }
    basic()
  }
}
person.method()
// 'method', { method: f }
// 'basic', Window
```

---


<div align="center">

### `this` в стрелочных функциях

</div>

---

Стрелочные функции не имеют своего контекста выполнения, поэтому `this` в них берется из внешней функции.

```js
const fn = () => {
  console.log(this)
}
fn()
// Window
```

```js
const person = {
  name: 'John',
  method: () => {
    console.log(this)
  }
}
person.method()
// Window
```

Пример, когда `this` в стрелочных функциях будет взят из внешнего окружения:
```js
const person = {
  name: 'John',
  method: function() {
    const arrow = () => {
      console.log(this)
    }
    arrow()
  }
}
person.method()
// { name: "John", method: ƒ }
```

---

<div align="center">

### `bind()`, `call()` и `apply()`

</div>

---

Метод `bind(this, arg1, arg2, ...)` — создает новую функцию, которая в качестве контекста выполнения `this` устанавливает переданное значение. В метод также передаётся набор аргументов, которые будут установлены перед переданными в привязанную функцию аргументами при её вызове.

```js
function fn(arg1, arg2) {
  console.log(this)
  console.log(arg1)
  console.log(arg2)
}

const newFn = fn.bind({ name: 'John' }, 'Hello', 'world')
newFn()
// { name: 'John' }
// 'Hello'
// 'world'
```

---

Метод `call(this, arg1, arg2, ...)` — в отличии от метода `bind()`, этот метод сразу вызывает функцию с указанным `this` и набором параметров через запятую.
```js
function fn(arg1, arg2) {
  console.log(this)
  console.log(arg1)
  console.log(arg2)
}

fn.call({ name: 'John' }, 'Smith', 33)
// { name: 'John' }
// 'Smith'
// 33
```

---

Метод `apply(this, [args])` — делает то же самое, что и `call()`, но набор параметров задается через массив.
```js
function fn(arg1, arg2) {
  console.log(this)
  console.log(arg1)
  console.log(arg2)
}

fn.apply({ name: 'John' }, ['Smith', 33])
// { name: 'John' }
// 'Smith'
// 33
```

---

Так как в стрелочных функциях контекст берется из внешнего окружения, то привязка `this` через `bind()`, `call()` и `apply()` будет проигнорирована:
```js
const fn = (arg1, arg2) => {
  console.log(this)
  console.log(arg1)
  console.log(arg2)
}

fn.call({ name: 'John' }, 'Smith', 33)
// Window
// 'Smith'
// 33
```

---

Источники:
* [`this`](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Operators/this)
* [`bind()`](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/Function/bind)
* [`call()`](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/Function/call)
* [`apply()`](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/Function/apply)
