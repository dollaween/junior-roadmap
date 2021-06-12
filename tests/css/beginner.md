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

##### 2. Какое значение свойства `border` будет у элементов `p` и `span`?

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

##### 3. Какое значение свойства `border` будет у элементов `p` и `span`?

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

---

##### 4. Какое значение свойства `color` будет у элемента `p`?

```html
<p>Example text</p>
```

```css
p {
  color: silver;
}

p {
  color: tan;
}
```

1. `silver`
2. `tan`
3. `black`
4. `inherit`

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 2**

  Какой стиль будет применен к элементу определяет **специфичность**. При одинаковой специфичности будут применены стили, указанные последними.

</p>
</details>

---

##### 5. Какие значения свойства `color` будут у первого и второго элементов `p`?

```html
<p class="blue red">Example text</p>
<p class="red blue">Example text</p>
```

```css
.blue {
  color: blue;
}

.red {
  color: red;
}
```

1. Первый — `red`, второй — `blue`
2. Первый — `blue`, второй —  `red`
3. Первый — `blue`, второй —  `blue`
4. Первый — `red`, второй —  `red`

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 4**

  При одинаковой специфичности будут применены стили, указанные последними.  
  В данном случае, последними указаны стили класса `.red`.

</p>
</details>

---

##### 6. Какое значение свойства `color` будет у элемента `span`?

```html
<div>
  <p>Exmaple <span class="purple">text</span></p>
</div>
```

```css
.purple {
  color: purple;
}

div p span {
  color: pink;
}
```

1. `purple`
2. `pink`
3. `black`
4. `inherit`

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 1**

  Селектор по классу всегда имеет более высокий приоритет (специфичность), чем селектор по типу. Поэтому значение `span` будет установлено в `purple`.

</p>
</details>

---

##### 7. Какое значение свойства `color` будет у элемента `span`?

```html
<div>
  <p>Exmaple <span>text</span></p>
</div>
```

```css
div p {
  color: aqua;
}

span {
  color: plum;
}
```

1. `aqua`
2. `plum`
3. `black`
4. `inherit`

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 2**

  Селектор `div p` не указывает прямо на элемент `span`. Селектор `span` же указывает конкретно на элемент `span`, поэтому он будет иметь более высокую специфичность.

</p>
</details>

---

##### 8. Какое значение свойства `color` будет у элемента `span`?

```html
<div class="wrapper">
  <div>
    <p>Exmaple <span class="target">text</span></p>
  </div>
</div>
```

```css
.wrapper span.target {
  color: green;
}

.wrapper div .target {
  color: red;
}
```

1. `green`
2. `red`
3. `black`
4. `unset`

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 2**

  Указанные селекторы имеют одинаковую специфичность. При одинаковой специфичности применяются стили написанные последними.

</p>
</details>

---

##### 9. Какое значение свойства `color` будет у элемента `p`?

```html
<p id="id" class="class" style="color: green">Example text</p>
```

```css
#id {
  color: red;
}

.class {
  color: blue;
}
```

1. `red`
2. `blue`
3. `green`
4. `black`

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 3**

  Инлайновые стили (стили, написанные в атрибуте `style`) имеют наивысший приоритет (специфичность). Их может перебить только указание ключевого слова `!important`.

</p>
</details>


---

##### 10. Какое значение свойства `color` будет у элемента `p`?

```html
<p id="id" class="class" style="color: green !important">Example text</p>
```

```css
#id {
  color: red !important;
}

.class {
  color: blue !important;
}
```

1. `red`
2. `blue`
3. `green`
4. `black`

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 3**

  Инлайновые стили (стили, написанные в атрибуте `style`) с ключевым словом `!important` имеют самый высокий приоритет (специфичность), их нельзя перебить ничем.

</p>
</details>

---

##### 11. Какой цвет будет у элемента `p`?

```html
<p>Example text</p>
```

```css
p {
  color: rgb(0, 255, 0);
}
```

1. `red`
2. `green`
3. `blue`
4. `black`

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 2**
  
  Функция `rgb()` принимает три параметра, которые отвечают за красный, зеленый и синий цвета. Так как на красный и синий цвета выставлены значения `0`, а на зеленый цвет выставлено максимальное значение `255`, то цвет будет зеленым.

</p>
</details>

---

##### 12. Какой цвет будет у элемента `p`?

```html
<p>Example text</p>
```

```css
p {
  color: #0000FF;
}
```

1. `red`
2. `green`
3. `blue`
4. `black`

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 3**
  
  В системе HEX первые два символа отвечают за красный, вторые — за зеленый, третие — за синий цвета. Так как на красный и зеленый цвета выставлены значения `00`, а на синий цвет выставлено максимальное значение `FF`, то цвет будет синим.

</p>
</details>

---

##### 13. Какой из элементов не будет обладать прозрачностью?

```html
<div class="first">Element 1</div>
<div class="second">Element 2</div>
<div class="third">Element 3</div>
<div class="fourth">Element 4</div>
```

```css
.first {
  color: hsl(100, 100%, 50%);
}

.second {
  color: rgba(255, 100, 37, .9);
}

.third {
  opacity: 0.4;
}

.fourth {
  color: #FF378222;
}
```

1. `.first`
2. `.second`
3. `.third`
4. `.fourth`

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 1**

</p>
</details>

---

##### 14. Какое значение свойства `font-size` будет у элемента `span`?

```html
<div>
  <p>Example <span>text</span></p>
</div>
```

```css
html {
  font-size: 16px;
}

div {
  font-size: 0.5rem;
}

p {
  font-size: 0.5rem;
}

span {
  font-size: 1rem;
}
```

1. `32px`
2. `16px`
3. `8px`
4. `4px`

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 2**
  
  `rem` — это относительная единица измерения, зависящая от значения `font-size` в теге `html`.

  `1rem` равен значению `font-size` у элемента `html`.

</p>
</details>

---

##### 15. Какое значение свойства `font-size` будет у элемента `span`?

```html
<div>
  <p>Example <span>text</span></p>
</div>
```

```css
html {
  font-size: 16px;
}

div {
  font-size: 0.5em;
}

p {
  font-size: 0.5em;
}

span {
  font-size: 1em;
}
```

1. `32px`
2. `16px`
3. `8px`
4. `4px`

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 4**
  
  `em` — это относительная единица измерения, свойство `font-size` которой зависит от значения `font-size` у родительского элемента.

  `1em` равен значению `font-size` родительского элемента.
  
  Итого получаем следующую цепочку:
  - `html` — `16px`
  - `div` — `0.5em = 16px / 2 = 8px`
  - `p` — `0.5em = 8px / 2 = 4px`
  - `span` — `1em = 4px`

</p>
</details>


---

##### 16. Какое значение свойства `padding` будет у элемента `p`?

```html
<div>
  <p>Example text</p>
</div>
```

```css
html {
  font-size: 16px;
}

div {
  font-size: 0.5em;
}

p {
  font-size: 0.5em;
  padding: 1em;
}
```

1. `32px`
2. `16px`
3. `8px`
4. `4px`

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 4**
  
  `em` — это относительная единица измерения:
  - `font-size` у элемента зависит от значения `font-size` родителя.
  - Все остальные значения свойств элемента зависят от своего `font-size`.

  Итого получаем следующую цепочку:
  - `html` — `16px`
  - `div` — `0.5em = 16px / 2 = 8px`
  
  Для элемента `p`:
  - `font-size` — `0.5em = 8px / 2 = 4px`.
  - `padding` (и все другие свойства) в качестве единицы измерения `em` берут значение относительно своего свойства `font-size` — `1em = 4px`.

</p>
</details>

---

##### 17. Какие значения свойства `padding` будут у элементов `button`?

```html
<button class="small">Small button</button>
<button class="large">Large button</button>
```

```css
html {
  font-size: 16px;
}

.small {
  font-size: 1em;
  padding: 1em;
}

.large {
  font-size: 2em;
  padding: 1em;
}
```

1. `small: 16px`, `large: 16px`
2. `small: 32px`, `large: 32px`
3. `small: 16px`, `large: 32px`
4. `small: 32px`, `large: 16px`

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 3**

  `em` — это относительная единица измерения:
  - `font-size` у элемента зависит от значения `font-size` родителя.
  - Все остальные значения свойств элемента зависят от своего `font-size`.

</p>
</details>

---

##### 18. Какое значение свойства `font-size` будет у элемента `li`?

```html
<ul>
  <ul>
    <ul>
      <ul>
        <li>Example element</li>
      </ul>
    </ul>
  </ul>
</ul>
```

```css
html {
  font-size: 32px;
}

ul {
  font-size: 0.5em;
}
```

1. `16px`
2. `8px`
3. `4px`
4. `2px`

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 4**

  `em` — это относительная единица измерения, свойство `font-size` которой зависит от значения `font-size` у родительского элемента.

</p>
</details>

