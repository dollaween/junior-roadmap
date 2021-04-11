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

Для добавления нового свойства к объекту, обратитесь к нему через оператор `.` или квадратных скобок `[]`.

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
