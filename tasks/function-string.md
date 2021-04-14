<div align="center">

# Работа со строками

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

##### 1. Вывод первого символа

Напишите функцию, которая принимает строку и возвращает первый символ строки.  
Также функция должна вывести первый символ строки в консоль.

```js
function firstChar() { /* ... */ }

firstChar('Hello')          // 'H'
firstChar('Somthing more')  // 'S'
```

<details><summary><b>Решение</b></summary>
<p>

```js
function firstChar(str) {
  const result = str[0]
  console.log(result)
  return result
}
```

</p>
</details>
