<div align="center">

# Map и Set

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

##### 4. Какой будет вывод?

```js
const map = new Map()
map.set('name', 'John').set('age', 33)

console.log(map.entries())
```

1. `MapIterator {"name" => "John", "age" => 33}`
2. `[{ name: 'John' }, { age: 33 }]`
3. `{{ name: 'John' }, { age: 33 }}`
4. `Symbol`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 1**

`map.entries()` — возвращает итерируемый объект.

</p>
</details>

---

##### 5. Какой будет вывод?

```js
const map = new Map()
map.set({ id: 1 }, 'John')
map.set({ id: 1 }, 'Richard')
map.delete({ id: 1 })

map.forEach((value) => {
  console.log(value)
})
```

1. `undefined`
2. `John`
3. `Richard`
4. `John`, `Richard`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 4**

Объекты хранятся по ссылке. Хотя `{ id: 1 }` во всех вариантах и одинаковый, но ссылки — разные. Все три записи `{ id: 1 }` указывают на разные объекты.

</p>
</details>

---

##### 6. Какой будет вывод?

```js
const set = new Set(['User'])

console.log(set.delete('User'))
console.log(set.delete('User'))
```

1. `true`, `true`
2. `true`, `false`
3. `true`, `undefined`
4. `Set {}`, `Set {}`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 2**

Если удаляемый объект содержится в коллекции — после удаления будет возвращено `true`, иначе — `false`.

</p>
</details>

---

##### 7. Какой будет вывод?

```js
const set = new Set(['apple', 'orange', 'cherry', 'apple', 'cherry'])

console.log(set.size)
```

1. `2`
2. `3`
3. `4`
4. `5`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 2**

Коллекция `Set` хранит только уникальные значения, все дубликаты будут удалены.

</p>
</details>

---



