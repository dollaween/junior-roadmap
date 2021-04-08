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

##### 1. Добавление элемента в массив

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

os.push('Linux')

console.log(os)
console.log(os.length)
```

</p>
</details>



