<div align="center">

# Логический тип (boolean), логические операторы

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

`Boolean` — логический тип данных, который может быть только двух значений: `true` (правда, истина), либо `false` (ложь).

В основном, используется в логических конструкциях `if ... else` или при работе с операторами `&&`, `||`, `!`, `>`, `<`, `>=`, `<=`, `==`, `===`.

Значения `0`, `null`, `false`, `NaN`, `undefined` преобразовываются в `false`. Все остальные значения преобразовываются в `true`.

---

Математические операторы:
* Оператор "Больше" (`>`) возвращает `true`, если левый операнд больше правого.
* Оператор "Меньше" (`<`) возвращает `true`, если левый операнд меньше правого.
* Оператор "Больше или равно" (`>=`) возвращает `true`, если левый операнд больше или равен правому.
* Оператор "Меньше или равно" (`<=`) возвращает `true`, если левый операнд меньше или равен правому.

```js
10 > 5  // true
10 < 5  // false
10 >= 5  // true
10 <= 5  // false
```

Строки сравниваются по алфавиту:
* Буква 'а' идет по-алфавиту раньше, чем буква `б`, поэтому `'а' < 'б'` будет возвращать `true`.
* Прописные (заглавные) буквы идут раньше строчных, поэтому `'А' <= 'Б'` будет `false`.
* Английские буквы идут раньше русских букв, поэтому `'G' <= 'Г'` будет `false`.

```js
'abc' < 'def'  // true
'ABC' < 'DEF'  // true
'ABC' < 'АБВ'  // true
```

Значение `true` больше `false` и `null`.

```js
true > false  // true
true > null   // true
```

---

Оператор "Логическое И" (`&&`) возвращает `true`, если оба его операнда истинны.

```js
console.log(true && true)    // true
console.log(true && false)   // false
console.log(false && true)   // false
console.log(false && false)  // false
```

---

Оператор "Логическое ИЛИ" (`||`) возвращает `true`, если один из его операндов истинен.

```js
console.log(true && true)    // true
console.log(true && false)   // true
console.log(false && true)   // true
console.log(false && false)  // false
```
---

Оператор "Логическое НЕ" (`!`) переводит `true` в `false`, и наоборот.

```js
console.log(!true)    // false
console.log(!false)   // true
console.log(!!true)   // true
console.log(!!false)  // false
```

---

Источники:
* [Выражения и операторы](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Operators)


