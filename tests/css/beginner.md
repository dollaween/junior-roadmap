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

---

##### 19. Какой будет цвет у первого элемента `li`?

```html
<ul>
  <li>Element 1<li>
  <li>Element 2<li>
  <li>Element 3<li>
  <li>Element 4<li>
</ul>
```

```css
li + li {
  color: orange;
}

li > li {
  color: yellow;
}

li ~ li {
  color: silver;
}
```

1. `orange`
2. `yellow`
3. `silver`
4. `black`

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 4**
  
  - **Комбинатор следующего соседнего элемента `+`** — выбирает элемент, который находится следующим на этом же уровне вложенности.
  - **Комбинатор дочерних элементов `>`** — выбирает элементы, которые являются непосредственно дочерними у указанного элемента.
  - **Комбинатор всех соседних элементов `~`** — выбирает все элементы, которые находятся на этом же уровне вложенности, после указанного элемента.

  Ни один из этих комбинаторов не затрагивает первый элемент `li`, поэтому его цвет будет установлен в значение по-умолчанию (`black`).

</p>
</details>

---

##### 20. Какого цвета будет элемент `button`?

```html
<button class="btn primary">Example button</button>
```

```css
.btn.primary {
  color: hotpink;
}

.btn .primary {
  color: gold;
}

button + .btn {
  color: cyan;
}

button > .primary {
  color: green;
}
```

1. `hotpink`
2. `gold`
3. `cyan`
4. `green`

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 1**

  Только селектор `.btn.primary` указывает на элемент `button`. Ни один из остальных селекторов не указывает на кнопку.

</p>
</details>

---

##### 21. К какой кнопке будут применены стили `.first.second`?

```html
<button class="first">Button 1</button>
<button class="second">Button 2</button>
<button class="first second">Button 3</button>
```

```css
.first.second {
  color: tomato;
}
```

1. К первой кнопке
2. Ко второй кнопке
3. К третьей кнопке
4. Ко всем кнопкам

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 3**

  **Комбинатор И (без символов между селекторами)** — выбирает элементы, у которых присутствуют одновременно все указанные селекторы.

</p>
</details>

---

##### 22. Какие итоговые размеры будут у элемента `div`?

```html
<div></div>
```

```css
div {
  width: 100px;
  height: 50px;
  padding: 20px;
  border: 5px solid tan;
  box-sizing: content-box;
}
```

1. `ширина: 100px`, `высота: 50px`
2. `ширина: 120px`, `высота: 70px`
3. `ширина: 140px`, `высота: 90px`
4. `ширина: 150px`, `высота: 100px`

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 4**
  
  Значение `content-box` означает, что к ширине и высоте элемента также будут добавлены размеры `padding` и `border`.
  
  Получается, что размеры контейнера будут высчитываться следующим образом:
  - `ширина =  width + padding-left + padding-right + border-left + border-right = 100 + 20 + 20 + 5 + 5 = 150px`
  - `высота = height + padding-top + padding-bottom + border-top + border-bottom = 50 + 20 + 20 + 5 + 5 = 100px`

</p>
</details>

---

##### 23. Какие итоговые размеры будут у элемента `div`?

```html
<div></div>
```

```css
div {
  width: 100px;
  height: 50px;
  padding: 20px;
  border: 5px solid tan;
  box-sizing: border-box;
}
```

1. `ширина: 100px`, `высота: 50px`
2. `ширина: 120px`, `высота: 70px`
3. `ширина: 140px`, `высота: 90px`
4. `ширина: 150px`, `высота: 100px`

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 1**
  
  Значение `border-box` означает, что внутренние отступы и рамка уже включены в заданные размеры элемента. В данном случае итоговая ширина элемента будет равна `width: 100px`, а высота — `height: 50px`.

</p>
</details>

---

##### 24. Какое расстояние будет между элементами `div`?

```html
<div class="first"></div>
<div class="second"></div>
```

```css
.first {
  margin-bottom: 40px;
}

.second {
  margin-top: 60px;
}
```

1. `40px`
2. `60px`
3. `100px`
4. `0px`

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 2**
  
  Вертикальный отступ между элементами не суммируется, а выбирается наибольшее из значений. Это называется схлопывание отступов (margin collapse).  
  В данном случае, наибольшее из значений — `60px`.

</p>
</details>

---

##### 25. Какое расстояние будет между элементами `span`?

```html
<p>
  <span class="first">Element 1</span>
  <span class="second">Element 2</span>
</p>
```

```css
.first {
  margin-right: 40px;
}

.second {
  margin-left: 60px;
}
```

1. `40px`
2. `60px`
3. `100px`
4. `0px`

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 3**

  Горизонтальный отступ между элементами суммируется. Расстояние будет равно `40px + 60px = 100px`.

</p>
</details>

---

##### 26. Какие итоговые размеры будут у элемента `span`?

```html
<span></span>
```

```css
span {
  width: 100px;
  height: 50px;
  box-sizing: border-box;
}
```

1. `ширина: 0px`, `высота: 0px`
2. `ширина: 100px`, `высота: 50px`
3. `ширина: 100px`, `высота: 55px`
4. `ширина: 0px`, `высота: 55px`

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 1**
  
  У `inline`-элементов свойства `width` и `height` работать не будут.

</p>
</details>

---

##### 27. Какая высота будет у элементов `span`?

```html
<span class="first">Element 1</span>
<span class="second">Element 2</span>
```

```css
.first,
.second {
  height: 16px;
  font-size: 20px;
  line-height: 0;
}

.first {
  font-family: Arial;
}

.second {
  font-family: Tahoma;
}
```

1. `20px` у обоих
2. `0px` у обоих
3. `16px` у обоих
4. У элементов высота будет отличаться

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 4**

  Свойство `height` — никак не влияет на `inline`-элемент.  
  Свойство `line-height` — влияет на межстрочное расстояние.
  
  На высоту самого `inline`-элемента влияют свойства `font-size` и `font-family`. Если с `font-size` все просто — сколько указали, столько и будет, то `font-family` может внести в высоту `inline`-элемента дополнительные пиксели. Разные шрифты добавляют разное количество доп. пикселей.

  В данном примере, высота будет следующая:
  - `.first — 22px`
  - `.second — 24px`

</p>
</details>

---

##### 28. Какое из следующих свойств выровняет последний элемент `li` по правому краю родительского контейнера?

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

##### 29. Какое свойство нужно применить к элементу `.second`, чтобы он занял все свободное пространство родительского контейнера, не изменяя размеры `.first`?

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

##### 30. Какие из стилей отцентрируют `.target` по горизонтали относительно родительского элемента?

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

