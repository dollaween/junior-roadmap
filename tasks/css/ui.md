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
- В состоянии фокуса рамка должна быть черной

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


