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

##### 2. Количество элементов в массиве

Напишите функцию, которая принимает массив и возвращает количество его элементов.  
Также функция должна вывести результат в консоль.

```js
function getArrayLength() { /* ... */ }

const arr = ['Leonard', 'Sheldon', 'Penny', 'Howard', 'Raj']
getArrayLength(arr)  // 5
```

<details><summary><b>Решение</b></summary>
<p>

```js
function getArrayLength(arr) {
  const length = arr.length
  console.log(length)
  return length
}
```

</p>
</details>

---

##### 3. Последний элемент массива

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

##### 4. Взятие элемента массива

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

##### 5. Взятие двух элементов массива

Напишите функцию, которая принимает массив и два индекса. Функция должна вернуть новый массив из двух элементов, соответствующих передаваемым индексам. Если в функцию передано меньше, чем два индекса — функция должна вернуть `null`.  
Также функция должна вывести результат в консоль.

```js
function getTwoElements() { /* ... */ }

const arr = ['Sam', 'Din', 'Castiel', 'Crowley', 'Lilith']
getTwoElements(arr, 0, 1)  // ['Sam', 'Din']
getTwoElements(arr, 2, 4)  // ['Castiel', 'Lilith']
getTwoElements(arr, 3)     // null
getTwoElements(arr)        // null
```

<details><summary><b>Решение</b></summary>
<p>

```js
function getTwoElements(arr, index1, index2) {
  if (index1 === undefined || index2 === undefined) {
    return null
  }

  const element1 = arr[index1]
  const element2 = arr[index2]

  const result = [element1, element2]

  console.log(result)
  return result
}
```

</p>
</details>


---

##### 6. Вывод всех элементов в консоль

Напишите функцию, которая принимает массив и выводит все его элементы в консоль.  

```js
function showElements() { /* ... */ }

const arr = ['Leonard', 'Sheldon', 'Penny', 'Howard', 'Raj']
showElements(arr)
// 'Leonard'
// 'Sheldon'
// 'Penny'
// 'Howard'
// 'Raj'
```

<details><summary><b>Решение</b></summary>
<p>

```js
function showElements(arr) {
  for (let i = 0; i < arr.length; i++) {
    console.log(arr[i])
  }
}
```

</p>
</details>

---

##### 7. Первые три элемента массива

Напишите функцию, которая принимает массив и возвращает три первых его элемента.  
Также функция должна вывести результат в консоль.

```js
function getFirstThreeElements() { /* ... */ }

const arr1 = ['Leonard', 'Sheldon', 'Penny', 'Howard', 'Raj']
const arr2 = ['Sam', 'Din', 'Castiel', 'Crowley', 'Lilith']
getFirstThreeElements(arr1)  // ['Leonard', 'Sheldon', 'Penny']
getFirstThreeElements(arr2)  // ['Sam', 'Din', 'Castiel']
```

<details><summary><b>Решение</b></summary>
<p>

```js
function getFirstThreeElements(arr) {
  const result = []

  for (let i = 0; i < 3; i++) {
    const element = arr[i]
    result.push(element)
  }

  console.log(result)
  return result
}
```

</p>
</details>

---

##### 8. Последние три элемента массива

Напишите функцию, которая принимает массив и возвращает последние три его элемента.  
Также функция должна вывести результат в консоль.

```js
function getLastThreeElements() { /* ... */ }

const arr1 = ['Leonard', 'Sheldon', 'Penny', 'Howard', 'Raj']
const arr2 = ['Sam', 'Din', 'Castiel', 'Crowley', 'Lilith']
getLastThreeElements(arr1)  // ['Penny', 'Howard', 'Raj']
getLastThreeElements(arr2)  // ['Castiel', 'Crowley', 'Lilith']
```

<details><summary><b>Решение</b></summary>
<p>

```js
function getLastThreeElements(arr) {
  let result = []

  for (let i = arr.length - 3; i < arr.length; i += 1) {
    const element = arr[i]
    result.push(element)
  }

  console.log(result)
  return result
}
```

</p>
</details>

---

##### 9. Взятие множества элементов массива

Напишите функцию, которая принимает массив и сколько угодно индексов. Функция должна вернуть новый массив, состоящий из элементов, соответствующих передаваемым индексам. Если индексы в функцию не передаются, то верните `null`.  
Также функция должна вывести результат в консоль.

```js
function getElements() { /* ... */ }

const arr = ['Sam', 'Din', 'Castiel', 'Crowley', 'Lilith']
getElements(arr, 1)        // ['Din']
getElements(arr, 2, 3, 4)  // ['Castiel', 'Crowley', 'Lilith']
getElements(arr)           // null
```

<details><summary><b>Решение</b></summary>
<p>

```js
function getElements(arr, ...indexes) {
  if (indexes.length === 0) {
    return null
  }

  const result = []
  for (let i = 0; i < indexes.length; i++) {
    const index = indexes[i]
    const element = arr[index]
    result.push(element)
  }

  console.log(result)
  return result
}
```

</p>
</details>

---

##### 10. Возведение чисел в квадрат

Напишите функцию, которая принимает массив чисел и возвращает новый массив, числа которого возведены в квадрат.  
Также функция должна вывести результат в консоль.

```js
function getSquaredNumbers() { /* ... */ }

const arr = [4, 8, 15, 16, 23, 42]
getSquaredNumber(arr)  // [16, 64, 225, 256, 529, 1764]
```

<details><summary><b>Решение 1</b></summary>
<p>

```js
function getSquaredNumber(arr) {
  const result = []

  for (let i = 0; i < arr.length; i++) {
    const element = arr[i] ** 2
    result.push(element)
  }

  console.log(result)
  return result
}
```

</p>
</details>

<details><summary><b>Решение 2</b></summary>
<p>

```js
function getSquaredNumber(arr) {
  const result = arr.map(num => {
    return num ** 2
  })

  console.log(result)
  return result
}
```

</p>
</details>



















