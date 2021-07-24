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

Свойства для работы с текстом можно разбить на следующие категории:
- Настройка шрифта:
  - `@font-face`
  - `font`
  - `font-family`
  - `font-size`
  - `font-weight`
  - `text-transform`
- Работа с переносами и пробелами:
  - `word-spacing`
  - `letter-spacing`
  - `line-height`
  - `white-space`
  - `word-break`
  - `text-indent`
- Работа с распололожением букв:
  - `text-align`
  - `text-align-last`
  - `writing-mode`
  - `text-orientation`
- Работа с декоративной линией:
  - `text-decoration`
  - `text-decoration-line`
  - `text-decoration-color`
  - `text-decoration-style`
  - `text-decoration-thickness`
  - `text-underline-offset`
- Стилизация шрифта:
  - `color`
- Работа с переполнением:
  - `text-overflow`
  - `-webkit-line-clamp`

---

<div align="center">

### `@font-face`

</div>

---

Правило [`@font-face`](https://developer.mozilla.org/ru/docs/Web/CSS/@font-face) — загружает шрифты с удаленного сервера или компьютера пользователя.

```css
@font-face {
  font-family: "Open Sans";
  src: url("./fonts/OpenSans.woff2") format("woff2");
}
```

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

### `text-align-last`

</div>

---

> Не поддерживается в Safari

Свойство [`text-align-last`](https://developer.mozilla.org/ru/docs/Web/CSS/text-align-last) — выравнивает последнюю строку в блоке.

Значения аналогичные `text-align`.

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

### `text-decoration-color`

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

### `text-underline-offset`

</div>

---

Свойство [`text-underline-offset`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-underline-offset) — устанавливает расстояние декоративной линии от текста.

Свойство применимо только для декоративной линии со значением `text-decoration-line: underline;`.

```css
p {
  text-decoration-line: underline;
  text-underline-offset: 4px;
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

<div align="center">

### `text-orientation`

</div>

---

Свойство [`text-orientation`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-orientation) — определяет ориентацию букв в строке. Это свойство применимо только если `writing-mode` установлен в `vertical-rl`/`vertical-lr`.

Значения:
- `mixed` — поворачивает буквы на 90 градусов.
- `upright` — размещает буквы в вертикальном положении.

```css
p {
  writing-mode: vertical-rl;
  text-orientation: upright;
}
```

---

<div align="center">

### `text-overflow`

</div>

---

Свойство [`text-overflow`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-overflow) — определяет, как будет отображаться переполненный текст (переполненный — это текст, не влезающий по ширине).

По-умолчанию, текст не переполняет контейнер. Чтобы добиться переполнения, нужно задать свойства `overflow` и `white-space`. Например:

```css
overflow: hidden;
white-space: nowrap;
```

Значения:
- `clip` — переполненный текст просто обрезается (значение по-умолчанию).
- `ellipsis` — добавляет троеточие `...` в конце переполненного текста.

```css
p {
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
}
```

---

<div align="center">

### `-webkit-line-clamp`

</div>

---

> Данное свойство поддерживается только с префиксом `-webkit`.

Свойство [`-webkit-line-clamp`](https://developer.mozilla.org/en-US/docs/Web/CSS/-webkit-line-clamp) — позволяет отобразить в блоке не более чем указанное количество строк.

Это свойство работает только в связке с двумя другими свойствами:
- `display` со значением `-webkit-box` или `-webkit-inline-box`.
- `-webkit-box-orient: vertical`.

```css
p {
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-line-clamp: 3;
  overflow: hidden;
}
```

---

<div align="center">

### `text-transform`

</div>

---

Свойство [`text-transform`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-transform) — определяет, какие буквы отобразить прописными, а какие строчными.

Значения:
- `none` — не изменять текст.
- `capitalize` — первая буква каждого слова становится прописной.
- `uppercase` — все буквы становятся прописными.
- `lowercase` — все буквы становятся строчными.

```css
p {
  text-transform: uppercase;
}
```

---

<div align="center">

### `font-family`

</div>

---

Свойство [`font-family`](https://developer.mozilla.org/ru/docs/Web/CSS/font-family) — определяет шрифт текста.

Значения:
- Название шрифта. Если в названии шрифта есть пробелы, знаки пунктуации или цифры, то оно должно быть в кавычках.
- Общие семейства шрифтов:
  - `serif` — шрифт с отстрыми окончаниями.
  - `sans-serif` — шрифт с гладкими окончаниями.
  - `monospace` — моноширинный шрифт.
  - `cursive` — курсивный шрифт.
  - `fantasy` — декоративный шрифт.
  - `system-ui` — дефолтный шрифт взятый из пользовательского интерфейса данной платформы.
  - `math` — шрифт, предназначенный для математики.
  - `emoji` — шрифт, предназначенный для отображения эмодзи.
  - `fangsong` — шрифт для китайских иероглифов.

Если указать несколько шрифтов — то браузер будет использовать самый первый из них. Если использование самого первого невозможно — попробует взять второй из списка. Если и второй использовать невозможно — возьмет третий и так далее.

В конце списка важно указывать хотя бы один шрифт из общего семейства шрифтов. Это позволит браузеру использовать запасной шрифт, если никакие другие не были найдены.

Некоторые общие семейства шрифтов:
```css
.serif {
  font-family: Times, Times New Roman, Georgia, serif;
}

.sansserif {
  font-family: Verdana, Arial, Helvetica, sans-serif;
}

.monospace {
  font-family: Lucida Console, Courier, monospace;
}
```

---

Источники:
- [`@font-face`](https://developer.mozilla.org/ru/docs/Web/CSS/@font-face)
- [`color`](https://developer.mozilla.org/en-US/docs/Web/CSS/color)
- [`font`](https://developer.mozilla.org/ru/docs/Web/CSS/font)
- [`font-size`](https://developer.mozilla.org/ru/docs/Web/CSS/font-size)
- [`font-weight`](https://developer.mozilla.org/ru/docs/Web/CSS/font-weight)
- [`letter-spacing`](https://developer.mozilla.org/ru/docs/Web/CSS/letter-spacing)
- [`word-spacing`](https://developer.mozilla.org/ru/docs/Web/CSS/word-spacing)
- [`line-height`](https://developer.mozilla.org/ru/docs/Web/CSS/line-height)
- [`text-align-last`](https://developer.mozilla.org/ru/docs/Web/CSS/text-align-last)
- [`text-align`](https://developer.mozilla.org/ru/docs/Web/CSS/text-align)
- [`white-space`](https://developer.mozilla.org/ru/docs/Web/CSS/white-space)
- [`word-break`](https://developer.mozilla.org/ru/docs/Web/CSS/word-break)
- [`text-indent`](https://developer.mozilla.org/ru/docs/Web/CSS/text-indent)
- [`text-decoration`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-decoration)
- [`text-decoration-line`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-decoration-line)
- [`text-decoration-color`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-decoration-color)
- [`text-decoration-style`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-decoration-style)
- [`text-decoration-thickness`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-decoration-thickness)
- [`text-underline-offset`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-underline-offset)
- [`writing-mode`](https://developer.mozilla.org/ru/docs/Web/CSS/writing-mode)
- [`text-orientation`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-orientation)
- [`text-overflow`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-overflow)
- [`-webkit-line-clamp`](https://developer.mozilla.org/en-US/docs/Web/CSS/-webkit-line-clamp)
- [`text-transform`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-transform)
- [`font-family`](https://developer.mozilla.org/ru/docs/Web/CSS/font-family)
