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


