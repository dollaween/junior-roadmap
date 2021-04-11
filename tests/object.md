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

---

##### 6. Какой будет вывод?

```javascript
const chars = { a: '1', b: '2', c: '3' }

console.log(chars.keys())
```

1. `['a', 'b', 'c']`
2. `[1, 2, 3]`
3. `[['a', 1], ['b', 2], 'c', 3]`
4. `TypeError`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 4**

В объекте `chars` не содержится метода `keys()`. Для вызова метода `keys()` нужно обратиться к глобальному объекту `Object`:

```js
const chars = { a: '1', b: '2', c: '3' }

console.log(Object.keys(chars))
// ['a', 'b', 'c']
```

</p>
</details>

---

##### 7. Какой будет вывод?

```javascript
const domain = {
  protocol: 'https',
  host: 'google.com'
}

console.log(Object.entries(domain))
```

1. `[['protocol', 'https'], ['host', 'goolge.com']]`
2. `['protocol', 'host']`
3. `['https', 'google.com']`
4. `['protocol', 'https'], ['host', 'goolge.com']`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 1**

Метод `Object.entries()` — возвращает массив, содержащий пары `'ключ': 'значение'` в виде `['ключ', 'значение']`.

</p>
</details>

---

##### 8. Какой будет вывод?

```javascript
const PI = {
  value: 3.14159
}

console.log(Object.values(PI))
```

1. `[3.14159]`
2. `3.14159`
3. `'3.14159'`
4. `undefined`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 1**

Метод `Object.values()` — возвращает массив значений объекта.

</p>
</details>

---

##### 9. Какой будет вывод?

```javascript
const coordinates = {
  x: 115,
  y: 25
}

for (let key in coordinates) {
  console.log(key + 5)
}
```

1. `120`, `30`
2. `'1155'`, `'255'`
3. `'x120'`, `'y30'`
4. `'x5'`, `'y5'`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 4**

Цикл `for .. in` перебирает свойства объекта.

В переменную `key` будет записано свойство объекта: `'x'` на первой итерации и `'y'` на второй итерации.

</p>
</details>

---

##### 10. Какой будет вывод?

```javascript
const coordinates = {
  x: 115,
  y: 25
}

for (let key in coordinates) {
  console.log(coordinates[key] + ': ' + key)
}
```

1. `'x': 115`, `'y': 25`
2. `'x: 115'`, `'y: 25'`
3. `'115: x'`, `'25: y'`
4. `115: 'x'`, `25: 'y'`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 3**

В перемнную `key` попадает свойство объекта: `'x'` на первой итерации цикла и `'y'` на второй итерации.

`coordinates[key]` нам возвращает значение объекта по ключу `key`: `115` на первой итерации цикла и `25` на второй итерации.

Далее получаем такие строчки:
1. `console.log(115 + ': ' + 'x')`
2. `console.log(25 + ': ' + 'y')`

Что в результате дает нам третий вариант ответа.

</p>
</details>















