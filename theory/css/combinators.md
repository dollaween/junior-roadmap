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
<div class="first">
  <p>Example <span>first text</span></p>
</div>
<div class="second">
  <p>Example <span>second text</span></p>
</div>
```

```css
/* Таким образом ко всем 'p' внутри 'div' будут применены стили */
div p {
  color: red;
}
```

```css
/* А вот так стили будут применены только к 'p' внутри элемента с классом second */
.second p {
  color: green;
}
```

```css
/* Комбинаторов потомков может быть несколько */
.first p span {
  color: teal;
}
```

```css
/* Уровень вложенности может быть любым */
/* span не является прямым дочерним элементом .second, но стили к нему все равно будут применены */
.second span {
  color: cyan;
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









