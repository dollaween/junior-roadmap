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

### `try ... catch`

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
