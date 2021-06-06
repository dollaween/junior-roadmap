<div align="center">

# Комбинаторы

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

**Комбинатор** — это оператор, который объединяет несколько селекторов.

---

**Комбинатор потомков ` ` (пробел)** — выбирает элементы, которые находятся внутри указанного элемента.

```html
<p>Example <span>first text</span></p>
<p class="paragraph">Example <span>second text</span></p>
```

```css
.paragraph span {
  color: red;
}
```

В результате, стили будут применены только к элементу `span`, который находится внутри элемента `p` с классом `paragraph`.
