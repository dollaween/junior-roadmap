<div align="center">

# Дата и время

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

Для управления датой в Javascript используется объект `Date`. Экземпляр объекта `Date` содержит число миллисекунд прошедших с 1 января 1970 г. UTC.

---

<div align="center">

### Создание даты

</div>

---

Синтаксис создания экземпляра даты:

```js
new Date(value)  // value — количество миллисекунд с 1 января 1970
new Date(dateString)
new Date(year, month, day, hour, minute, second, millisecond)
```

Пример:

```js
new Date()
// 2019-06-25T15:33:35.095Z

new Date(2019)
// 1970-01-01T00:00:02.019Z

// Обычный вызов функции Date() (то есть без оператора `new`), вернет строку, вместо объекта
Date()
// Tue Jun 25 2019 22:33:47 GMT+0700 (GMT+07:00)
```

