<div align="center">

# `Map`

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

```js
const map = new Map([
  [1, 'Daniel'],
  [1, 'Sam']
])

for (let value of map.values()) {
  console.log(value)
}
```

1. `Daniel`
2. `Sam`
3. `Daniel`, `Sam`
4. `1`, `1`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 2**

В случае, если ключ не уникален – последнее значение перезапишет предыдущее.

</p>
</details>

---

