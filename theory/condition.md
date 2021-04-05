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

Для работы с логическим типом данных в Javascript представлено три логических инструкции: `if ... else`, `.. ? .. : ..` и `switch`.

---

Инструкция `if ... else` — выполняет инструкцию `if`, если указанное условие истинно (`true`), иначе будет выполнена инструкция `else`.

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

Пример с инструкцией `else`:
```js
const login = 'moderator'

if (login === 'admin') {
  console.log('Эта инструкция не будет исполнена')
} else {
  console.log('А вот эта инструкция будет выполнена, потому что если условие ложно, то исполнится инструкция `else`')
}
```

---
