<div align="center">

# Функции

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

**Функция** — это блок кода со входными параметрами и возвращаемым значением.

---

<div align="center">

### Объявление функций

</div>

---

Объявить функции можно двумя способами:
1. Function declaration
2. Function definition

Объявление **Function declaration** состоит из:
1. Ключевого слова `function`.
2. Имени функции.
3. Списка параметров (аргументов), заключенных в круглые скобки `()`.
4. Инструкции, которая будет выполнена после вызова функции, заключенной в `{}`.

Пример:
```js
function square(number) {
  return number * number
}

const result = square(10)
console.log(result)
// 100

const result2 = square(5)
console.log(result2)
// 25
```

Параметров может быть несколько:
```js
function sum(number1, number2) {
  return number1 + number2
}

console.log(sum(10, 5))
// 15

console.log(sum(6, 13))
// 19
```

Объявление **Function definition** состоит из:
1. Переменной, которой будет присвоена функция.
2. И далее так же, как и **function declaration**, за тем лишь исключением, что у функции может не быть имени.

```js
const square = function(number) {
  return number * number
}

console.log(square(3))
// 9
```

В качестве параметра, функция может принимать любой тип данных, включая и другие функции.

---

Оператор `return` — завершает выполнение функции и возвращает значение.

```js
function get10() {
  // return вернет то значение, которое находится сразу после него
  return 10
}

console.log(get10())
// 10
```

Операторов `return` может быть несколько.
```js
function firstLetter(str) {
  if (!str) {
    return null
  }
  return str[0]
}

console.log(firstLetter('Hello'))
// 'H'

console.log(firstLetter())
// null
```

---

<div align="center">

### Параметры по-умолчанию

</div>

---

Если параметр не был передан при вызове функции, то по-умолчанию, ему будет присвоено значение `undefined`.

```js
function showMessage(message) {
  console.log(message)
}

showMessage()
// undefined
```

Мы можем поменять значение по-умолчанию:

```js
function showMessage(message = 'Сообщение отсутствует') {
  console.log(message)
}

showMessage()
// 'Сообщение отсутствует'
```

Мы можем назначить значение по-умолчанию одному, или нескольким выбранным параметрам:

```js
// теперь у параметра `b` по-умолчанию значение `1`
function multiply(a, b = 1) {
  console.log(a * b)
}

multiply(10)
// 10
```

---

<div align="center">

### Оставшиеся параметры

</div>

---

**Оставшиеся параметры (rest parameters)** — позволяют представить неограниченное множество параметров в виде массива.

```js
function showArguments(...rest) {
  console.log(rest)
}

showArguments(10, 'Hello', true)
// [10, 'Hello', true]
```

Оставшиеся параметры:
* Собирают в себя только те параметры, которые не были уже записаны в другие переменные.
* Должны располагаться последними в списке параметров.

```js
function showNumbers(a, b, ...rest) {
  console.log(rest)
}

showNumbers(1, 2, 3, 4, 5, 6)
// [3, 4, 5, 6]
```










---

Источники:
* [Функции](https://developer.mozilla.org/ru/docs/Web/JavaScript/Guide/Functions)
* [`return`](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Statements/return)
* [Параметры по-умолчанию](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Functions/Default_parameters)
* [Оставшиеся параметры](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Functions/Rest_parameters)


