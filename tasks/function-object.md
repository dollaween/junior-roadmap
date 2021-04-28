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

##### 1. Добавление элементов в объект

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

