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


---

Источники
- [`::first-letter`](https://developer.mozilla.org/ru/docs/Web/CSS/::first-letter)
- [`::first-line`](https://developer.mozilla.org/ru/docs/Web/CSS/::first-line)
