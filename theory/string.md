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

```
