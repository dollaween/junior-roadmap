<div align="center">

# Объекты

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

##### 1. Добавление свойства в объект

Добавьте в объект свойство `age` и выведите получившийся объект в консоль

```js
const person = {
  name: 'John'
}

/* ... */

console.log(person)
// { name: 'John', age: 33 }
```

<details><summary><b>Подсказка</b></summary>
<p>

Для добавления нового свойства к объекту, обратитесь к нему через оператор `.` или квадратные скобки `[]`.

</p>
</details>

<details><summary><b>Решение 1</b></summary>
<p>

```js
const person = {
  name: 'John'
}

person.age = 33

console.log(person)
```

</p>
</details>

<details><summary><b>Решение 2</b></summary>
<p>

```js
const person = {
  name: 'John'
}

person[age] = 33

console.log(person)
```

</p>
</details>

---

##### 2. Вывод свойств объекта

Выведите все названия свойств объекта в консоль

```js
const wallpaper = {
  width: 1920,
  height: 1080
}

/* ... */
// 'width'
// 'height'
```

<details><summary><b>Подсказка</b></summary>
<p>

Для итерации по свойствам объекта, используйте цикл `for .. in`.

</p>
</details>

<details><summary><b>Решение 1</b></summary>
<p>

```js
const wallpaper = {
  width: 1920,
  height: 1080
}

for (let key in wallpaper) {
  console.log(key)
}
```

</p>
</details>


<details><summary><b>Решение 2</b></summary>
<p>

```js
const wallpaper = {
  width: 1920,
  height: 1080
}

const keys = Object.keys(wallpaper)

keys.forEach((elem) => {
  console.log(elem)
})
```

</p>
</details>

---

##### 3. Вывод значений объекта

Выведите все значения объекта в консоль.

```js
const teapot = {
  type: 'metal',
  isNew: true
}

/* ... */
// 'metal'
// true
```

<details><summary><b>Подсказка</b></summary>
<p>

Для итерации по значениям объекта, используйте цикл `for .. in`.

</p>
</details>

<details><summary><b>Решение 1</b></summary>
<p>

```js
const teapot = {
  type: 'metal',
  isNew: true
}

for (let key in teapot) {
  console.log(teapot[key])
}
```

</p>
</details>

<details><summary><b>Решение 2</b></summary>
<p>

```js
const teapot = {
  type: 'metal',
  isNew: true
}

const values = Object.values(teapot)

values.forEach((elem) => {
  console.log(elem)
})
```

</p>
</details>














