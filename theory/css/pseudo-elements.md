<div align="center">

# Псевдоэлементы

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

Псевдоэлемент — это ключевое слово, добавляемое к селектору, которое позволяет стилизовать определенную часть выбранного элемента или добавить в разметку новый HTML-элемент.

> Псевдоэлементы правильно писать с двумя двоеточиями `::`, но никаких ошибок не будет, если писать их с одинарным двоеточием `:` (это сделано в рамках совместимости с предыдущими версиями CSS).

---

<div align="center">

### `::first-letter`

</div>

---

Псевдоэлемент `::first-letter` — применяет стили к первой букве первой строки блочного элемента.

```html
<p>Example text</p>
```

```css
/* Стили будут применены к букве `E` */
p::first-letter {
  color: red;
  font-size: 22px;
}
```

---

<div align="center">

### `::first-line`

</div>

---

Псевдоэлемент `::first-line` — применяет стили к первой строке блочного элемента.

```html
<p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Iste ratione iure, magni nam dicta laboriosam soluta eos incidunt, voluptatem expedita.</p>
```

```css
/* Стили будут применены к первой строке */
p::first-line {
  color: orange;
  font-size: 72px;
}
```

---

<div align="center">

### `::after`

</div>

---

Псевдоэлемент `::after` — создает псевдоэлемент (HTML-элемент), который является последним потомком выбранного элемента.

```html
<a href="#">Перейти по ссылке</a>
```

```css
/* После ссылки будет создан элемент со стрелочкой */
a::after {
  content: "→";
}
```

---

<div align="center">

### `::before`

</div>

---

Псевдоэлемент `::before` — аналогичен псевдоэлементу `::after` за той лишь разницей, что элемент создается перед всеми потомками выбранного элемента.

---

<div align="center">

### `::selection`

</div>

---

Псевдоэлемент `::selection` — применяет стили к части документа, которую выделил пользователь (например, мышью).

```html
<p>Example text</p>
```

```css
/* Стили применятся тогда, когда пользователь выделит текст в элементе `p` */
p::selection {
  background: green;
  color: white;
}
```

---

<div align="center">

### `::placeholder`

</div>

---

Псевдоэлемент `::placeholder` — применяет стили к тексту placeholder в `<input>` или `<textarea>`.

```html
<input type="text" placeholder="Введите логин">
```

```css
input::placeholder {
  color: red;
}
```

---

Источники
- [`::first-letter`](https://developer.mozilla.org/ru/docs/Web/CSS/::first-letter)
- [`::first-line`](https://developer.mozilla.org/ru/docs/Web/CSS/::first-line)
- [`::after`](https://developer.mozilla.org/ru/docs/Web/CSS/::after)
- [`::before`](https://developer.mozilla.org/ru/docs/Web/CSS/::before)
- [`::selection`](https://developer.mozilla.org/ru/docs/Web/CSS/::selection)
- [`::placeholder`](https://developer.mozilla.org/ru/docs/Web/CSS/::placeholder)
