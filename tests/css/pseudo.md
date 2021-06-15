<div align="center">

# Псевдоклассы и псевдоэлементы

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

##### 1. Когда цвет кнопки будет становиться зеленым?

```html
<button>Example button</button>
```

```css
button:hover {
  color: green;
}
```

1. Всегда
2. При нажатии на кнопку
3. При наведении на кнопку
4. Никогда

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 3**

  Псевдокласс `:hover` срабатывает, когда пользователь наводит на элемент мышью.

</p>
</details>

---

##### 2. Когда цвет фона элемента `p` будет становиться зеленым?

```html
<p>Example text</p>
```

```css
p:active {
  background: green;
}
```

1. При нажатии на элемент
2. При наведении на элемент
3. При перемещении к элементу кнопкой TAB
4. Никогда

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 1**

  Псевдокласс `:active` срабатывает, когда пользователь активирует элемент.

</p>
</details>

---

##### 3. Когда цвет фона элемента `div` будет становиться зеленым?

```html
<div>Example text</div>
```

```css
div:focus {
  background: green;
}
```

1. При нажатии на элемент
2. При наведении на элемент
3. При перемещении к элементу кнопкой TAB
4. Никогда

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 4**

  Псевдокласс `:focus` срабатывает, когда пользователь устанавливает фокус на элементе. Но не все элементы имеют состояние "фокус" (например, `div`), его нужно добавить вручную. Для этого необходимо добавить нужному элементу атрибут `tabindex`.

</p>
</details>

---

##### 4. При каком условии элемент `div` будет иметь зеленый цвет фона?

```html
<div>
  <input type="text" autofocus>
</div>
```

```css
div:focus-within {
  background: green;
}
```

1. При установке фокуса на `input`
2. При установке фокуса на `div`
3. При потере фокуса
4. Никогда

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 1**

  Псевдокласс `:focus-within` срабатывает, когда либо сам элемент имеет фокус, либо содержит элемент, который имеет фокус. Без атрибута `tabindex` на `div` установить фокус нельзя.

</p>
</details>

---

##### 5. Какой из элементов будет окрашен в зеленый цвет?

```html
<div>
  <span>First element</span>
  <div>Second element</div>
  <p>Third element</p>
</div>
```

```css
p:first-child {
  background: green;
}
```

1. `span`
2. `div`
3. `p`
4. Никакой

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 4**

  Псевдокласс `:first-child` — находит элемент, который является первым в своем родителе.

  Элемент `p` — не является первым в списке.

</p>
</details>

---

##### 6. Какой из элементов будет окрашен в зеленый цвет?

```html
<div>
  <span>First element</span>
  <p>Second element</p>
  <div>Third element</div>
</div>
```

```css
div :last-child {
  background: green;
}
```

1. `span`
2. `div`
3. `p`
4. Никакой

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 3**

  Псевдокласс `:last-child` — находит элемент, который является последним в своем родителе.

  Запись вида `div :last-child` (с пробелом перед двоеточием) аналогична записи `div *:last-child` — то есть будет найдет любой последний элемент внутри элемента `div`.

</p>
</details>


