<div align="center">

# Работа с массивами

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

##### 1. Взятие первого элемента массива

Напишите функцию, которая принимает массив и возвращает его первый элемент.  
Также функция должна вывести результат в консоль.

```js
function getFirstElement() { /* ... */ }

getFirstElement(['Sam', 'Din'])  // 'Sam'
getFirstElement(['Castiel', 'Crowley', 'Lilith'])  // 'Castiel'
```

<details><summary><b>Решение</b></summary>
<p>

```js
function getFirstElement(arr) {
  const result = arr[0]
  console.log(result)
  return result
}
```

</p>
</details>

---

##### 2. Последний элемент массива

Напишите функцию, которая принимает массив и возвращает его последний элемент.  
Также функция должна вывести результат в консоль.

```js
function getLastElement() { /* ... */ }

getLastElement(['Sam', 'Din'])  // 'Din'
getLastElement(['Castiel', 'Crowley', 'Lilith'])  // 'Lilith'
```

<details><summary><b>Решение</b></summary>
<p>

```js
function getLastElement(arr) {
  const result = arr[arr.length - 1]
  console.log(result)
  return result
}
```

</p>
</details>


---

##### 3. Взятие элемента массива

Напишите функцию, которая принимает массив и индекс. Функция должна вернуть элемент массива, который находится по передаваемому индексу.  
Также функция должна вывести результат в консоль.

```js
function getElement() { /* ... */ }

const arr = ['Sam', 'Din', 'Castiel', 'Crowley', 'Lilith']
getElement(arr, 0)  // 'Sam'
getElement(arr, 3)  // 'Crowley'
```

<details><summary><b>Решение</b></summary>
<p>

```js
function getElement(arr, index) {
  const result = arr[index]
  console.log(result)
  return result
}
```

</p>
</details>

---

##### 4. Взятие двух элементов массива

Напишите функцию, которая принимает массив и два индекса. Функция должна вернуть массив из двух элементов, соответствующих передаваемым индексам.  
Также функция должна вывести результат в консоль.

```js
function getTwoElements() { /* ... */ }

const arr = ['Sam', 'Din', 'Castiel', 'Crowley', 'Lilith']
getTwoElements(arr, 0, 1)  // ['Sam', 'Din']
getTwoElements(arr, 2, 4)  // ['Castiel', 'Lilith']
```

<details><summary><b>Решение</b></summary>
<p>

```js
function getTwoElements(arr, index1, index2) {
  const element1 = arr[index1]
  const element2 = arr[index2]

  const result = [element1, element2]

  console.log(result)
  return result
}
```

</p>
</details>















