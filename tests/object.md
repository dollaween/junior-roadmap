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

---

##### 4. Какой будет вывод?

```javascript
const duplicate = {
  key: 'value 1',
  key: 'value 2'
}

console.log(duplicate)
```

1. `{ key: 'value 1', key: 'value 2' }`
2. `{ key: 'value 1' }`
3. `{ key: 'value 2' }`
4. `SyntaxError`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 3**

В объекте содержатся только уникальные свойства. Если несколько свойств имеют одно и то же имя, последнее из них перезатрет все предыдущие.

</p>
</details>

---

##### 5. Какой будет вывод?

```javascript
const route = {
  title: 'home',
  path: '/'
}

route[0] = 'main'

console.log(route)
```

1. `{ 0: 'main', title: 'home', path: '/' }`
2. `{ title: 'home', path: '/' }`
3. `{ title: 'main', path: '/' }`
4. `SyntaxError`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 1**

В квадратных скобках `[]` мы задаем новое свойство для объекта, имя которого `0`.

</p>
</details>













