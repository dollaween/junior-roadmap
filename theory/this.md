
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

В глобальной области видимости и в области видимости глобальных функцию, `this` будет указывать на глобальный объект (в браузере это объект `Window`).
```js
console.log(this)
// Window
```

```js
function globalFunction() {
  console.log(this)
}
globalFunction()
// Window
```



