<div align="center">

# Promise

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

##### 1. Какой будет вывод?

```javascript
console.log(1)

new Promise(() => {
  console.log(3)
})

console.log(2)
```

1. `1`, `2`, `3`
2. `1`, `3`, `2`
3. `3`, `1`, `2`
4. `3`, `2`, `1`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 2**

Исполняющая функция в `Promise` будет выполнена сразу.

</p>
</details>

---
