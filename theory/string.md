<div align="center">

# Строки

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

Есть три вида записи строк:
* Одинарные кавычки `''`
* Двойные кавычки `""`
* Апострофы ``

```js
// одинарные кавычки ничем не отличаются от двойных
const hello = 'Hello'
const hi = "Hi"

// если в строке с одинарными кавычками вам нужно вставить символ одинарной кавычки, то есть два пути
// 1. Изменить внешние кавычки на двойные
"I'm programmer"
// 2. Перед символом одинарной кавычки поставить специальный символ `\`
'I\'m programmer'

// то же самое работает и с двойными кавычками
'We have "something" in storage'
"We have \"something\" in storage"

// все что внутри кавычек — это обычный текст, поэтому переменные в таких строках вызваны не будут
const name = 'John'
console.log('My name is ${name}')  // 'My name is ${name}'
```

В кавычках через апостроф можно вызывать переменные:
```js
const name = 'John'
console.log(`My name is ${name}`)  // 'My name is John'
```

---

**Конкатенация строк** — объединение нескольких строк в одну.

```js
const greet = 'Hello'
const target = 'world'

console.log(greet + target) // 'Helloworld'

// для объединения строк с пробелом, его можно вставить
console.log(greet + ' ' + target)
// либо использовать переменные в кавычках-апострофах
console.log(`${greet} ${target}`)

// либо в самой переменной добавить нужный пробел
const name = ' John'
console.log(greet + target)  // 'Hello John'
```

---

