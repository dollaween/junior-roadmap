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

#### Зачем нужен `Promise`?

`Promise` может находиться в трёх состояниях:
- ожидание (pending): начальное состояние, не исполнен и не отклонён.
- исполнено (fulfilled): операция завершена успешно.
- отклонено (rejected): операция завершена с ошибкой.

---

<div align="center">

### Создание промиса

</div>

---

```js
new Promise((resolve, reject) => {
  /* part 1 */
}).then(() => {
  /* part 2 */
}).catch(() => {
  /* part 3 */
}).finally(() => {
  /* part 4 */
})
```

Промис состоит из четырех частей:
1. `part 1` — блок кода, который будет выполнен сразу.
2. `part 2` — блок кода, который будет выполнен, если сработает колбэк `resolve`.
3. `part 3` — блок кода, который будет выполнен, если сработает колбэк `reject` или если будет выброшена ошибка.
4. `part 4` — блок кода, который будет выполнен при срабатывании `resolve` или `reject`.

---

Источники:
- [Promise](https://learn.javascript.ru/promise)
- [JavaScript Promise](https://www.w3schools.com/js/js_promise.asp)
