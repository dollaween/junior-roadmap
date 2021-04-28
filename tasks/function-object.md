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

