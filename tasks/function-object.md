<div align="center">

# Работа с объектами

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

##### 1. Доступ к элементу объекта

Напишите функцию, которая принимает объект и имя. Функция должна вернуть `true`, если в переданном объекте свойство `name` совпадает с переданным именем.  
Также функция должна вывести результат в консоль.

```js
function hasProperty() { /* ... */ }

const person = { name: 'John' }

hasProperty(person, 'John')  // true
hasProperty(person, 'Donald')  // false
```

<details><summary><b>Решение</b></summary>
<p>

```js
function hasProperty(obj, name) {
  const result = obj.name === name
  console.log(result)
  return result
}
```

</p>
</details>

---

##### 2. Доступ к нескольким элементам объекта

Напишите функцию, которая принимает объект, имя, фамилию и возраст. Функция должна вернуть `true`, если переданный объект содержит имя, фамилию и возраст.  
Также функция должна вывести результат в консоль.

```js
function hasPersonalData() { /* ... */ }

const person = {
  firstName: 'John',
  lastName: 'Smith',
  age: 33
}

hasPersonalData(person, 'John', 'Smith', 33)  // true
hasPersonalData(person, 'Glen', 'Smith', 33)  // false
```

<details><summary><b>Решение</b></summary>
<p>

```js
function hasPersonalData(obj, firstName, lastName, age) {
  const result = obj.firstName === firstName && obj.lastName === lastName && obj.age === age
  console.log(result)
  return result
}
```

</p>
</details>

---

##### 3. Добавление элементов в объект

Напишите функцию, которая принимает имя и возраст. Функция должна вернуть объект вида `{ name: 'Name', age: 'Age' }`.  
Также функция должна вывести результат в консоль.

```js
function setNameAndAge() { /* ... */ }

setNameAndAge('John', 33)  // { name: 'John', age: 33 }
setNameAndAge('Glen', 28)  // { name: 'Glen', age: 28 }
```

<details><summary><b>Решение</b></summary>
<p>

```js
function setNameAndAge(name, age) {
  const person = { name: name, age: age }
  console.log(person)
}
```

</p>
</details>

---

##### 4. Перебор всех ключей

Напишите функцию, которая принимает объект и выводит в консоль все свойства этого объекта.

```js
function showProperties() { /* ... */ }

showProperties({ name: 'John', age: 33 })
// name
// age

showProperties({
  city: 'New York',
  address: 'central street, 15',
  rooms: ['kitchen', 'bedroom']
})
// city
// address
// rooms
```

<details><summary><b>Решение</b></summary>
<p>

```js
function showProperties(obj) {
  for (let key in obj) {
    console.log(key)
  }
}
```

</p>
</details>

---

##### 5. Взятие всех значений

Напишите функцию, которая принимает объект и возвращает все значения этого объекта в виде массива.  
Также функция должна вывести результат в консоль.

```js
function getValues() { /* ... */ }

getValues({ name: 'John', age: 33 })
// ['John', 33]

getValues({
  city: 'New York',
  address: 'central street, 15',
  rooms: ['kitchen', 'bedroom']
})
// ['New York', 'central street, 15', ['kitchen', 'bedroom']]
```

<details><summary><b>Решение</b></summary>
<p>

```js
function getValues(obj) {
  const result = Object.values(obj)
  console.log(result)
  return result
}
```

</p>
</details>

---

##### 6. Количество элементов

Напишите функцию, которая принимает объект все значения которого — массивы. Функция должна вернуть количество всех элементов во всех массивах.  
Также функция должна вывести результат в консоль.

```js
function getValuesLength() { /* ... */ }

const notebook = {
  A: ['Andrew', 'Ashley'],
  B: ['Brad'],
  C: ['Charlie', 'Cole']
}

const phones = {
  800: [88001009090, 88002009090],
  913: [89131009090]
}

getValuesLength(notebook)  // 5, так как всего у нас пять имен
getValuesLength(phones)  // 3, так как всего у нас три номера телефона
```

<details><summary><b>Решение 1</b></summary>
<p>

```js
function getValuesLength(obj) {
  const values = Object.values(obj)
  
  // Используем метод `flat` чтобы превратить двумерный массив в одномерный
  const length = values.flat().length
  console.log(length)
  return length
}
```

</p>
</details>


<details><summary><b>Решение 2</b></summary>
<p>

```js
function getValuesLength(obj) {
  const values = Object.values(obj)
  let length = 0

  for (let i = 0; i < values.length; i++) {
    length += values[i].length
  }

  console.log(length)
  return length
}
```

</p>
</details>

---

##### 7. Обнуление всех свойств

Напишиту функцию, которая принимает объект. Функция должна вернуть объект с теми же свойствами, но значения всех свойств должны стать `null`.  
Также функция должна вывести результат в консоль.

```js
function setValuesToNull() { /* ... */ }

setValuesToNull({ name: 'John', age: 33 })  // { name: null, age: null }
```

<details><summary><b>Решение</b></summary>
<p>

```js
function setValuesToNull(obj) {
  for (let key in obj) {
    obj[key] = null
  }

  console.log(obj)
  return obj
}
```

</p>
</details>






