<div align="center">

# Массивы

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

##### 1. Добавление элемента в конец массива

Дан массив операционных систем `os`, добавьте в него элемент `'Linux'`. Выведите полученный массив в консоль. Выведите длину полученного массива в консоль.

```js
const os = ['Windows', 'MacOS']
const linux = 'Linux'

console.log(/* ... */)
// ['Windows', 'MacOS', 'Linux']

console.log(/* ... */)
// 3
```

<details><summary><b>Подсказка</b></summary>
<p>

Для добавления элемента в массив используйте метод `push()`.

</p>
</details>

<details><summary><b>Решение</b></summary>
<p>

```js
const os = ['Windows', 'MacOS']
const linux = 'Linux'

const length = os.push('Linux')

console.log(os)
console.log(length)

// либо
console.log(os.length)
```

</p>
</details>

---

##### 2. Удаление первого элемента массива

Удалите первый элемент массива. Выведите в консоль удаленное значение, а также выведите в консоль получившийся массив.

```js
const heroes = ['Superman', 'Batman', 'Flash']

console.log(/* ... */)
// 'Superman'

console.log(/* ... */)
// ['Batman', 'Flash']
```

<details><summary><b>Подсказка</b></summary>
<p>

Для удаления первого элемента массива используйте метод `shift()`.

</p>
</details>

<details><summary><b>Решение</b></summary>
<p>

```js
const heroes = ['Superman', 'Batman', 'Flash']

console.log(heroes.shift())
console.log(heroes)
```

</p>
</details>

---

##### 3. Добавление элемента в начало массива и удаление последнего элемента

Удалите из массива последний элемент и добавьте его в начало. Выведите полученный результат в консоль.

```js
const chars = ['B', 'C', 'D', 'E', 'A']

console.log(/* ... */)
// ['A', 'B', 'C', 'D', 'E']
```

<details><summary><b>Подсказка</b></summary>
<p>

Для удаления последнего элемента используйте метод `pop()`.

Для вставки элемента в начало массива, используйте метод `unshift()`.

</p>
</details>

<details><summary><b>Решение</b></summary>
<p>

```js
const chars = ['B', 'C', 'D', 'E', 'A']

const char = chars.pop()

chars.unshift(char)

console.log(chars)
```

</p>
</details>

---

##### 4. Удаление элемента из массива

Удалите `'Bartender'` и `'Hookah master'` из массива. Выведите результат в консоль.

```js
const professions = ['HR', 'Tester', 'Hookah master', 'Frontend Developer', 'Product Manager', 'Bartender']

console.log(/* ... */)
// ['HR', 'Tester', 'Frontend Developer', 'Product Manager']
```

<details><summary><b>Подсказка</b></summary>
<p>

Для удаления элементов из массива по индексу используйте метод `splice()`.

</p>
</details>

<details><summary><b>Решение</b></summary>
<p>

```js
const professions = ['HR', 'Tester', 'Hookah master', 'Frontend Developer', 'Product Manager', 'Bartender']

professions.splice(2, 1)
professions.splice(4, 1)

console.log(professions)
```

</p>
</details>













