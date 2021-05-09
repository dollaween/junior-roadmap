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
  fn: function() {
    console.log(this)
  }
}
person.fn()
// { name: "John", age: 33, fn: ƒ }
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

### `bind()`, `call()` и `apply()`

</div>

---

Метод `bind(this)` — создает новую функцию, которая в качестве контекста выполнения `this` устанавливает переданное значение. В метод также передаётся набор аргументов, которые будут установлены перед переданными в привязанную функцию аргументами при её вызове.

```js
function fn() {
  console.log(this)
}

const newFn = fn.bind({ name: 'John' })
newFn()
// { name: 'John' }
```



