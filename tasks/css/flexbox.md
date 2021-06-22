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
  height: 150px;
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

Макет: [Figma]()

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
  height: 150px;
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



