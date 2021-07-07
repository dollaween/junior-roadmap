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

<div align="center">

### `word-break`

</div>

---

Свойство [`word-break`](https://developer.mozilla.org/ru/docs/Web/CSS/word-break) — определяет, где будет установлен перевод на новую строку, если слово не вмещается в блок.

Значения:
- `normal` — перевод будет осуществляться только на месте пробельных символов. Если слово начинается с начала блока и не влезает в него — то оно не будет никак обработано.
- `break-all` — если слово не вмещается, то остаток будет перенесен на новую строку.

```css
p {
  word-break: break-all;
}
```

---

<div align="center">

### `text-indent`

</div>

---

Свойство [`text-indent`](https://developer.mozilla.org/ru/docs/Web/CSS/text-indent) — определяет размер отступа перед первой строкой блока.

```css
p {
  text-indent: 30px;
}
```

---

<div align="center">

### `text-decoration`

</div>

---

Свойство [`text-decoration`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-decoration) — это сокращение для свойств `text-decoration-line`, `text-decoration-color`, `text-decoration-style` и `text-decoration-thickness`.

---

<div align="center">

### `text-decoration-line`

</div>

---

Свойство [`text-decoration-line`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-decoration-line) — определяет декоративную линию у текста.

Значения:
- `none` — линия отсутствует.
- `underline` — линия под текстом.
- `overline` — линия над текстом.
- `line-through` — линия, зачеркивающая текст.
- `underline overline` — можно указать несколько значений одновременно.

```css
p {
  text-decoration: underline;
}
```

---

<div align="center">

### `text-decoration-line`

</div>

---

Свойство [`text-decoration-color`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-decoration-color) — определяет цвет декоративной линии.

```css
p {
  text-decoration-line: underline;
  text-decoration-color: red;
}
```

---

<div align="center">

### `text-decoration-style`

</div>

---

Свойство [`text-decoration-style`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-decoration-style) — определяет вид декоративной линии.

Значения:
- `solid` — сплошная линия.
- `double` — двойная линия.
- `dotted` — линия из точек.
- `dashed` — пунктирная линия.
- `wavy` — волнистая линия.

```css
p {
  text-decoration-line: underline;
  text-decoration-style: dashed;
}
```

---

<div align="center">

### `text-decoration-thickness`

</div>

---

Свойство `text-decoration-thickness` — определяет толщину декоративной линии.

```css
p {
  text-decoration-line: underline;
  text-decoration-thickness: 4px;
}
```

---

<div align="center">

### `writing-mode`

</div>

---

Свойство [`writing-mode`](https://developer.mozilla.org/ru/docs/Web/CSS/writing-mode) — определяет как будет расположено содержимое — вертикально или горизонтально.

Значения:
- `horizontal-tb` — содержимое будет расположено по горизонтали слева направо, по вертикали — сверху вниз.
- `horizontal-bt` — содержимое будет расположено по горизонтали слева направо, по вертикали — снизу вверх.
- `vertical-rl` — содержимое будет расположено по вертикали сверху вниз, по горизонтали — справа налево.
- `vertical-lr` — содержимое будет расположено по вертикали сверху вниз, по горизонтали — слева направо.

```css
p {
  writing-mode: vertical-rl;
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
- [`word-break`](https://developer.mozilla.org/ru/docs/Web/CSS/word-break)
- [`text-indent`](https://developer.mozilla.org/ru/docs/Web/CSS/text-indent)
- [`text-decoration`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-decoration)
- [`text-decoration-line`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-decoration-line)
- [`text-decoration-color`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-decoration-color)
- [`text-decoration-style`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-decoration-style)
- [`writing-mode`]([`writing-mode`](https://developer.mozilla.org/ru/docs/Web/CSS/writing-mode))
