<div align="center">

# Ошибки и их обработка

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

<div align="center">

### `throw`

</div>

---

**Инструкция `throw`** — позволяет создавать пользовательские ошибки. При этом выполнение текущей функции будет остановлено (инструкции после `throw` выполнены не будут).

```js
throw 'Произошла ошибка'
// Uncaught Произошла ошибка
```

Обычно используется в связке с конструктором `Error`.

**Конструктор Error** — создает объект ошибки.

```js
throw new Error('Пользовательский текст ошибки')
// Uncaught Error: Пользовательский текст ошибки
```

---

<div align="center">

### `try ... catch ... finally`

</div>

---

**Конструкция `try ... catch`** — пытается выполнить инструкцию в блоке `try`, и, в случае ошибки, выполняется блок `catch`.

```js
try {
  console.log('Инструкция try')
} catch(err) {
  console.log('Инструкция catch')
}

// 'Инструкция try' — так как ошибока нет, то блок catch будет проигнорирован
```

В примере ниже мы выкидываем ошибку. Все инструкции в `try` до ошибки будут выполнены, а после ошибки — нет. После получения ошибки начнет выполняться инструкция `catch(err)`, где `err` — это полученная ошибка.
```js
try {
  console.log('Консоль 1')
  throw new Error()
  console.log('Консоль 2')
} catch(err) {
  console.log('Консоль 3')
}

// 'Консоль 1'
// 'Консоль 3'
```

---

**Инструкция `finally`** — блок кода, который будет выполнен в любом случае.

Можно использовать для:
- Безопасного завершения скрипта.
- Освобождения памяти и ресурсов, которые использовал скрипт.

```js
try {
  console.log('Консоль 1')
} catch(err) {
  console.log('Консоль 2')
} finally {
  console.log('Консоль 3')
}
// 'Консоль 1'
// 'Консоль 3'

try {
  throw new Error()
  console.log('Консоль 1')
} catch(err) {
  console.log('Консоль 2')
} finally {
  console.log('Консоль 3')
}
// 'Консоль 2'
// 'Консоль 3'

try {
  throw new Error()
  console.log('Консоль 1')
} catch(err) {
  throw new Error()
  console.log('Консоль 2')
} finally {
  console.log('Консоль 3')
}
// 'Консоль 3'
```

---

<div align="center">

### Типы ошибок

</div>

---

Кроме конструктора `Error`, существует еще шесть конструкторов ошибок.

---

Ошибка `ReferenceError` — выбрасывается, когда используется переменная, которая не была объявлена:

```js
console.log(num)  // переменная num нигде не объявлена
// ReferenceError: num is not defined
```

---

Ошибка `SyntaxError` — выбрасывается, если в коде была допущена синтаксическая ошибка.

```js
const = 10 + 5  // пропущено имя константы
// SyntaxError: Unexpected token '='
```

---

Ошибка `TypeError` — выбрасывается, если используется значение не поддерживаемое данным типом.

```js
const num = 10
num.toUpperCase()  // у чисел нет метода toUpperCase()
// TypeError: num.toUpperCase is not a function
```

```js
const str = 'Hello'
str.unknownMethod()  // такого метода у строк нет
// TypeError: str.unknownMethod is not a function
```

```js
const arr = [1, 2, 3]
arr()  // пытаемся вызвать массив, как функцию, что невозможно
// TypeError: arr is not a function
```

```js
undefined.name  // свойства name у undefined нет
// TypeError: Cannot read property 'name' of undefined
```

---

Ошибка `RangeError` — выбрасывается, когда число выходит за пределы допустимого диапазона.

```js
const num = 1
num.toFixed(200)  // метод поддерживает параметр от 0 до 100
// RangeError: toFixed() digits argument must be between 0 and 100
```

---

Ошибка `URIError` — выбрасывается при передаче в функцию `encodeURI()` или `decodeURI()` недопустимых параметров.

```js
decodeURI('%%%')
// URIError: URI malformed
```

---

Ошибка `EvalError` — выбрасывается, когда возникает ошибка в глобальной функции `eval()`.

---

Источники:
- [`throw`](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Statements/throw)
- [`Error`](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/Error)
- [`try ... catch`](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Statements/try...catch)
- [JavaScript Errors - Throw and Try to Catch](https://www.w3schools.com/js/js_errors.asp)
- [JavaScript ссылки на ошибки](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Errors)
