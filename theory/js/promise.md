<div align="center">

# Обещания (Promise)

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

Объект **Promise** — обёртка для значения, неизвестного на момент создания.

#### Пример

Мы хотим получить из Instagram последние 20 фотографий из определенного профиля. Отправляем запрос, но у нас остаются следующие вопросы:
- Когда Instagram вышлет нам фотографии? Через секунду, через 5, через 10? Мы не знаем.
- Придут ли нам фотографии вообще? Может у нас нет доступа к профилю, или сервер Instagram'а на данный момент недоступен? На момент создания запроса мы не знаем ответ.

Промис решает эти вопросы:  
С помощью промиса, можно отправить запрос к серверу Instagram и ждать до тех пор, пока нам не придет ответ. Если запрос был выполнен успешно — то получить фотографии и использовать как нам нужно. Если сервер отклонил запрос — обработать ошибку.

---

<div align="center">

### Создание промиса

</div>

---

Promise API предоставляется конструктором `Promise`:

```js
new Promise((resolve, reject) => {
  /* part 1 */
})
  .then(() => { /* part 2 */ })
  .catch(() => { /* part 3 */ })
  .finally(() => { /* part 4 */ })
```

Промис состоит из четырех частей:
1. `part 1` — блок кода, который будет выполнен сразу.
2. `part 2` — блок кода, который будет выполнен, если сработает колбэк `resolve`.
3. `part 3` — блок кода, который будет выполнен, если сработает колбэк `reject` или если будет выброшена ошибка.
4. `part 4` — блок кода, который будет выполнен при срабатывании `resolve` или `reject`.

`then`, `catch` и `finally` — необязательные методы.

Пример успешного сценария:
```js
new Promise((resolve, reject) => {
  resolve()
})
  .then(() => console.log('Это сообщение будет выведено в консоль'))
  .catch(() => console.log('До этого блока дело не дойдет'))
```

Пример отклоненного сценария:
```js
new Promise((resolve, reject) => {
  reject()
})
  .then(() => console.log('До этого блока дело не дойдет'))
  .catch(() => console.log('Это сообщение будет выведено в консоль'))
```

Пример ошибки в промисе:
```js
new Promise((resolve, reject) => {
  throw new Error()
})
  .then(() => console.log('До этого блока дело не дойдет'))
  .catch(() => console.log('Это сообщение будет выведено в консоль'))
```

---

<div align="center">

### Состояния промиса

</div>

---

`Promise` может находиться в трёх состояниях:
- ожидание (pending) — начальное состояние, не исполнен и не отклонён.
- исполнено (fulfilled) — операция завершена успешно.
- отклонено (rejected) — операция завершена с ошибкой.

При создании, промис находится в состоянии `pending`:
```js
const promise = new Promise((resolve, reject) => {})
console.log(promise)
// Promise {<pending>}
```

Соответственно:
- Когда все операции в промисе будут успешно завершены, то его состояние изменится на `fulfilled`.
- Если в результате операций возникла ошибка, то состояние промиса изменится на `rejected`.

> В Javascript нет метода, чтобы узнать текущее состояние промиса.

---

<div align="center">

### `then`

</div>

---

Метод `.then(result)` — это функция, которая будет выполнена после вызова `resolve(params)`,  
где `result` — это параметры, которые мы передаем при вызове `resolve(params)`.

```js
new Promise((resolve, reject) => {
  setTimeout(() => resolve('Success message'), 1000)
})
  .then((result) => console.log(result))

// Через одну секунду будет выведено:
// 'Success message'
```

Метод `then()` возвращает промис. Это значит, что мы можем вызывать несколько `then()` подряд. Всё, что мы будем возвращать из `then()` — будет попадать как параметры в следующий `then()`:
```js
new Promise((resolve, reject) => {
  setTimeout(() => resolve('Success message'), 1000)
})
  .then((result) => {
    console.log(result)
    return 'Another message'
  })
  .then((result) => console.log(result))

// Через одну секунду будет выведено:
// 'Success message'
// 'Another message'
```

---

<div align="center">

### `catch`

</div>

---

Метод `.catch(err)` — это функция, которая будет выполнена после вызова `reject(params)` или при выброшенной ошибке.

Метод `catch()` используется для обработки ошибок.

```js
new Promise((resolve, reject) => {
  throw new Error('Reject error')
})
  .catch((err) => console.error(err))

// Error: Reject error
```

---

Источники:
- [Promise](https://learn.javascript.ru/promise)
- [JavaScript Promise](https://www.w3schools.com/js/js_promise.asp)
