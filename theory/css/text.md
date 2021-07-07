<div align="center">

# Работа с текстом

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

<div align="center">

### `color`

</div>

---

Свойство [`color`](https://developer.mozilla.org/en-US/docs/Web/CSS/color) — задает цвет текста.  
Цвет может быть указан несколькими способами (подробнее в главе [«Цвет»](./color.md)).

```css
p {
  color: green;
}
```

---

<div align="center">

### `font`

</div>

---

Свойство [`font`](https://developer.mozilla.org/ru/docs/Web/CSS/font) — это сокращение для свойств `font-style`, `font-variant`, `font-weight`, `font-stretch`, `font-size`, `line-height` и `font-family`.

---

<div align="center">

### `font-size`

</div>

---

Свойство [`font-size`](https://developer.mozilla.org/ru/docs/Web/CSS/font-size) — определяет размер шрифта.  
Размер шрифта может быть задан с помощью нескольких единиц измерения (подробнее в главе [«Единицы измерения»](./units.md))

```css
p {
  font-size: 18px;
}
```

---

<div align="center">

### `font-weight`

</div>

---

Свойство [`font-weight`](https://developer.mozilla.org/ru/docs/Web/CSS/font-weight) — определяет насыщенность шрифта (то есть его жирность).

Доступные значения:
- Числа `100`, `200`, `300`, `400`, `500`, `600`, `700`, `800`, `900`, чем больше — тем жирнее начертание шрифта. Не у всех шрифтов есть все типы начертаний, у многих есть только `400` и `700`.
- Ключевые слова `regular` (аналогичен значению `400`) и `bold` (аналогичен значению `700`).

```css
p {
  font-weight: 700;
}

span {
  font-weight: bold;
}
```

---

<div align="center">

### `letter-spacing`

</div>

---

Свойство [`letter-spacing`](https://developer.mozilla.org/ru/docs/Web/CSS/letter-spacing) — определяет расстояние между буквами в тексте.  

Положительные значения увеличивают расстояние между буквами, отрицательные значения — уменьшают.

```css
p {
  letter-spacing: 4px;
}
```

---

<div align="center">

### `word-spacing`

</div>

---

Свойство [`word-spacing`](https://developer.mozilla.org/ru/docs/Web/CSS/word-spacing) — определяет расстояние между словами в тексте.

Положительные значения увеличивают расстояние между словами, отрицательные значения — уменьшают.

```css
p {
  word-spacing: 10px;
}
```

---

<div align="center">

### `line-height`

</div>

---

Свойство [`line-height`](https://developer.mozilla.org/ru/docs/Web/CSS/line-height) — устанавливает величину пространства между строками. Больше число — больше расстояние.

```css
p {
  line-height: 24px;
}
```

---

<div align="center">

### `text-align`

</div>

---

Свойство [`text-align`](https://developer.mozilla.org/ru/docs/Web/CSS/text-align) — выравнивает линейное содержимое (такое как `inline`, `inline-block`).

Значения:
- `left` — выравнивает содержимое по левому краю.
- `right` — выравнивает содержимое по правому краю.
- `center` — выравнивает содержимое по центру.
- `justify` — выравнивает текст так, чтобы его левая и правая границы соприкасались с границами родительского контейнера.

```css
p {
  text-align: right;
}
```

---

<div align="center">

### `white-space`

</div>

---

Свойство [`white-space`](https://developer.mozilla.org/ru/docs/Web/CSS/white-space) — управляет пробельными символами.

Значения:
- `normal` — если строка не вмещается в блок — то она будет перенесена; несколько пробелов подряд будут объединены в один.
- `nowrap` — если строка не вмещается в блок — она не будет перенесена; несколько пробелов подряд будут объединены в один.
- `pre` — строки переносятся только там, где мы явно это укажем с помощью специальных символов или тега `<br>`; несколько пробелов подряд не объединяются.
- `pre-wrap` — если строка не вмещается в блок — то она будет перенесена; также строки переносятся там, где указаны специальные символы или тег `<br>`; несколько пробелов подряд не объединяются.
- `pre-line` — если строка не вмещается в блок — то она будет перенесена; также строки переносятся там, где указаны специальные символы или тег `<br>`; несколько пробелов подряд объединяются в один.
- `break-spaces` — поведение аналогично `pre-wrap` со следующими отличиями:
  - Последовательности пробелов сохраняются так, как они указаны в источнике, включая пробелы на концах строк.
  - Строки переносятся по любым пробелам, в том числе в середине последовательности пробелов.
  - Пробелы занимают место и не висят на концах строк, а значит влияют на внутренние размеры (`min-content` и `max-content`).

```css
p {
  white-space: nowrap;
}
```

---

Источники:
- [`color`](https://developer.mozilla.org/en-US/docs/Web/CSS/color)
- [`font`](https://developer.mozilla.org/ru/docs/Web/CSS/font)
- [`font-size`](https://developer.mozilla.org/ru/docs/Web/CSS/font-size)
- [`font-weight`](https://developer.mozilla.org/ru/docs/Web/CSS/font-weight)
- [`letter-spacing`](https://developer.mozilla.org/ru/docs/Web/CSS/letter-spacing)
- [`word-spacing`](https://developer.mozilla.org/ru/docs/Web/CSS/word-spacing)
- [`line-height`](https://developer.mozilla.org/ru/docs/Web/CSS/line-height)
- [`text-align`](https://developer.mozilla.org/ru/docs/Web/CSS/text-align)
- [`white-space`](https://developer.mozilla.org/ru/docs/Web/CSS/white-space)
