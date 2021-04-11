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
3. Списка аргументов, заключенных в круглые скобки `()`.
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

Аргументов может быть несколько:
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

В качестве аргумента, функция может принимать любой тип данных, включая и другие функции.

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

Источники:
* [Функции](https://developer.mozilla.org/ru/docs/Web/JavaScript/Guide/Functions)
* [`return`](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Statements/return)


