<div align="center">

# Тесты на знание базы CSS

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

##### 1. Какое значение свойства `color` будет у элемента `p`?

```html
<div>
  <p>Example text</p>
</div>
```

```css
div {
  color: green;
}
```

1. `black`
2. `green`
3. `transparent`
4. `default`

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 2**

  Так как свойство `color` у элемента `p` не задано, то оно будет унаследовано у родительского элемента. То есть значение будет равно `green`.

</p>
</details>

---

##### 2. Какое значение свойства `border` будет у `p` и `span`?

```html
<div>
  <p>Example <span>text</span></p>
</div>
```

```css
div {
  border: 1px solid blue;
}

p {
  border: inherit;
}

span {
  border: inherit;
}
```

1. `p: none`, `span: none`
2. `p: 1px solid blue`, `span: 1px solid blue`
3. `p: 1px solid blue`, `span: none`
4. `p: none`, `span: 1px solid blue`

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 2**

  Значение `inherit` — наследует значение свойства у родительского элемента.
  
  В данном случае, элемент `p` получает синюю рамку от своего родителя `div`. Затем `span` получает рамку от элемента `p`.

</p>
</details>

---

##### Какое значение свойства `border` будет у `p` и `span`?

```html
<div>
  <p>Example <span>text</span></p>
</div>
```

```css
div {
  border: 1px solid blue;
}

p {
  border: unset;
}

span {
  border: inherit;
}
```

1. `p: none`, `span: none`
2. `p: 1px solid blue`, `span: 1px solid blue`
3. `p: 1px solid blue`, `span: none`
4. `p: none`, `span: 1px solid blue`

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 1**
  
  `unset` — возвращает свойству его естественное значение. Если свойство наследуется — действует как `inherit`, иначе действует как `initial`.

  Свойство `border` не наследуется, поэтому его значение будет установлено в `initial`. То есть у элемента `p` рамки не будет.

  Раз у элемента `p` рамки нет, то и у `span` рамки не будет.

</p>
</details>


