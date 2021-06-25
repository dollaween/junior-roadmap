<div align="center">

# Задачи по созданию UI-компонентов

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

##### 1. Создайте и стилизуйте компонент Input

- При наведении на элемент рамка должна менять цвет.
- В состоянии фокуса рамка должна быть черной.

![image](https://user-images.githubusercontent.com/48933270/123074398-eb331400-d41f-11eb-9846-438b07a09996.png)

Макет: [Figma](https://www.figma.com/file/PnnS2RDlKkxS20vZGoKTRy/Tasks?node-id=188%3A1)

<details><summary><b>Решение</b></summary>
<p>

```html
<input class="input" type="text" placeholder="Enter your login..">
```

```css
.input {
  width: 240px;
  font-size: 14px;
  padding: 8px 10px;
  border-radius: 4px;
  border: 1px solid #bfbfbf;
  cursor: pointer;
  outline: none;
}

.input:hover,
.input:focus {
  border-color: #000;
}

.input::placeholder {
  color: #bfbfbf;
}
```

</p>
</details>

---

##### 2. Создайте и стилизуйте компонент Input

- При наведении на элемент рамка должна менять цвет.
- При наведении на крестик — рамка и крестик должны быть черного цвета.
- В состоянии фокуса рамка, поясняющий текст и крестик должны быть черного цвета.
- При нажатии на крестик ничего происходить не должно (очищение поля делается через Javascript).

![image](https://user-images.githubusercontent.com/48933270/123079444-a067cb00-d424-11eb-9abd-302ee765ad35.png)

Макет: [Figma](https://www.figma.com/file/PnnS2RDlKkxS20vZGoKTRy/Tasks?node-id=188%3A2)

<details><summary><b>Решение</b></summary>
<p>

```html
<label class="input">
  <p class="input__label">Optional label</p>
  <div class="input__container">
    <input class="input__field" type="text" placeholder="Enter your login..">
    <svg class="input__clear-button" viewBox="0 0 20 20">
      <path d="M5.34119 4.57509C5.12965 4.36356 4.78669 4.36356 4.57515 4.57509C4.36362 4.78663 4.36362 5.12959 4.57515 5.34113L9.234 9.99997L4.65887 14.5751C4.44734 14.7866 4.44734 15.1296 4.65887 15.3411C4.87041 15.5527 5.21337 15.5527 5.42491 15.3411L10 10.766L14.5752 15.3411C14.7867 15.5527 15.1297 15.5527 15.3412 15.3411C15.5527 15.1296 15.5527 14.7866 15.3412 14.5751L10.7661 9.99997L15.4249 5.34113C15.6364 5.12959 15.6364 4.78663 15.4249 4.57509C15.2134 4.36356 14.8704 4.36356 14.6589 4.57509L10 9.23394L5.34119 4.57509Z" />
    </svg>
  </div>
</label>

```

```css
.input {
  cursor: pointer;
}

.input:focus-within .input__label {
  color: #000;
}

.input:focus-within .input__clear-button {
  fill: #000;
}

.input__label,
.input__field {
  font-size: 14px;
  line-height: 16px;
}

.input__label {
  margin-bottom: 4px;
  color: #bfbfbf;
}

.input__container {
  width: 240px;
  display: flex;
  align-items: center;
  padding: 4px 10px;
  box-sizing: border-box;
  border: 1px solid #bfbfbf;
  border-radius: 4px;
}

.input__container:hover,
.input__container:focus-within {
  border-color: #000;
}

.input__field {
  flex-grow: 1;
  padding: 0;
  border: none;
  outline: none;
  cursor: pointer;
}

.input__field::placeholder {
  color: #bfbfbf;
}

.input__clear-button {
  width: 24px;
  height: 24px;
  fill: #bfbfbf;
}

.input__clear-button:hover {
  fill: #000;
}
```

</p>
</details>

---

##### 3. Создайте и стилизуйте компонент Dropdown

Механизм работы Dropdown:
- При наведении мышкой на текст "Hover me" — должно открываться выпадающее меню.
- Внутри выпадающего меню может находиться все что угодно (для примера показан список элементов).

![image](https://user-images.githubusercontent.com/48933270/123455872-dfe01400-d5ea-11eb-90c9-22d3d231c874.png)

Макет: [Figma](https://www.figma.com/file/PnnS2RDlKkxS20vZGoKTRy/Tasks?node-id=188%3A3)

<details><summary><b>Решение</b></summary>
<p>

```html
<div class="dropdown">
  <div class="dropdown__trigger">
    <span>Hover me</span>
    <svg width="20" height="20" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
      <path d="M5.11972 8.56009C5.11972 8.38009 5.18972 8.21009 5.32972 8.08009C5.59972 7.84009 6.00972 7.86009 6.24972 8.12009L11.99 14.4892L17.54 8.08006C17.78 7.81006 18.19 7.80006 18.46 8.04006C18.72 8.28006 18.74 8.69006 18.5 8.96006L12.51 15.8592C12.23 16.1692 11.75 16.1692 11.47 15.8592L5.28972 9.00009C5.16972 8.87009 5.11972 8.72009 5.11972 8.56009Z" fill="black"/>
    </svg>
  </div>
  <div class="dropdown__menu">
    <ul class="dropdown__list">
      <li class="dropdown__item">Element 1</li>
      <li class="dropdown__item">Element 2</li>
      <li class="dropdown__item">Element 3</li>
      <li class="dropdown__item">Element 4</li>
    </ul>
  </div>
</div>
```

```css
body {
  font-family: Arial, sans-serif;
  font-size: 14px;
  line-height: 20px;
}

.dropdown {
  position: relative;
}

.dropdown:hover .dropdown__menu {
  opacity: 1;
  pointer-events: auto;
}

.dropdown__trigger {
  display: flex;
  cursor: default;
}

.dropdown__menu {
  position: absolute;
  top: 100%;
  left: 0;
  width: 150px;
  padding: 10px;
  border-radius: 4px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, .2);
  opacity: 0;
  pointer-events: none;
}

.dropdown__item {
  margin-bottom: 4px;
}

.dropdown__item:last-child {
  margin-bottom: 0;
}
```

</p>
</details>

---

##### 4. Создайте и стилизуйте компонент Checkbox

- При нажатии на чекбокс он должен переходить из выключенного состояния во включенное, и наоборот.
- При наведении на чекбокс или текст — чекбокс должен подсвечиваться серым цветом.
- Если текст не влезает в одну строку — он должен переноситься на вторую.

![image](https://user-images.githubusercontent.com/48933270/123470786-8a613280-d5fd-11eb-9db8-94ce1ff8a3f1.png)

Макет: [Figma](https://www.figma.com/file/PnnS2RDlKkxS20vZGoKTRy/Tasks?node-id=188%3A4)

<details><summary><b>Решение</b></summary>
<p>

  Проблема стандартного чекбокса `<input type="checkbox">` в том, что он крайне ограничен в стилизации (например, ему нельзя задать значения `background-color` или `border`).

  Для обхода ограничений чекбокса, нам нужно создать его заменитель и работать с ним. В качестве заменителя в примере создан элемент `.checkbox__icon-box`. Его мы и будем стилизовать отталкиваясь от псевдокласса `:checked` оригинального чекбокса.

```html
<label class="checkbox">
  <input class="checkbox__input" type="checkbox">
  <span class="checkbox__icon-box">
    <svg class="checkbox__icon" viewBox="3 3 18 18">
      <path d="M10.2118 15.7333C10.6014 16.0996 11.2413 16.0865 11.617 15.7071L17.766 9.4281C18.0999 9.0749 18.0721 8.53857 17.7104 8.22462C17.3487 7.91067 16.7644 7.92375 16.4305 8.27694L10.8796 13.9542L7.54075 10.8147C7.19295 10.4877 6.60865 10.4877 6.26085 10.8147C5.91305 11.1417 5.91305 11.6912 6.26085 12.0182L10.2118 15.7333Z"/>
    </svg>
  </span>
  <span class="checkbox__text">Example text</span>
</label>
```

```css
.checkbox {
  position: relative;
  display: inline-flex;
  align-items: center;
  cursor: pointer;
}

.checkbox:hover .checkbox__icon-box {
  background: #d9d9d9;
}

.checkbox__input {
  position: absolute;
  width: 0;
  height: 0;
  margin: 0;
  visibility: hidden;
  pointer-events: none;
}

.checkbox__input:checked + .checkbox__icon-box {
  background: #fa8c16;
  border-color: #fa8c16;
}
.checkbox__input:checked + .checkbox__icon-box .checkbox__icon {
  fill: white;
}

.checkbox__icon-box {
  width: 14px;
  height: 14px;
  display: flex;
  align-items: center;
  flex-shrink: 0;
  border: 1px solid #000;
  border-radius: 2px;
}

.checkbox__icon {
  width: 14px;
  height: 14px;
  fill: transparent;
}

.checkbox__text {
  margin-left: 4px;
}
```

</p>
</details>

---

##### 5. Создайте и стилизуйте компонент Radio

- При нажатии на радио-кнопку она должна переходить во включенное состояние (при всех последующих нажатиях радио-кнопка все равно должна оставаться во включенном состоянии до тех пор, пока не будет выбрана другая радио-кнопка в группе).
- При наведении на радио-кнопку или текст — радио-кнопка должна подсвечиваться серым цветом.
- Если текст не влезает в одну строку — он должен переноситься на вторую.

![image](https://user-images.githubusercontent.com/48933270/123470690-70bfeb00-d5fd-11eb-9898-5a416332f273.png)

Макет: [Figma](https://www.figma.com/file/PnnS2RDlKkxS20vZGoKTRy/Tasks?node-id=188%3A5)

<details><summary><b>Решение</b></summary>
<p>
  
  Проблемы стандартных радио-кнопок `<input type="radio">` те же, что и у стандартных чекбоксов — ограниченная стилизация. И решение этой проблемы аналогичное — добавление заменителя (в примере это `.radio__icon-box`).

```html
<label class="radio">
  <input class="radio__input" type="radio">
  <span class="radio__icon-box"></span>
  <span class="radio__text">Example text</span>
</label>
```

```css
.radio {
  position: relative;
  display: inline-flex;
  align-items: center;
  cursor: pointer;
}

.radio:hover .radio__icon-box {
  background: #d9d9d9;
}

.radio__input {
  position: absolute;
  width: 0;
  height: 0;
  margin: 0;
  visibility: hidden;
  pointer-events: none;
}

.radio__input:checked + .radio__icon-box {
  border-color: #fa8c16;
  background: white;
}

.radio__input:checked + .radio__icon-box:after {
  background: #fa8c16;
}

.radio__icon-box {
  position: relative;
  width: 16px;
  height: 16px;
  display: flex;
  align-items: center;
  flex-shrink: 0;
  box-sizing: border-box;
  border: 1px solid #000;
  border-radius: 50%;
}

.radio__icon-box:after {
  position: absolute;
  content: '';
  width: 10px;
  height: 10px;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
  background: transparent;
  border-radius: 50%;
}

.radio__text {
  margin-left: 4px;
}
```

</p>
</details>

---

##### 6. Создайте и стилизуйте компонент Link

- При наведении на ссылку — должно появляться нижнее подчеркивание.
- Ссылка может быть как с иконкой, так и без нее. При наведении — иконка не должна подчеркиваться.

![image](https://user-images.githubusercontent.com/48933270/123479611-db772380-d609-11eb-8320-9639a64790de.png)

Макет: [Figma](https://www.figma.com/file/PnnS2RDlKkxS20vZGoKTRy/Tasks?node-id=188%3A6)

<details><summary><b>Решение</b></summary>
<p>

  Пользовательское подчеркивание можно добавить через `border-bottom`. Важно отметить, что корректно переноситься на несколько строк может только `display: inline` элемент (`inline-block` может быть перенесен только целиком).

  Элемент `.link__text` специально обернут в элемент `.link__text-wrapper`, потому что дочерние элементы флексбокса не могут быть `inline`, а для реализации подчеркивания нам нужен именно `inline` элемент.
  
```html
<a class="link" href="#">
  <span class="link__text-wrapper">
    <span class="link__text">Example text</span>
  </span>
  <svg class="link__icon" viewBox="0 0 24 24">
    <path d="M11.02 18.1482C11.15 18.2882 11.32 18.3582 11.5 18.3582C11.66 18.3582 11.81 18.3082 11.94 18.1882L17.98 12.6982C18.29 12.4182 18.29 11.9382 17.98 11.6582L11.94 6.16817C11.67 5.92817 11.26 5.94817 11.02 6.20817C10.78 6.47817 10.79 6.88817 11.06 7.12817L15.8956 11.5282H5C4.64101 11.5282 4.35 11.8192 4.35 12.1782C4.35 12.5372 4.64101 12.8282 5 12.8282H15.8956L11.06 17.2282C10.8 17.4682 10.78 17.8782 11.02 18.1482Z" />
  </svg>
</a>
```

```css
.link {
  display: inline-flex;
  align-items: center;
  color: #1890ff;
  text-decoration: none;
}

.link:hover {
  color: #096dd9;
}

.link:hover .link__text {
  border-color: #0050b3;
}

.link:hover .link__icon {
  fill: #0050b3;
}

.link__text {
  border-bottom: 1px solid transparent;
}

.link__icon {
  width: 20px;
  height: 20px;
  flex-shrink: 0;
  fill: #1890ff;
  margin-left: 4px;
}
```

</p>
</details>

---

##### 7. Создайте и стилизуйте компонент Pagination

- При наведении на пункт пагинации — он должен быть подсвечен серым цветом.
- Активный пункт пагинации должен иметь оранжевый цвет. При наведении на активный пункт — его цвет меняться не должен.
- Переключение по страницам реализовывать не нужно.

![image](https://user-images.githubusercontent.com/48933270/123482475-e7fd7b00-d60d-11eb-86dc-d1d7bf31b657.png)

Макет: [Figma](https://www.figma.com/file/PnnS2RDlKkxS20vZGoKTRy/Tasks?node-id=188%3A7)

<details><summary><b>Решение</b></summary>
<p>

```html
<ul class="pagination">
  <li class="pagination__item">
    <a class="pagination__link" href="#">
      <svg class="pagination__arrow-icon pagination__arrow-icon_left" viewBox="0 0 20 20">
        <path d="M4.26644 7.13341C4.26644 6.98341 4.32477 6.84175 4.44143 6.73341C4.66644 6.53341 5.0081 6.55008 5.2081 6.76675L9.99168 12.0744L14.6167 6.73339C14.8167 6.50839 15.1584 6.50006 15.3834 6.70006C15.6 6.90006 15.6167 7.24172 15.4167 7.46672L10.425 13.216C10.1917 13.4744 9.79168 13.4744 9.55835 13.216L4.4081 7.50008C4.3081 7.39174 4.26644 7.26674 4.26644 7.13341Z" />
      </svg>
    </a>
  </li>
  <li class="pagination__item">
    <a class="pagination__link" href="#">1</a>
  </li>
  <li class="pagination__item">
    <a class="pagination__link" href="#">...</a>
  </li>
  <li class="pagination__item">
    <a class="pagination__link" href="#">7</a>
  </li>
  <li class="pagination__item">
    <a class="pagination__link" href="#">8</a>
  </li>
  <li class="pagination__item pagination__item_active">
    <a class="pagination__link" href="#">9</a>
  </li>
  <li class="pagination__item">
    <a class="pagination__link" href="#">10</a>
  </li>
  <li class="pagination__item">
    <a class="pagination__link" href="#">11</a>
  </li>
  <li class="pagination__item">
    <a class="pagination__link" href="#">...</a>
  </li>
  <li class="pagination__item">
    <a class="pagination__link" href="#">24</a>
  </li>
  <li class="pagination__item">
    <a class="pagination__link" href="#">
      <svg class="pagination__arrow-icon pagination__arrow-icon_right" viewBox="0 0 20 20">
        <path d="M4.26644 7.13341C4.26644 6.98341 4.32477 6.84175 4.44143 6.73341C4.66644 6.53341 5.0081 6.55008 5.2081 6.76675L9.99168 12.0744L14.6167 6.73339C14.8167 6.50839 15.1584 6.50006 15.3834 6.70006C15.6 6.90006 15.6167 7.24172 15.4167 7.46672L10.425 13.216C10.1917 13.4744 9.79168 13.4744 9.55835 13.216L4.4081 7.50008C4.3081 7.39174 4.26644 7.26674 4.26644 7.13341Z" />
      </svg>
    </a>
  </li>
</ul>
```

```css
.pagination {
  display: flex;
}

.pagination__item {
  width: 40px;
  height: 40px;
  flex-shrink: 0;
  border-radius: 4px;
}

.pagination__item:hover:not(.pagination__item_active) {
  background: #d9d9d9;
}

.pagination__item_active {
  background: #fa8c16;
  color: white;
}

.pagination__link {
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  color: inherit;
  text-decoration: none;
}

.pagination__arrow-icon {
  width: 20px;
  height: 20px;
}

.pagination__arrow-icon_left {
  transform: rotate(90deg);
}

.pagination__arrow-icon_right {
  transform: rotate(-90deg);
}
```

</p>
</details>

---

##### 8. Создайте и стилизуйте компонент Switch

- При наведении на круг или текст цвет круга должен меняться.
- При нажатии круг должен плавно перемещаться вправо, а цвет должен меняться на оранжевый.

![image](https://user-images.githubusercontent.com/48933270/123488133-f9e41b80-d617-11eb-956a-85787d3f3379.png)

Макет: [Figma](https://www.figma.com/file/PnnS2RDlKkxS20vZGoKTRy/Tasks?node-id=188%3A8)

<details><summary><b>Решение</b></summary>
<p>

  В качестве основы нам отлично подойдет логика работы `<input type="checkbox">`, только заменитель оформляем в форме Switch.
  
```html
<label class="switch">
  <input class="switch__input" type="checkbox">
  <span class="switch__icon-box"></span>
  <span class="switch__text">Example text</span>
</label>
```

```css
.switch {
  position: relative;
  display: inline-flex;
  align-items: center;
  cursor: pointer;
}

.switch:hover .switch__icon-box::after {
  background: #d9d9d9;
}

.switch__input {
  position: absolute;
  width: 0;
  height: 0;
  margin: 0;
  visibility: hidden;
  pointer-events: none;
}

.switch__input:checked + .switch__icon-box {
  background: #fa8c16;
}

.switch__input:checked + .switch__icon-box::after {
  transform: translateX(12px);
}

.switch__icon-box {
  position: relative;
  width: 28px;
  height: 16px;
  display: flex;
  align-items: center;
  flex-shrink: 0;
  background: #000;
  border-radius: 8px;
  transition: .2s;
}

.switch__icon-box::after {
  content: '';
  position: absolute;
  width: 12px;
  height: 12px;
  left: 2px;
  border-radius: 50%;
  background: white;
  transition: .2s;
}

.switch__text {
  margin-left: 4px;
}
```

</p>
</details>

---

##### 9. Создайте и стилизуйте компонент Table

- Каждый нечетный ряд должен иметь серый фон.
- При наведении на ряд — он должен менять фон на серый.
- Первый и последний столбцы должны занимать минимальное возможное пространство.
- Последний столбец должен быть выравнен по правому краю.

![image](https://user-images.githubusercontent.com/48933270/123490370-927c9a80-d61c-11eb-9d50-9ffe19f5f341.png)

Макет: [Figma](https://www.figma.com/file/PnnS2RDlKkxS20vZGoKTRy/Tasks?node-id=188%3A9)

<details><summary><b>Решение</b></summary>
<p>

```html
<table>
  <thead>
    <tr>
      <td>ID</td>
      <td>Title</td>
      <td>Date</td>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>1</td>
      <td>Terminator</td>
      <td>26.10.1984</td>
    </tr>
    <tr>
      <td>2</td>
      <td>Robocop</td>
      <td>17.07.1987</td>
    </tr>
    <tr>
      <td>3</td>
      <td>Back to the Future</td>
      <td>03.07.1985</td>
    </tr>
    <tr>
      <td>4</td>
      <td>Gremlins</td>
      <td>08.06.1984</td>
    </tr>
  </tbody>
</table>
```

```css
table {
  width: 400px;
}

thead {
  font-weight: bold;
}

thead tr {
  background: #f0f0f0;
}

tr:nth-child(even) {
  background: #f0f0f0;
}

tr:hover {
  background: #d9d9d9;
}

td {
  padding: 4px 8px;
  border: 1px solid #f0f0f0;
}

td:first-child,
td:last-child {
  width: 1%;
}

td:last-child {
  text-align: right;
}
```

</p>
</details>



