<div align="center">

# Тесты: Object, циклы, методы

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
const obj = {}
obj.name = 'Object'

console.log(obj)
```

1. `{ name: 'Object' }`
2. `[object Object]`
3. `'Object'`
4. `TypeError: Константы менять нельзя!`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 1**

В константе `obj` хранится не сам объект, а ссылка на него. Поэтому при изменении свойств и значений объекта ошибки не будет, ведь ссылка на объект останется без изменений.

</p>
</details>

---

##### 2. Какой будет вывод?

```javascript
const obj = {}
obj = { name: 'Object' }

console.log(obj)
```

1. `{ name: 'Object' }`
2. `[object Object]`
3. `'Object'`
4. `TypeError: Константы менять нельзя!`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 4**

В этом примере мы в константу `obj` пытаемся поместить совершенно новый объект, что вызовет ошибку, ведь константы менять нельзя.

</p>
</details>

---

##### 3. Какой будет вывод?

```javascript
const chair = {
  product type: 'Chair',
  material: 'Wood'
}

chair.color = '#222'

console.log(chair)
```

1. `{ 'product type': 'Chair', material: 'Wood', color: '#222' }`
2. `{ 'product type': 'Chair', material: 'Wood' }`
3. `{ color: '#222' }`
4. `SyntaxError`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 4**

В определении свойства `product type` содержится ошибка. Если в имени свойства содержится пробел, то оно должно быть записано как строка:

```js
const chair = {
  'product type': 'Chair',
  material: 'Wood',
  color: '#222'
}
```

</p>
</details>


