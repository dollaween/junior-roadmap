<div align="center">

# Условные инструкции

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

Для работы с логическим типом данных в Javascript представлено три логических инструкции: `if ... else`, тернарный оператор `.. ? .. : ..` и `switch`.

---

**Инструкция `if ... else`** — выполняет инструкцию `if`, если указанное условие истинно (`true`), иначе будет выполнена инструкция `else`.

```js
if (true) {
  console.log('Эта инструкция будет выполнена, потому что в блоке `if` условие истинно')
}

if (false) {
  console.log('Эта инструкция выполнена не будет')
}
```

Примеры:
```js
// Пример 1
const a = 10
const b = 5

if (a > b) {
  console.log('Выполнено, так как условие истинно')
}

// Пример 2
const password = '123'

if (password === 'abc') {
  console.log('Не выполнено, так как условие ложно')
}
```

Если условие ложно, то будет исполнена инструкция `else`:
```js
const login = 'moderator'

if (login === 'admin') {
  console.log('Эта инструкция не будет исполнена')
} else {
  console.log('А вот эта инструкция будет выполнена')
}
```

Можно вкладывать несколько условий, которые будут проверяться сверху вниз одна за другой. Если одно из условие истинно, то оно будет исполнено, а все последующие — нет:
```js
const age = 17

if (age >= 18) {
  console.log('Вам можно посещать данный сайт')
} else if (age < 18 && age >= 16) {
  // эта инструкция будет исполнена
  console.log('Посещать данный сайт можно только с разрешения родителей')
} else {
  console.log('Вам не рекомендуется посещать данный сайт')
}
```

---

**Условный (тернарный) оператор** — укороченный вариант инструкции `if ... else`.

Сперва пишется условие, за которым следует знак вопроса `?`, затем выражение которое должно быть выполнено, если условие истинно, затем знак двоеточия `:` и выражение которое должно быть выполнено, если условие ложно.

```js
const age = 18

age >= 18 ? console.log('Вход выполнен!') : console.log('Отказано в доступе')
// 'Вход выполнен'

age > 20 ? console.log('Вход выполнен!') : console.log('Отказано в доступе')
// 'Отказано в доступе'
```

---

**Инструкция `switch`** — сравнивает выражение со случаями `case`, перечисленными внутри неё, а затем выполняет соответствующие инструкции.

```js
const role = 'moderator'

switch (role) {
  case 'admin':
    console.log('У вас полный доступ к сайту')
    break
  case 'moderator':
    console.log('У вас доступ на создание и редактирование новостей')
    break
  default:
    console.log('У вас нет доступа')
}

// 'У вас доступ на создание и редактирование новостей'
```

Можно перечислить несколько случаев `case`:
```js
// если переменная `country` равна 'Russia', 'Ukraine' или 'Kazakhstan' — будет выполнена первая инструкция
const country = 'Russia'

switch (country) {
  case 'Russia':
  case 'Ukraine':
  case 'Kazakhstan':
    console.log('Язык по-умолчанию: русский')
    break
  default:
    console.log('Язык по-умолчанию: английский')
}

// 'Язык по-умолчанию: русский'
```

---

Источники:
* [`if ... else`](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Statements/if...else)
* [Тернарный оператор](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Operators/Conditional_Operator)
* [`switch`](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Statements/switch)





