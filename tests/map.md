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

##### 2. Какой будет вывод?

```js
const map = new Map([
  [8, 'Daniel'],
  [3, 'Sam'],
  [5, 'Michael']
])

for (let key of map.keys()) {
  console.log(key)
}
```

1. `8`, `3`, `5`
2. `8`, `5`, `3`
3. `3`, `5`, `8`
4. `Daniel`, `Sam`, `Michael`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 1**

В отличие от объектов, Map сохраняет порядок добавления элементов.

</p>
</details>

---

##### 3. Какой будет вывод?

```js
const map = new Map()
map.set(NaN, null)

console.log(map.get(NaN))
```

1. `SyntaxError`
2. `NaN`
3. `null`
4. `undefined`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 3**

В качестве ключей, Map может хранить любой тип данных, включая NaN.

</p>
</details>

---


