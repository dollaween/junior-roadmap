<div align="center">

# Flow, Flexbox, Grid

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

##### 1. Какое из следующих свойств выровняет последний элемент `li` по правому краю родительского контейнера?

```html
<ul>
  <li>Element 1</li>
  <li>Element 2</li>
  <li>Element 3</li>
  <li class="last">Element 4</li>
</ul>
```

```css
ul {
  display: flex;
  justify-content: flex-start;
  width: 600px;
}

li {
  width: 100px;
}
```

1. `.last { align-self: flex-end }`
2. `.last { justify-content: flex-end }`
3. `.last { justify-self: end }`
4. `.last { margin-left: auto }`

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 4**

</p>
</details>

---

##### 2. Какое свойство нужно применить к элементу `.second`, чтобы он занял все свободное пространство родительского контейнера, не изменяя размеры `.first`?

```html
<div class="flex">
  <div class="first">Element 1</div>
  <div class="second">Element 2</div>
</div>
```

```css
.flex {
  display: flex;
  width: 400px;
}

.first {
  width: 100px;
}

.second {
  width: 100%;
}
```

1. `.second { flex-grow: 1 }`
2. `.second { width: 100% }`
3. `.second { width: auto }`
4. `.second { flex-shrink: 1 }`

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 1**
  
  - Свойство `flex-grow` — определяет, как много свободного пространства займет элемент. При значении `1` — элемент займет все свободное пространство.
  - Свойство `width: 100%` — растянет элемент на всю ширину, но из-за этого элемент `.first` будет уменьшен в размерах.
  - Свойство `width: auto` — сделает ширину элемента по ширине содержимого (то есть изменений не будет).
  - Свойство `flex-shrink` — определяет фактор сжатия элемента.

</p>
</details>

---

##### 3. Какие из стилей отцентрируют `.target` по горизонтали относительно родительского элемента?

```html
<div class="target"></div>
```

```css
.target {
  width: 100px;
  height: 50px;
  background: #333;
}
```

1. `.target { margin: 0 auto }`
2. `.target { display: flex; justify-content: center; }`
3. `.target { display: grid; justify-content: center; }`
4. Все вышеперечисленные

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 1**
  
  Варианты 2 и 3 будут центрировать дочерние элементы `.target`, но не сам элемент `.target`.
  
  Свойство `margin: 0 auto` — выровняет элемент `.target` по горизонтали относительно родительского элемента.

</p>
</details>

---

##### 4. Какие из стилей отцентрируют `.target` по вертикали относительно родительского элемента?

```html
<div class="target"></div>
```

```css
.target {
  width: 100px;
  height: 50px;
  background: #333;
}
```

1. `.target { margin: auto 0 }`
2. `.target { display: flex; align-items: center; }`
3. `.target { vertical-align: middle }`
4. Ни одни из вышеперечисленных

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 4**

  Без изменения родительского элемента невозможно отцентрировать `.target` по вертикали.

  - Свойства `margin: auto 0` и `vertical-align` не центрируют блочные элементы по вертикали.
  - Свойство `{ display: flex; align-items: center; }` — центрирует по вертикали только дочерние элементы.
  
  Варианты центрирования `.target` по вертикали
  1. У родительского элемента прописать `{ display: flex; align-items: center; }`.
  2. У родительского элемента прописать `{ position: relative }`, а у `.target` — `{ position: absolute; top: 50%; transform: translateY(-50%) }`.

</p>
</details>


