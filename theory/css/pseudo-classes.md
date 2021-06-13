<div align="center">

# Псевдоклассы

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

**Псевдокласс** — это ключевое слово, добавленное к селектору, которое определяет его особое состояние.

Псевдоклассы позволяют добавлять стили к элементам, основываясь на позиции курсора мыши (`:hover`), состоянии содержимого (`:checked`) или истории посещения (`:visited`).

---

<div align="center">

### `:hover`

</div>

---

Псевдокласс `:hover` срабатывает, когда пользователь наводит на элемент мышью.

В примере ниже, при наведении на элемент `button` курсора мыши, будет меняться его цвет фона:

```css
button {
  background: #333;
  color: #fff;
}

button:hover {
  background: #666;
}
```


---

<div align="center">

### `:active`

</div>

---

Псевдокласс `:active` срабатывает, когда пользователь активирует элемент.  
"Активирует" — означает время между нажатием и отпусканием кнопки мыши.

В примере ниже, при нажатии на элемент будет меняться цвет фона:

```css
button {
  background: #333;
  color: #fff;
}

button:active {
  background: #666;
}
```

---

<div align="center">

### `:focus`

</div>

---

Псевдокласс `:focus` срабатывает, когда пользователь устанавливает фокус на элементе.

Фокус можно установить путем:
1. Нажатия на элемент.
2. Перемещения к элементу с помощью клавиши TAB на клавиатуре.

```css
input {
  background: #fff;
}

input:focus {
  background: #ccc;
}
```

По-умолчанию, при установке фокуса на элемент, у него будет присутствовать рамка (свойство `outline`). Чтобы убрать эту рамку нужно установить `outline: none`.

```css
input:focus {
  background: #ccc;
  outline: none;
}
```

Не все элементы имеют состояние "фокус" (например, `div`), но его можно добавить вручную. Для этого необходимо добавить нужному элементу атрибут `tabindex`.

```html
<div tabindex="0"></div>
```

```css
div {
  width: 100px;
  height: 50px;
  background: green;
}

div:focus {
  background: orange;
}
```

---

<div align="center">

### `:focus-within`

</div>

---

Псевдокласс `focus-within` срабатывает, когда либо сам элемент имеет фокус, либо содержит элемент, который имеет фокус.

```html
<div>
  <input type="text">
</div>
```

```css
div {
  padding: 20px;
  background: #ccc;
}

div:focus-within {
  background: orange;
}
```

---

<div align="center">

### `:first-child`

</div>

---

Псевдокласс `:first-child` — находит элемент, который является первым в своем родителе.

В примере ниже, первый элемент `li` будет иметь красный цвет.

```html
<ul>
  <li>Element 1</li>
  <li>Element 2</li>
  <li>Element 3</li>
  <li>Element 4</li>
</ul>
```

```css
li:first-child {
  color: red;
}
```

---

<div align="center">

### `:last-child`

</div>

---

Псевдокласс `:last-child` — находит элемент, который является последним в своем родителе.

В примере ниже, последний элемент `li` будет иметь красный цвет.

```html
<ul>
  <li>Element 1</li>
  <li>Element 2</li>
  <li>Element 3</li>
  <li>Element 4</li>
</ul>
```

```css
li:last-child {
  color: red;
}
```

---

<div align="center">

### `:nth-child()`

</div>

---

Псевдокласс `:nth-child()` — находит элемент на указанной позиции.

```html
<ul>
  <li>Element 1</li>
  <li>Element 2</li>
  <li>Element 3</li>
  <li>Element 4</li>
  <li>Element 5</li>
  <li>Element 6</li>
</ul>
```

```css
/* Второй элемент `li` будет иметь красный цвет. */
li:nth-child(2) {
  color: red;
}


/* Третий элемент `li` будет иметь синий цвет. */
li:nth-child(3) {
  color: blue;
}
```

Кроме указания конкретного элемента, поддерживаются два ключевых слова:
- `even` — все нечетные элементы.
- `odd` — все четные элементы.

```css
/* Все нечетные элементы `li` будут иметь зеленый фон */
li:nth-child(even) {
  backgorund: green;
}


/* Все четные элементы `li` будут иметь оранжевый фон */
li:nth-child(odd) {
  background: orange;
}
```

Также, если добавить к порядковому номеру букву `n` — тогда стили будут применены к каждому `n`-ому элементу:

```css
/* Эти стили будут применены к каждому третьему элементу `li` */
li:nth-child(3n) {
  font-size: 30px;
}
```

---

<div align="center">

### `:first-of-type`, `:last-of-type`, `:nth-of-type()`

</div>

---

В отличии от `first-child`, псевдокласс `first-of-type` находит первый элемент указанного типа (тега).

```html
<div>
  <span>Example span 1</span>
  <span>Example span 2</span>
  <p>Example p 1</p>
  <p>Example p 2</p>
</div>
```

```css
/* Первый элемент `p` будет иметь красный цвет */
p:first-of-type {
  color: red;
}

/* А вот эти стили применены не будут, так как элемент `p` — не первый среди всех элементов родителя */
p:first-child {
  background: orange;
}
```

Псевдокласс `:last-of-type` — действует по аналогии с `last-child`, но находит последний элемент указанного типа (тега).

Псевдокласс `:nth-of-type()` — действует по аналогии с `:nth-child()`, но также находит только элементы указанного типа (тега).

---

<div align="center">

### `:only-child`

</div>

---

Псевдокласс `:only-child` — находит элемент, являющийся единственным потомком родителя.

```html
<ul>
  <li>Example element</li>
</ul>

<ul>
  <li>Example element 1</li>
  <li>Example element 2</li>
</ul>
```

```css
/*
 * Эти стили будут применены к элементу `li` в первом `ul`, так как `li` является единственным потомком.
 * Во втором списке `ul` к `li` стили применены не будут, так как потомков два.
 */
li:only-child {
  color: green;
}
```

---

<div align="center">

### `:only-of-type`

</div>

---

Псевдокласс `:only-of-type` — находит элемент, который является единственным потомком такого типа (тега).

```html
<div>
  <span>Example span</span>
  <p>Example p</p>
</div>

<div>
  <span>Example span</span>
  <p>Example p 1</p>
  <p>Example p 2</p>
</div>
```

```css
/*
 * Эти стили будут применены к `p` в первом `div`, так как в нем `p` является единственным элементом такого типа.
 * Второй `div` содержит два элемента типа `p`, поэтому к ним стили применены не будут.
 */
p:only-of-type {
  background: orange;
}
```

---

<div align="center">

### `:not()`

</div>

---

Псевдокласс `:not()` — исключает из нахождения элементы, которые указаны внутри скобок.

```html
<p>Example text 1</p>
<p class="dont-use-it">Example text 2</p>
<p class="dont-use-it">Example text 3</p>
<p>Example text 4</p>
```

```css
/* Эти стили будут применены ко всем элементам `p`, у которых нет класса `dont-use-it` (то есть к первому и четвертому) */
p:not(.dont-use-it) {
  color: orange;
}

/* Эти стили будут применены ко всем элементам `p`, кроме последнего */
p:not(p:last-child) {
  background: green;
}
```


---

Источники:
- [`:hover`](https://developer.mozilla.org/ru/docs/Web/CSS/:hover)
- [`:active`](https://developer.mozilla.org/ru/docs/Web/CSS/:active)
- [`:focus`](https://developer.mozilla.org/ru/docs/Web/CSS/:focus)
- [`:first-child`](https://developer.mozilla.org/ru/docs/Web/CSS/:first-child)
- [`:last-child`](https://developer.mozilla.org/ru/docs/Web/CSS/:last-child)
- [`:nth-child()`](https://developer.mozilla.org/ru/docs/Web/CSS/:nth-child)
- [`:first-of-type`](https://developer.mozilla.org/ru/docs/Web/CSS/:first-of-type)
- [`:last-of-type`](https://developer.mozilla.org/ru/docs/Web/CSS/:last-of-type)
- [`:nth-of-type()`](https://developer.mozilla.org/ru/docs/Web/CSS/:nth-of-type)
- [`:only-child`](https://developer.mozilla.org/ru/docs/Web/CSS/:only-child)
- [`:only-of-type`](https://developer.mozilla.org/ru/docs/Web/CSS/:only-of-type)
- [`:not()`](https://developer.mozilla.org/ru/docs/Web/CSS/:not)

