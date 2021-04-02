<div align="center">

# Тесты: Boolean, NaN, undefined, null

[Главная](https://github.com/dollaween/junior-roadmap/)
|
[Карта](/roadmap/README.md)
|
[Тесты](/tests/README.md)
|
[Задачи](/tasks/README.md)

</div>

---

##### 1. Какой будет вывод?

```javascript
const a = 5
const b = 2
const c = 4

console.log(a > b + c)
```
яч
1. `true`
2. `false`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 2**

Оператор сложения `+` имеет более высокий приоритет, чем оператор больше `>`, поэтому в первую очередь будет выполнено сложение переменных `b` и `c`.

</p>
</details>
