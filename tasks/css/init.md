<div align="center">

# Базовые задачи

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

##### 1. Расположите элементы так, как показано на скриншоте

![image](https://user-images.githubusercontent.com/48933270/122679095-3071fe80-d1f2-11eb-994d-b2c48dd95686.png)

Макет: [Figma](https://www.figma.com/file/PnnS2RDlKkxS20vZGoKTRy/Tasks?node-id=2%3A5)

<details><summary><b>Решение Flow</b></summary>
<p>

```html
<ul>
  <li>Home</li>
  <li>About</li>
  <li>Contacts</li>
  <li>Service</li>
  <li>FAQ</li>
</ul>
```

```css
ul {
  width: max-content;
  margin: 30px auto;
  padding: 0;
}

li {
  display: inline-block;
  margin-right: 25px;
}

li:last-child {
  margin-right: 0;
}
```

</p>
</details>

<details><summary><b>Решение Flexbox</b></summary>
<p>

```html
<ul>
  <li>Home</li>
  <li>About</li>
  <li>Contacts</li>
  <li>Service</li>
  <li>FAQ</li>
</ul>
```

```css
ul {
  display: flex;
  width: max-content;
  margin: 30px auto;
  padding: 0;
  gap: 25px;
}

li {
  list-style: none;
}
```

</p>
</details>

---

##### 2. Расположите элементы так, как показано на скриншоте

![image](https://user-images.githubusercontent.com/48933270/122679706-91023b00-d1f4-11eb-8947-b87a118799ee.png)

Макет: [Figma](https://www.figma.com/file/PnnS2RDlKkxS20vZGoKTRy/Tasks?node-id=2%3A6)


<details><summary><b>Решение Flow</b></summary>
<p>

В качестве точки-разделителя, использован символ шрифта `•`.

```html
<ul>
  <li>Home</li>
  <li>About</li>
  <li>Contacts</li>
  <li>Service</li>
  <li>FAQ</li>
</ul>
```

```css
ul {
  width: max-content;
  margin: 30px auto;
  padding: 0;
}

li {
  display: inline-block;
  margin-right: 40px;
  position: relative;
}

li::after {
  content: '•';
  position: absolute;
  color: #aaa;
  top: 0;
  right: -23px;
}

li:last-child {
  margin-right: 0;
}

li:last-child::after {
  display: none;
}
```

</p>
</details>

<details><summary><b>Решение Flexbox</b></summary>
<p>

В качестве точки-разделителя сделан псевдоэлемент с размерами и фоном.
  
```html
<ul>
  <li>Home</li>
  <li>About</li>
  <li>Contacts</li>
  <li>Service</li>
  <li>FAQ</li>
</ul>
```

```css
ul {
  display: flex;
  width: max-content;
  margin: 30px auto;
  padding: 0;
  gap: 40px;
}

li {
  list-style: none;
  position: relative;
}

li::after {
  content: '';
  position: absolute;
  width: 5px;
  height: 5px;
  background: #aaa;
  border-radius: 50%;
  top: 50%;
  right: -23px;
  transform: translateY(-50%);
}

li:last-child::after {
  display: none;
}
```

</p>
</details>

---

##### 3. Расположите элементы так, как показано на скриншоте

![image](https://user-images.githubusercontent.com/48933270/122681278-2523d080-d1fc-11eb-9849-ec7210136af7.png)

Макет: [Figma](https://www.figma.com/file/PnnS2RDlKkxS20vZGoKTRy/Tasks?node-id=2%3A7)

<details><summary><b>Решение Flow</b></summary>
<p>

```html

```

```css

```

</p>
</details>

<details><summary><b>Решение Flexbox</b></summary>
<p>

```html

```

```css

```

</p>
</details>




