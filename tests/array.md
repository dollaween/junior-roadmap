<div align="center">

# Тесты: Array, циклы, методы, сортировка

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
const dates = [1993, 1995, 2002, 2010, 2021]

console.log(dates[2])
```

1. `1993`
2. `1995`
3. `2002`
4. `2010`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 3**

Оператор `[index]` — возвращает элемент массива по индексу `index`.

</p>
</details>

---

##### 2. Какой будет вывод?

```javascript
const colors = ['red', 'blue']

const result = colors.push('green')

console.log(colors)
console.log(result)
```

1. `['red', 'blue']`, `3`
2. `['red', 'blue', 'green']`, `3`
3. `['red', 'blue']`, `'green'`
4. `['red', 'blue', 'green']`, `green`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 2**

Метод `push()` — добавляет элемент в конец массива и возвращает длину нового массива.

</p>
</details>

---

##### 3. Какой будет вывод?

```javascript
const rooms = ['bedroom', 'kitchen', 'bathroom']

const result = rooms.pop()

console.log(rooms)
console.log(result)
```

1. `['bedroom', 'kitchen']`, `2`
2. `['bedroom', 'kitchen', 'bathroom']`, `2`
3. `['bedroom', 'kitchen']`, `'bathroom'`
4. `['bedroom', 'kitchen', 'bathroom']`, `'bathroom'`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 3**

Метод `pop()` — удаляет последний элемент массива и возвращает его значение.

</p>
</details>

---

##### 4. Какой будет вывод?

```javascript
const cars = ['BMW', 'Porsche', 'Ford']

const result = cars.unshift()

console.log(cars)
console.log(result)
```

1. `['Porsche', 'Ford']`, `2`
2. `['BMW', 'Porsche', 'Ford']`, `2`
3. `['Porsche', 'Ford']`, `3`
4. `['BMW', 'Porsche', 'Ford']`, `3`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 4**

Метод `unshift()` — добавляет один или несколько элементов в начало массива и возвращает новую длину массива.

Здесь мы ничего не добавляем в массив, поэтому он останется без изменений.

</p>
</details>

---

##### 5. Какой будет вывод?

```javascript
const notebooks = ['Macbook', 'Lenovo']

const result = notebooks.shift('HP')

console.log(notebooks)
console.log(result)
```

1. `['Lenovo']`, `'Macbook'`
2. `['HP', 'Macbook', 'Lenovo']`, `3`
3. `['Macbook', 'Lenovo']`, `2`
4. `['Lenovo']`, `1`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 1**

Метод `shift()` — удаляет первый элемент массива и возвращает его значение.

Метод не принимает никаких аргументов, поэтому при передаче в него значения `'HP'` — ни на что не влияет.

</p>
</details>

---

##### 6. Какой будет вывод?

```javascript
const chars = ['A', 'B', 'C']

chars.reverse().reverse()

console.log(chars)
```

1. `['C', 'B', 'A']`
2. `['A', 'B', 'C']`
3. `['c', 'b', 'a']`
4. `['a', 'b', 'c']`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 2**

Метод `reverse()` — переворачивает массив — первый элемент становится последним и наоборот.

Мы вызываем метод два раза — после первого вызова массив становится `['C', 'B', 'A']`, после второго — возвращается обратно к значению `['A', 'B', 'C']`.

</p>
</details>

---

##### 7. Какой будет вывод?

```javascript
const games = ['Anno', 'Age of Empires', 'StarCraft', 'XCOM']

const result = games.splice(1, 1)

console.log(games)
console.log(result)
```

1. `['Anno', 'Age of Empires', 'StarCraft', 'XCOM']`, `''`
2. `['Anno', 'StarCraft', 'XCOM']`, `'Age of Empires'`
3. `['Age of Empires', 'StarCraft', 'XCOM']`, `['Anno']`
4. `['Anno', 'StarCraft', 'XCOM']`, `['Age of Empires']`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 4**

Метод `splice(start, deleteCount)` — удаляет существующие элементы и/или добавляет новые. Возвращает **массив** удаленных значений.

</p>
</details>

---

##### 8. Какой будет вывод?

```javascript
const characters = ['Mario', 'Luigi', 'Bowser', 'Toad']

console.log(characters.indexOf('Toad'))
console.log(characters.indexOf('Wario'))
```

1. `4`, `undefined`
2. `4`, `null`
3. `3`, `-1`
4. `3`, `undefined`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 3**

Метод `indexOf()` — возвращает первый индекс, по которому данный элемент может быть найден в массиве или `-1`, если такого индекса нет.

</p>
</details>

---

##### 9. Какой будет вывод?

```javascript
const numbers = [5, 2, 1, 9, 5, 1, 8]

console.log(numbers.lastIndexOf(1))
```

1. `0`
2. `2`
3. `5`
4. `-1`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 3**

Метод `lastIndexOf()` — возвращает первый индекс, по которому данный элемент может быть найден в массиве или `-1`, если такого индекса нет.

</p>
</details>

---

##### 10. Какой будет вывод?

```javascript
const brands = ['Calvin Klein', 'Tommy Hilfiger', 'Gucci', 'Fendi']

brands.slice(0, 2)

console.log(brands)
```

1. `['Fendi']`
2. `['Gucci', 'Fendi']`
3. `['Tommy Hilfiger', 'Gucci', 'Fendi']`
4. `['Calvin Klein', 'Tommy Hilfiger', 'Gucci', 'Fendi']`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 4**

Метод `slice(start, stop)` — возвращает копию массива от индекса `start` до индекса `stop` (не включительно).

Метод не изменяет исходный массив, поэтому массив `brands` не изменится.

</p>
</details>

---

##### 11. Какой будет вывод?

```javascript
const parts = ['will', 'i', 'am']

const result = parts.join('.')

console.log(result)
```

1. `'will.i.am'`
2. `'william'`
3. `'will . i . am'`
4. `['will', '.', 'i', '.', 'am']`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 1**

Метод `join(separator)` — объединяет все элементы массива в строку.

Если указать `separator` — то он будет вставлен в строку между элементами.

</p>
</details>

---

##### 12. Какой будет вывод?

```javascript
const bools = [true, true, false, false]

const result = bools.map((elem) => !elem)

console.log(result)
```

1. `[true, true, false, false]`
2. `[false, false, true, true]`
3. `[]`
4. `undefined`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 2**

Метод `map()` — создает новый массив, выполняет переданную функцию для каждого элемента массива и заполняет результатами созданный массив.

Оператором `!` — мы переводим `true` в `false`, и наоборот.

</p>
</details>

---

##### 13. Какой будет вывод?

```javascript
const hexs = ['FFFF00', 'FF00FF', '00FFFF', '000000']

hexs.map((elem) => {
  return elem.toLowerCase()
})

console.log(hexs)
```

1. `['FFFF00', 'FF00FF', '00FFFF', '000000']`
2. `['00', '00', '00', '000000']`
3. `undefined`
4. `['ffff00', 'ff00ff', '00ffff', '000000']`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 1**

Метод `map()` — не изменяет исходный массив, поэтому после всех операций массив `hexs` останется без изменений.

</p>
</details>

---

##### 14. Какой будет вывод?

```javascript
const array = [undefined, 0, 'true']

const result = array.every((elem) => isNaN(elem))

console.log(result)
```

1. `true`
2. `false`
3. `-1`
4. `[]`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 2**

Метод `every()` — проверяет, удовлетворяют ли все элементы массива условию, заданному в передаваемой функции.

Функция `isNaN()` — проверяет, является ли значение `NaN` (не число).

* `isNaN(undefined)` —> `true`
* `isNaN('true')` —> `true`
* `isNaN(0)` —> `false`, так как `0` — число

</p>
</details>









