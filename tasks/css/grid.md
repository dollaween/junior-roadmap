<div align="center">

# Задачи по Grid

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

![image](https://user-images.githubusercontent.com/48933270/123003527-fb190c80-d3bb-11eb-97b8-1200deffd590.png)

Макет: [Figma](https://www.figma.com/file/PnnS2RDlKkxS20vZGoKTRy/Tasks?node-id=2%3A28)

<details><summary><b>Решение</b></summary>
<p>

```html
<div class="container">
  <div class="item"></div>
  <div class="item"></div>
  <div class="item"></div>
  <div class="item"></div>
  <div class="item"></div>
  <div class="item"></div>
  <div class="item"></div>
  <div class="item"></div>
  <div class="item"></div>
</div>
```

```css
.container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 15px;
}

.item {
  height: 80px;
  box-sizing: border-box;
  background: #69c0ff;
  border: 10px solid #1890ff;
}
```

</p>
</details>

---

##### 2. Расположите элементы так, как показано на скриншоте

![image](https://user-images.githubusercontent.com/48933270/123004426-3ff17300-d3bd-11eb-8488-6b5625be9408.png)

Макет: [Figma](https://www.figma.com/file/PnnS2RDlKkxS20vZGoKTRy/Tasks?node-id=2%3A29)

<details><summary><b>Решение</b></summary>
<p>

```html
<div class="container">
  <header class="item header"></header>
  <aside class="item sidebar"></aside>
  <article class="item content"></article>
  <aside class="item ads"></aside>
  <footer class="item footer"></footer>
</div>
```

```css
.container {
  display: grid;
  grid-template-areas:
    "header header header"
    "sidebar content ads"
    "footer footer footer";
  gap: 15px;
}

.item {
  height: 80px;
  box-sizing: border-box;
  background: #69c0ff;
  border: 10px solid #1890ff;
}

.header {
  grid-area: header;
}
.sidebar {
  grid-area: sidebar;
}
.content {
  grid-area: content;
}
.ads {
  grid-area: ads;
}
.footer {
  grid-area: footer;
}
```

</p>
</details>

---

##### 3. Расположите элементы так, как показано на скриншоте

![image](https://user-images.githubusercontent.com/48933270/123006136-ec345900-d3bf-11eb-86d3-28f055aa1e89.png)

Макет: [Figma](https://www.figma.com/file/PnnS2RDlKkxS20vZGoKTRy/Tasks?node-id=2%3A30)

<details><summary><b>Решение</b></summary>
<p>

```html
<div class="container">
  <div class="item"></div>
  <div class="item"></div>
  <div class="item"></div>
  <div class="item"></div>
  <div class="item"></div>
  <div class="item"></div>
  <div class="item"></div>
  <div class="item"></div>
  <div class="item"></div>
  <div class="item"></div>
  <div class="item"></div>
  <div class="item"></div>
  <div class="item"></div>
</div>
```

```css
.container {
  display: grid;
  width: 600px;
  height: 248px;
  grid-template-areas:
    'a b c d'
    'l m m e'
    'k m m f'
    'j i h g';
  gap: 16px;
}

.item {
  box-sizing: border-box;
  background: #69c0ff;
  border: 10px solid #1890ff;
}

.item:nth-child(1) {
  grid-area: a;
}
.item:nth-child(2) {
  grid-area: b;
}
.item:nth-child(3) {
  grid-area: c;
}
.item:nth-child(4) {
  grid-area: d;
}
.item:nth-child(5) {
  grid-area: e;
}
.item:nth-child(6) {
  grid-area: f;
}
.item:nth-child(7) {
  grid-area: g;
}
.item:nth-child(8) {
  grid-area: h;
}
.item:nth-child(9) {
  grid-area: i;
}
.item:nth-child(10) {
  grid-area: j;
}
.item:nth-child(11) {
  grid-area: k;
}
.item:nth-child(12) {
  grid-area: l;
}
.item:last-child {
  grid-area: m;
}
```

</p>
</details>

