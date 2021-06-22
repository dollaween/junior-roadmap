<div align="center">

# Задачи на Flexbox

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

> Во всех решениях перед стилями подключен файл [`reset.css`](https://meyerweb.com/eric/tools/css/reset/).  
> Вы можете использовать [`normalize.css`](https://necolas.github.io/normalize.css/) или не использовать сброс стилей вовсе. В таком случае решения могут немного отличаться.

---

##### 1. Расположите элементы так, как показано на скриншоте

Каждый элемент должен занимать равную долю ширины родительского контейнера. Если элемента 2 — то каждый занимает по 50%, если элементов 4 — то каждый занимает по 25%, и так далее.

![image](https://user-images.githubusercontent.com/48933270/122962479-21c04e80-d38e-11eb-8cdb-450c695feda9.png)

Макет: [Figma](https://www.figma.com/file/PnnS2RDlKkxS20vZGoKTRy/Tasks?node-id=2%3A17)

<details><summary><b>Решение</b></summary>
<p>

```html
<div class="container">
  <div class="item"></div>
  <div class="item"></div>
  <div class="item"></div>
  <div class="item"></div>
</div>
```

```css
.container {
  display: flex;
}

.item {
  height: 120px;
  background: #69c0ff;
  border: 10px solid #1890ff;
  flex-grow: 1;
}
```

</p>
</details>

---

##### 2. Расположите элементы так, как показано на скриншоте

Условия:
- Ширина всех элементов — `100px`.
- Ширина последнего элемента — все оставшееся свободное пространство.

![image](https://user-images.githubusercontent.com/48933270/122962645-4d433900-d38e-11eb-9e14-50fea309fd73.png)

Макет: [Figma](https://www.figma.com/file/PnnS2RDlKkxS20vZGoKTRy/Tasks?node-id=2%3A18)

<details><summary><b>Решение</b></summary>
<p>

```html
<div class="container">
  <div class="item"></div>
  <div class="item"></div>
  <div class="item"></div>
  <div class="item"></div>
</div>
```

```css
.container {
  display: flex;
}

.item {
  width: 100px;
  height: 120px;
  background: #69c0ff;
  border: 10px solid #1890ff;
}

.item:last-child {
  flex-grow: 1;
  background: #ffc069;
  border-color: #fa8c16;
}
```

</p>
</details>

---

##### 3. Расположите элементы так, как показано на скриншоте

Условия:
- Центральный элемент должен быть в 2 раза больше остальных.

![image](https://user-images.githubusercontent.com/48933270/122963210-bd51bf00-d38e-11eb-895a-a73d7eb7e720.png)

Макет: [Figma](https://www.figma.com/file/PnnS2RDlKkxS20vZGoKTRy/Tasks?node-id=2%3A19)

<details><summary><b>Решение</b></summary>
<p>

```html
<div class="container">
  <div class="item"></div>
  <div class="item"></div>
  <div class="item"></div>
</div>
```

```css
.container {
  display: flex;
}

.item {
  height: 120px;
  background: #69c0ff;
  border: 10px solid #1890ff;
  flex-grow: 1;
}

.item:nth-child(2) {
  background: #ffc069;
  border-color: #fa8c16;
  flex-grow: 2;
}
```

</p>
</details>

---

##### 4. Расположите элементы так, как показано на скриншоте

Условия:
- Последний элемент должен быть прижат к правому краю родительского контейнера.

![image](https://user-images.githubusercontent.com/48933270/122963665-29ccbe00-d38f-11eb-95ce-a541b5e4a90d.png)

Макет: [Figma](https://www.figma.com/file/PnnS2RDlKkxS20vZGoKTRy/Tasks?node-id=2%3A20)

<details><summary><b>Решение</b></summary>
<p>

```html
<div class="container">
  <div class="item"></div>
  <div class="item"></div>
  <div class="item"></div>
  <div class="item"></div>
</div>
```

```css
.container {
  display: flex;
}

.item {
  width: 100px;
  height: 120px;
  background: #69c0ff;
  border: 10px solid #1890ff;
}

.item:last-child {
  background: #ffc069;
  border-color: #fa8c16;
  margin-left: auto;
}
```

</p>
</details>

---

##### 5. Расположите элементы так, как показано на скриншоте

- Второй и третий элементы должны быть прижаты к правому краю родительского контейнера.

![image](https://user-images.githubusercontent.com/48933270/122964551-0eae7e00-d390-11eb-8bf1-19be4720b871.png)

Макет: [Figma](https://www.figma.com/file/PnnS2RDlKkxS20vZGoKTRy/Tasks?node-id=2%3A22)

<details><summary><b>Решение</b></summary>
<p>

```html
<div class="container">
  <div class="item"></div>
  <div class="item"></div>
  <div class="item"></div>
  <div class="item"></div>
</div>
```

```css
.container {
  display: flex;
}

.item {
  width: 100px;
  height: 120px;
  background: #69c0ff;
  border: 10px solid #1890ff;
}

.item:nth-child(3),
.item:last-child {
  background: #ffc069;
  border-color: #fa8c16;
}

.item:nth-child(3) {
  margin-left: auto;
}
```

</p>
</details>

---

##### 6. Расположите элементы так, как показано на скриншоте

- Высота элементов должна равняться высоте содержимого контента.

![image](https://user-images.githubusercontent.com/48933270/122967861-9a75d980-d393-11eb-9d5f-2719a5a063f2.png)

Макет: [Figma](https://www.figma.com/file/PnnS2RDlKkxS20vZGoKTRy/Tasks?node-id=2%3A21)

<details><summary><b>Решение</b></summary>
<p>

```html
<div class="container">
  <div class="item">First item</div>
  <div class="item">Second item, which has 2 lines</div>
  <div class="item">Third item, which has exactly three lines</div>
  <div class="item">Last item, which can be more than one or two or three lines</div>
</div>
```

```css
body {
  font-family: Arial, sans-serif;
  font-size: 14px;
  line-height: 16px;
}

.container {
  display: flex;
  align-items: flex-start;
  width: 600px;
}

.item {
  width: 25%;
  padding: 10px;
  box-sizing: border-box;
  text-align: center;
  color: #fff;
  background: #69c0ff;
  border: 10px solid #1890ff;
}
```

</p>
</details>

---

##### 7. Расположите элементы так, как показано на скриншоте

![image](https://user-images.githubusercontent.com/48933270/122968049-cabd7800-d393-11eb-9292-d06b02ef310a.png)

Макет: [Figma](https://www.figma.com/file/PnnS2RDlKkxS20vZGoKTRy/Tasks?node-id=2%3A24)

<details><summary><b>Решение</b></summary>
<p>

```html
<div class="container">
  <div class="item">First item</div>
  <div class="item">Second item, which has 2 lines</div>
  <div class="item">Third item, which has exactly three lines</div>
  <div class="item">Last item, which can be more than one or two or three lines</div>
</div>
```

```css
body {
  font-family: Arial, sans-serif;
  font-size: 14px;
  line-height: 16px;
}

.container {
  display: flex;
  align-items: center;
  width: 600px;
}

.item {
  width: 25%;
  padding: 10px;
  box-sizing: border-box;
  text-align: center;
  color: #fff;
  background: #69c0ff;
  border: 10px solid #1890ff;
}
```

</p>
</details>

---

##### 8. Расположите элементы так, как показано на скриншоте

- Высота элементов должна равняться высоте содержимого контента.

![image](https://user-images.githubusercontent.com/48933270/122972667-0f97dd80-d399-11eb-831b-788003545318.png)

Макет: [Figma](https://www.figma.com/file/PnnS2RDlKkxS20vZGoKTRy/Tasks?node-id=2%3A23)

<details><summary><b>Решение</b></summary>
<p>

```html
<div class="container">
  <div class="item">Lorem ipsum</div>
  <div class="item">Lorem ipsum dolor sit amet, consectetur adipisicing elit</div>
  <div class="item">Lorem ipsum dolor sit amet, consectetur</div>
  <div class="item">Lorem ipsum dolor sit amet</div>
</div>
```

```css
body {
  font-family: Arial, sans-serif;
  font-size: 14px;
  line-height: 16px;
}

.container {
  width: 600px;
  display: flex;
  align-items: flex-start;
  flex-wrap: wrap;
  gap: 10px;
}

.item {
  width: calc(50% - 5px);
  padding: 10px;
  box-sizing: border-box;
  text-align: center;
  color: #fff;
  background: #69c0ff;
  border: 10px solid #1890ff;
}
```

</p>
</details>

---

##### 9. Расположите элементы так, как показано на скриншоте

- Высота элементов должна равняться высоте самого высокого элемента в строке.

![image](https://user-images.githubusercontent.com/48933270/122972968-630a2b80-d399-11eb-9f85-55fe8e769b4b.png)

Макет: [Figma](https://www.figma.com/file/PnnS2RDlKkxS20vZGoKTRy/Tasks?node-id=2%3A25)

<details><summary><b>Решение</b></summary>
<p>

```html
<div class="container">
  <div class="item">Lorem ipsum</div>
  <div class="item">Lorem ipsum dolor sit amet, consectetur adipisicing elit</div>
  <div class="item">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ad, aspernatur delectus distinctio dolore dolorem</div>
  <div class="item">Lorem ipsum dolor sit amet</div>
</div>
```

```css
body {
  font-family: Arial, sans-serif;
  font-size: 14px;
  line-height: 16px;
}

.container {
  display: flex;
  width: 600px;
  align-items: stretch;
  flex-wrap: wrap;
  gap: 10px;
}

.item {
  width: calc(50% - 5px);
  padding: 10px;
  box-sizing: border-box;
  text-align: center;
  color: #fff;
  background: #69c0ff;
  border: 10px solid #1890ff;
}
```

</p>
</details>

---

##### 10. Расположите элементы так, как показано на скриншоте

- Высота элементов должна равняться высоте самого высокого элемента в строке.
- Элемент `button` должен быть прижат к нижней части родительского контейнера.

![image](https://user-images.githubusercontent.com/48933270/122980989-f5aec880-d3a1-11eb-870e-3bb6ac50a9c8.png)

Макет: [Figma](https://www.figma.com/file/PnnS2RDlKkxS20vZGoKTRy/Tasks?node-id=2%3A25)

<details><summary><b>Решение</b></summary>
<p>

```html
<div class="container">
  <div class="item">
    <span>Lorem ipsum</span>
    <button>Button</button>
  </div>
  <div class="item">
    <span>Lorem ipsum dolor sit amet, consectetur adipisicing elit</span>
    <button>Button</button>
  </div>
  <div class="item">
    <span>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Cumque doloribus facilis molestiae odio.</span>
    <button>Button</button>
  </div>
</div>
```

```css
body {
  font-family: Arial, sans-serif;
  font-size: 14px;
  line-height: 16px;
}

.container {
  display: flex;
  width: 600px;
  align-items: stretch;
  justify-content: space-between;
}

.item {
  width: calc(33.33% - 15px);
  display: flex;
  flex-direction: column;
  padding: 10px;
  box-sizing: border-box;
  text-align: center;
  color: #fff;
  background: #69c0ff;
  border: 10px solid #1890ff;
}

span {
  margin-bottom: 10px;
}

button {
  width: 100%;
  margin-top: auto;
  padding: 7px 0;
  color: white;
  background: #ffc069;
  border: 4px solid #fa8c16;
}
```

</p>
</details>


