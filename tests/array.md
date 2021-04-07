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


