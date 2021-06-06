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
<p class="first">Example <span>first text</span></p>
<p class="second">Example <span>second text</span></p>
```

```css
/* Таким образом ко всем span внутри p будут применены стили */
p span {
  color: red;
}
```

```css
/* А вот так стили будут применены только к span внутри элемента с классом second */
.second span {
  color: green;
}
```

---

**Комбинатор дочерних селекторов `>`** — выбирает элементы, которые являются непосредственно дочерними у указанного элемента.

```html
<ul class="list">
  <li>First</li>
  <li>Second</li>
  <ul class="list-inner">
    <li>Thirds</li>
  </ul>
</ul>
```

```css
.list > li {
  background: tomato;
}
```

Эти стили будут применены к элементам `li`, которые являются непосредственно дочерними у элемента с классом `list`.

---








