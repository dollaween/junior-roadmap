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

> Во всех решениях перед стилями подключен файл [`reset.css`](https://meyerweb.com/eric/tools/css/reset/).  
> Вы можете использовать [`normalize.css`](https://necolas.github.io/normalize.css/) или не использовать сброс стилей вовсе. В таком случае решения могут немного отличаться.

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
<ul>
  <li>
    <svg viewBox="0 0 20 20">
      <path d="M5.34119 4.57509C5.12965 4.36356 4.78669 4.36356 4.57515 4.57509C4.36362 4.78663 4.36362 5.12959 4.57515 5.34113L9.234 9.99997L4.65887 14.5751C4.44734 14.7866 4.44734 15.1296 4.65887 15.3411C4.87041 15.5527 5.21337 15.5527 5.42491 15.3411L10 10.766L14.5752 15.3411C14.7867 15.5527 15.1297 15.5527 15.3412 15.3411C15.5527 15.1296 15.5527 14.7866 15.3412 14.5751L10.7661 9.99997L15.4249 5.34113C15.6364 5.12959 15.6364 4.78663 15.4249 4.57509C15.2134 4.36356 14.8704 4.36356 14.6589 4.57509L10 9.23394L5.34119 4.57509Z" />
    </svg>
    <span>Home</span>
  </li>
  <li>
    <svg viewBox="0 0 20 20">
      <path d="M5.34119 4.57509C5.12965 4.36356 4.78669 4.36356 4.57515 4.57509C4.36362 4.78663 4.36362 5.12959 4.57515 5.34113L9.234 9.99997L4.65887 14.5751C4.44734 14.7866 4.44734 15.1296 4.65887 15.3411C4.87041 15.5527 5.21337 15.5527 5.42491 15.3411L10 10.766L14.5752 15.3411C14.7867 15.5527 15.1297 15.5527 15.3412 15.3411C15.5527 15.1296 15.5527 14.7866 15.3412 14.5751L10.7661 9.99997L15.4249 5.34113C15.6364 5.12959 15.6364 4.78663 15.4249 4.57509C15.2134 4.36356 14.8704 4.36356 14.6589 4.57509L10 9.23394L5.34119 4.57509Z" />
    </svg>
    <span>About</span>
  </li>
  <li>
    <svg viewBox="0 0 20 20">
      <path d="M5.34119 4.57509C5.12965 4.36356 4.78669 4.36356 4.57515 4.57509C4.36362 4.78663 4.36362 5.12959 4.57515 5.34113L9.234 9.99997L4.65887 14.5751C4.44734 14.7866 4.44734 15.1296 4.65887 15.3411C4.87041 15.5527 5.21337 15.5527 5.42491 15.3411L10 10.766L14.5752 15.3411C14.7867 15.5527 15.1297 15.5527 15.3412 15.3411C15.5527 15.1296 15.5527 14.7866 15.3412 14.5751L10.7661 9.99997L15.4249 5.34113C15.6364 5.12959 15.6364 4.78663 15.4249 4.57509C15.2134 4.36356 14.8704 4.36356 14.6589 4.57509L10 9.23394L5.34119 4.57509Z" />
    </svg>
    <span>Contacts</span>
  </li>
</ul>
```

```css
body {
  font-family: Arial, sans-serif;
  font-size: 14px;
  line-height: 20px;
}

ul {
  width: max-content;
  margin: 30px auto;
  padding: 0;
}

li {
  display: inline-block;
  margin-right: 40px;
}

li:last-child {
  margin-right: 0;
}

svg {
  width: 20px;
  height: 20px;
  vertical-align: bottom;
  margin-right: 6px;
}
```

</p>
</details>


<details><summary><b>Решение Flexbox</b></summary>
<p>

```html
<ul>
  <li>
    <svg viewBox="0 0 20 20">
      <path d="M5.34119 4.57509C5.12965 4.36356 4.78669 4.36356 4.57515 4.57509C4.36362 4.78663 4.36362 5.12959 4.57515 5.34113L9.234 9.99997L4.65887 14.5751C4.44734 14.7866 4.44734 15.1296 4.65887 15.3411C4.87041 15.5527 5.21337 15.5527 5.42491 15.3411L10 10.766L14.5752 15.3411C14.7867 15.5527 15.1297 15.5527 15.3412 15.3411C15.5527 15.1296 15.5527 14.7866 15.3412 14.5751L10.7661 9.99997L15.4249 5.34113C15.6364 5.12959 15.6364 4.78663 15.4249 4.57509C15.2134 4.36356 14.8704 4.36356 14.6589 4.57509L10 9.23394L5.34119 4.57509Z" />
    </svg>
    <span>Home</span>
  </li>
  <li>
    <svg viewBox="0 0 20 20">
      <path d="M5.34119 4.57509C5.12965 4.36356 4.78669 4.36356 4.57515 4.57509C4.36362 4.78663 4.36362 5.12959 4.57515 5.34113L9.234 9.99997L4.65887 14.5751C4.44734 14.7866 4.44734 15.1296 4.65887 15.3411C4.87041 15.5527 5.21337 15.5527 5.42491 15.3411L10 10.766L14.5752 15.3411C14.7867 15.5527 15.1297 15.5527 15.3412 15.3411C15.5527 15.1296 15.5527 14.7866 15.3412 14.5751L10.7661 9.99997L15.4249 5.34113C15.6364 5.12959 15.6364 4.78663 15.4249 4.57509C15.2134 4.36356 14.8704 4.36356 14.6589 4.57509L10 9.23394L5.34119 4.57509Z" />
    </svg>
    <span>About</span>
  </li>
  <li>
    <svg viewBox="0 0 20 20">
      <path d="M5.34119 4.57509C5.12965 4.36356 4.78669 4.36356 4.57515 4.57509C4.36362 4.78663 4.36362 5.12959 4.57515 5.34113L9.234 9.99997L4.65887 14.5751C4.44734 14.7866 4.44734 15.1296 4.65887 15.3411C4.87041 15.5527 5.21337 15.5527 5.42491 15.3411L10 10.766L14.5752 15.3411C14.7867 15.5527 15.1297 15.5527 15.3412 15.3411C15.5527 15.1296 15.5527 14.7866 15.3412 14.5751L10.7661 9.99997L15.4249 5.34113C15.6364 5.12959 15.6364 4.78663 15.4249 4.57509C15.2134 4.36356 14.8704 4.36356 14.6589 4.57509L10 9.23394L5.34119 4.57509Z" />
    </svg>
    <span>Contacts</span>
  </li>
</ul>
```

```css
body {
  font-family: Arial, sans-serif;
  font-size: 14px;
  line-height: 20px;
}

ul {
  display: flex;
  width: max-content;
  margin: 30px auto;
  padding: 0;
  gap: 40px;
}

li {
  display: flex;
  align-items: center;
}

svg {
  width: 20px;
  height: 20px;
  margin-right: 8px;
}
```

</p>
</details>

---

##### 4. Расположите элементы так, как показано на скриншоте

![image](https://user-images.githubusercontent.com/48933270/122694203-51177400-d245-11eb-841d-858128c2491b.png)

Макет: [Figma](https://www.figma.com/file/PnnS2RDlKkxS20vZGoKTRy/Tasks?node-id=2%3A8)

<details><summary><b>Решение Flow</b></summary>
<p>

```html
<ul>
  <li>
    <svg viewBox="0 0 20 20">
      <path d="M5.34119 4.57509C5.12965 4.36356 4.78669 4.36356 4.57515 4.57509C4.36362 4.78663 4.36362 5.12959 4.57515 5.34113L9.234 9.99997L4.65887 14.5751C4.44734 14.7866 4.44734 15.1296 4.65887 15.3411C4.87041 15.5527 5.21337 15.5527 5.42491 15.3411L10 10.766L14.5752 15.3411C14.7867 15.5527 15.1297 15.5527 15.3412 15.3411C15.5527 15.1296 15.5527 14.7866 15.3412 14.5751L10.7661 9.99997L15.4249 5.34113C15.6364 5.12959 15.6364 4.78663 15.4249 4.57509C15.2134 4.36356 14.8704 4.36356 14.6589 4.57509L10 9.23394L5.34119 4.57509Z" />
    </svg>
    <p>Home</p>
  </li>
  <li>
    <svg viewBox="0 0 20 20">
      <path d="M5.34119 4.57509C5.12965 4.36356 4.78669 4.36356 4.57515 4.57509C4.36362 4.78663 4.36362 5.12959 4.57515 5.34113L9.234 9.99997L4.65887 14.5751C4.44734 14.7866 4.44734 15.1296 4.65887 15.3411C4.87041 15.5527 5.21337 15.5527 5.42491 15.3411L10 10.766L14.5752 15.3411C14.7867 15.5527 15.1297 15.5527 15.3412 15.3411C15.5527 15.1296 15.5527 14.7866 15.3412 14.5751L10.7661 9.99997L15.4249 5.34113C15.6364 5.12959 15.6364 4.78663 15.4249 4.57509C15.2134 4.36356 14.8704 4.36356 14.6589 4.57509L10 9.23394L5.34119 4.57509Z" />
    </svg>
    <p>About</p>
  </li>
  <li>
    <svg viewBox="0 0 20 20">
      <path d="M5.34119 4.57509C5.12965 4.36356 4.78669 4.36356 4.57515 4.57509C4.36362 4.78663 4.36362 5.12959 4.57515 5.34113L9.234 9.99997L4.65887 14.5751C4.44734 14.7866 4.44734 15.1296 4.65887 15.3411C4.87041 15.5527 5.21337 15.5527 5.42491 15.3411L10 10.766L14.5752 15.3411C14.7867 15.5527 15.1297 15.5527 15.3412 15.3411C15.5527 15.1296 15.5527 14.7866 15.3412 14.5751L10.7661 9.99997L15.4249 5.34113C15.6364 5.12959 15.6364 4.78663 15.4249 4.57509C15.2134 4.36356 14.8704 4.36356 14.6589 4.57509L10 9.23394L5.34119 4.57509Z" />
    </svg>
    <p>Contacts</p>
  </li>
</ul>
```

```css
body {
  font-family: Arial, sans-serif;
  font-size: 14px;
  line-height: 20px;
}

ul {
  width: max-content;
  margin: 30px auto;
  padding: 0;
}

li {
  display: inline-block;
  margin-right: 40px;
  text-align: center;
}

li:last-child {
  margin-right: 0;
}

svg {
  width: 20px;
  height: 20px;
}

p {
  margin: 0;
}
```

</p>
</details>

<details><summary><b>Решение Flexbox</b></summary>
<p>

```html
<ul>
  <li>
    <svg viewBox="0 0 20 20">
      <path d="M5.34119 4.57509C5.12965 4.36356 4.78669 4.36356 4.57515 4.57509C4.36362 4.78663 4.36362 5.12959 4.57515 5.34113L9.234 9.99997L4.65887 14.5751C4.44734 14.7866 4.44734 15.1296 4.65887 15.3411C4.87041 15.5527 5.21337 15.5527 5.42491 15.3411L10 10.766L14.5752 15.3411C14.7867 15.5527 15.1297 15.5527 15.3412 15.3411C15.5527 15.1296 15.5527 14.7866 15.3412 14.5751L10.7661 9.99997L15.4249 5.34113C15.6364 5.12959 15.6364 4.78663 15.4249 4.57509C15.2134 4.36356 14.8704 4.36356 14.6589 4.57509L10 9.23394L5.34119 4.57509Z" />
    </svg>
    <p>Home</p>
  </li>
  <li>
    <svg viewBox="0 0 20 20">
      <path d="M5.34119 4.57509C5.12965 4.36356 4.78669 4.36356 4.57515 4.57509C4.36362 4.78663 4.36362 5.12959 4.57515 5.34113L9.234 9.99997L4.65887 14.5751C4.44734 14.7866 4.44734 15.1296 4.65887 15.3411C4.87041 15.5527 5.21337 15.5527 5.42491 15.3411L10 10.766L14.5752 15.3411C14.7867 15.5527 15.1297 15.5527 15.3412 15.3411C15.5527 15.1296 15.5527 14.7866 15.3412 14.5751L10.7661 9.99997L15.4249 5.34113C15.6364 5.12959 15.6364 4.78663 15.4249 4.57509C15.2134 4.36356 14.8704 4.36356 14.6589 4.57509L10 9.23394L5.34119 4.57509Z" />
    </svg>
    <p>About</p>
  </li>
  <li>
    <svg viewBox="0 0 20 20">
      <path d="M5.34119 4.57509C5.12965 4.36356 4.78669 4.36356 4.57515 4.57509C4.36362 4.78663 4.36362 5.12959 4.57515 5.34113L9.234 9.99997L4.65887 14.5751C4.44734 14.7866 4.44734 15.1296 4.65887 15.3411C4.87041 15.5527 5.21337 15.5527 5.42491 15.3411L10 10.766L14.5752 15.3411C14.7867 15.5527 15.1297 15.5527 15.3412 15.3411C15.5527 15.1296 15.5527 14.7866 15.3412 14.5751L10.7661 9.99997L15.4249 5.34113C15.6364 5.12959 15.6364 4.78663 15.4249 4.57509C15.2134 4.36356 14.8704 4.36356 14.6589 4.57509L10 9.23394L5.34119 4.57509Z" />
    </svg>
    <p>Contacts</p>
  </li>
</ul>
```

```css
body {
  font-family: Arial, sans-serif;
  font-size: 14px;
  line-height: 20px;
}

ul {
  display: flex;
  width: max-content;
  margin: 30px auto;
  padding: 0;
  gap: 40px;
}

li {
  display: flex;
  align-items: center;
  flex-direction: column;
}

svg {
  width: 20px;
  height: 20px;
}

p {
  margin: 0;
}
```

</p>
</details>

---

##### 5. Расположите элементы так, как показано на скриншоте

![image](https://user-images.githubusercontent.com/48933270/122694484-237efa80-d246-11eb-870c-1fb6a942e562.png)

Макет: [Figma](https://www.figma.com/file/PnnS2RDlKkxS20vZGoKTRy/Tasks?node-id=2%3A9)

<details><summary><b>Решение Flow</b></summary>
<p>

```html
<div class="delivery">
  <svg class="delivery__icon" viewBox="0 0 20 20">
    <path d="M5.34119 4.57509C5.12965 4.36356 4.78669 4.36356 4.57515 4.57509C4.36362 4.78663 4.36362 5.12959 4.57515 5.34113L9.234 9.99997L4.65887 14.5751C4.44734 14.7866 4.44734 15.1296 4.65887 15.3411C4.87041 15.5527 5.21337 15.5527 5.42491 15.3411L10 10.766L14.5752 15.3411C14.7867 15.5527 15.1297 15.5527 15.3412 15.3411C15.5527 15.1296 15.5527 14.7866 15.3412 14.5751L10.7661 9.99997L15.4249 5.34113C15.6364 5.12959 15.6364 4.78663 15.4249 4.57509C15.2134 4.36356 14.8704 4.36356 14.6589 4.57509L10 9.23394L5.34119 4.57509Z" />
  </svg>
  <div class="delivery__text">
    <p class="delivery__description">Deliver to</p>
    <p class="delivery__country">Russian Federation</p>
  </div>
</div>
```

```css
body {
  font-family: Arial, sans-serif;
  font-size: 14px;
  line-height: 20px;
}

.delivery {
  width: max-content;
  margin: 30px auto;
}

.delivery__icon {
  width: 24px;
  height: 24px;
  vertical-align: 2px;
}

.delivery__text {
  display: inline-block;
  margin-left: 8px;
}

.delivery__description,
.delivery__country {
  margin: 0;
}

.delivery__country {
  font-size: 16px;
}
```

</p>
</details>

<details><summary><b>Решение Flexbox</b></summary>
<p>

```html
<div class="delivery">
  <svg class="delivery__icon" viewBox="0 0 20 20">
    <path d="M5.34119 4.57509C5.12965 4.36356 4.78669 4.36356 4.57515 4.57509C4.36362 4.78663 4.36362 5.12959 4.57515 5.34113L9.234 9.99997L4.65887 14.5751C4.44734 14.7866 4.44734 15.1296 4.65887 15.3411C4.87041 15.5527 5.21337 15.5527 5.42491 15.3411L10 10.766L14.5752 15.3411C14.7867 15.5527 15.1297 15.5527 15.3412 15.3411C15.5527 15.1296 15.5527 14.7866 15.3412 14.5751L10.7661 9.99997L15.4249 5.34113C15.6364 5.12959 15.6364 4.78663 15.4249 4.57509C15.2134 4.36356 14.8704 4.36356 14.6589 4.57509L10 9.23394L5.34119 4.57509Z" />
  </svg>
  <div class="delivery__text">
    <p class="delivery__description">Deliver to</p>
    <p class="delivery__country">Russian Federation</p>
  </div>
</div>
```

```css
body {
  font-family: Arial, sans-serif;
  font-size: 14px;
  line-height: 20px;
}

.delivery {
  width: max-content;
  margin: 30px auto;
  display: flex;
  align-items: center;
}

.delivery__icon {
  width: 24px;
  height: 24px;
  vertical-align: 2px;
}

.delivery__text {
  margin-left: 10px;
}

.delivery__description,
.delivery__country {
  margin: 0;
}

.delivery__country {
  font-size: 16px;
}
```

</p>
</details>

---

##### 6. Расположите элементы так, как показано на скриншоте

![image](https://user-images.githubusercontent.com/48933270/122694894-8de46a80-d247-11eb-890b-8dafc8e740e6.png)

Макет: [Figma](https://www.figma.com/file/PnnS2RDlKkxS20vZGoKTRy/Tasks?node-id=2%3A10)

<details><summary><b>Решение Flow</b></summary>
<p>

```html
<div class="menu">
  <div class="menu__item">
    <p>
      <span>Hello, Sign in</span>
      <svg class="menu__icon" viewBox="0 0 20 20">
        <path d="M5.34119 4.57509C5.12965 4.36356 4.78669 4.36356 4.57515 4.57509C4.36362 4.78663 4.36362 5.12959 4.57515 5.34113L9.234 9.99997L4.65887 14.5751C4.44734 14.7866 4.44734 15.1296 4.65887 15.3411C4.87041 15.5527 5.21337 15.5527 5.42491 15.3411L10 10.766L14.5752 15.3411C14.7867 15.5527 15.1297 15.5527 15.3412 15.3411C15.5527 15.1296 15.5527 14.7866 15.3412 14.5751L10.7661 9.99997L15.4249 5.34113C15.6364 5.12959 15.6364 4.78663 15.4249 4.57509C15.2134 4.36356 14.8704 4.36356 14.6589 4.57509L10 9.23394L5.34119 4.57509Z" />
      </svg>
    </p>
    <p>
      <span class="menu__text_big">Accounts & Lists</span>
      <svg class="menu__icon" viewBox="0 0 20 20">
        <path d="M5.34119 4.57509C5.12965 4.36356 4.78669 4.36356 4.57515 4.57509C4.36362 4.78663 4.36362 5.12959 4.57515 5.34113L9.234 9.99997L4.65887 14.5751C4.44734 14.7866 4.44734 15.1296 4.65887 15.3411C4.87041 15.5527 5.21337 15.5527 5.42491 15.3411L10 10.766L14.5752 15.3411C14.7867 15.5527 15.1297 15.5527 15.3412 15.3411C15.5527 15.1296 15.5527 14.7866 15.3412 14.5751L10.7661 9.99997L15.4249 5.34113C15.6364 5.12959 15.6364 4.78663 15.4249 4.57509C15.2134 4.36356 14.8704 4.36356 14.6589 4.57509L10 9.23394L5.34119 4.57509Z" />
      </svg>
    </p>
  </div>

  <div class="menu__item">
    <p>Returns</p>
    <p>
      <span class="menu__text_big">& Orders</span>
      <svg class="menu__icon" viewBox="0 0 20 20">
        <path d="M5.34119 4.57509C5.12965 4.36356 4.78669 4.36356 4.57515 4.57509C4.36362 4.78663 4.36362 5.12959 4.57515 5.34113L9.234 9.99997L4.65887 14.5751C4.44734 14.7866 4.44734 15.1296 4.65887 15.3411C4.87041 15.5527 5.21337 15.5527 5.42491 15.3411L10 10.766L14.5752 15.3411C14.7867 15.5527 15.1297 15.5527 15.3412 15.3411C15.5527 15.1296 15.5527 14.7866 15.3412 14.5751L10.7661 9.99997L15.4249 5.34113C15.6364 5.12959 15.6364 4.78663 15.4249 4.57509C15.2134 4.36356 14.8704 4.36356 14.6589 4.57509L10 9.23394L5.34119 4.57509Z" />
      </svg>
    </p>
  </div>
</div>
```

```css
body {
  font-family: Arial, sans-serif;
  font-size: 14px;
  line-height: 20px;
}

p {
  margin: 0;
}

.menu {
  width: max-content;
  margin: 30px auto;
}

.menu__item {
  display: inline-block;
  margin-right: 40px;
}

.menu__item:last-child {
  margin-right: 0;
}

.menu__icon {
  width: 20px;
  height: 20px;
  vertical-align: bottom;
  margin-left: 1px;
}

.menu__text_big {
  font-size: 16px;
}
```

</p>
</details>

<details><summary><b>Решение Flexbox</b></summary>
<p>

```html
<div class="menu">
  <div class="menu__item">
    <p>
      <span>Hello, Sign in</span>
      <svg class="menu__icon" viewBox="0 0 20 20">
        <path d="M5.34119 4.57509C5.12965 4.36356 4.78669 4.36356 4.57515 4.57509C4.36362 4.78663 4.36362 5.12959 4.57515 5.34113L9.234 9.99997L4.65887 14.5751C4.44734 14.7866 4.44734 15.1296 4.65887 15.3411C4.87041 15.5527 5.21337 15.5527 5.42491 15.3411L10 10.766L14.5752 15.3411C14.7867 15.5527 15.1297 15.5527 15.3412 15.3411C15.5527 15.1296 15.5527 14.7866 15.3412 14.5751L10.7661 9.99997L15.4249 5.34113C15.6364 5.12959 15.6364 4.78663 15.4249 4.57509C15.2134 4.36356 14.8704 4.36356 14.6589 4.57509L10 9.23394L5.34119 4.57509Z" />
      </svg>
    </p>
    <p>
      <span class="menu__text_big">Accounts & Lists</span>
      <svg class="menu__icon" viewBox="0 0 20 20">
        <path d="M5.34119 4.57509C5.12965 4.36356 4.78669 4.36356 4.57515 4.57509C4.36362 4.78663 4.36362 5.12959 4.57515 5.34113L9.234 9.99997L4.65887 14.5751C4.44734 14.7866 4.44734 15.1296 4.65887 15.3411C4.87041 15.5527 5.21337 15.5527 5.42491 15.3411L10 10.766L14.5752 15.3411C14.7867 15.5527 15.1297 15.5527 15.3412 15.3411C15.5527 15.1296 15.5527 14.7866 15.3412 14.5751L10.7661 9.99997L15.4249 5.34113C15.6364 5.12959 15.6364 4.78663 15.4249 4.57509C15.2134 4.36356 14.8704 4.36356 14.6589 4.57509L10 9.23394L5.34119 4.57509Z" />
      </svg>
    </p>
  </div>

  <div class="menu__item">
    <p>Returns</p>
    <p>
      <span class="menu__text_big">& Orders</span>
      <svg class="menu__icon" viewBox="0 0 20 20">
        <path d="M5.34119 4.57509C5.12965 4.36356 4.78669 4.36356 4.57515 4.57509C4.36362 4.78663 4.36362 5.12959 4.57515 5.34113L9.234 9.99997L4.65887 14.5751C4.44734 14.7866 4.44734 15.1296 4.65887 15.3411C4.87041 15.5527 5.21337 15.5527 5.42491 15.3411L10 10.766L14.5752 15.3411C14.7867 15.5527 15.1297 15.5527 15.3412 15.3411C15.5527 15.1296 15.5527 14.7866 15.3412 14.5751L10.7661 9.99997L15.4249 5.34113C15.6364 5.12959 15.6364 4.78663 15.4249 4.57509C15.2134 4.36356 14.8704 4.36356 14.6589 4.57509L10 9.23394L5.34119 4.57509Z" />
      </svg>
    </p>
  </div>
</div>
```

```css
body {
  font-family: Arial, sans-serif;
  font-size: 14px;
  line-height: 20px;
}

p {
  margin: 0;
}

.menu {
  width: max-content;
  margin: 30px auto;
  display: flex;
  gap: 40px;
}

.menu__item:last-child {
  margin-right: 0;
}

.menu__icon {
  width: 20px;
  height: 20px;
  vertical-align: bottom;
  margin-left: 1px;
}

.menu__text_big {
  font-size: 16px;
}
```

</p>
</details>

---

##### 7. Расположите элементы так, как показано на скриншоте

![image](https://user-images.githubusercontent.com/48933270/122695538-4e1e8280-d249-11eb-82d0-7c4b8c0c51c2.png)

Макет: [Figma](https://www.figma.com/file/PnnS2RDlKkxS20vZGoKTRy/Tasks?node-id=2%3A11)

<details><summary><b>Решение Flexbox</b></summary>
<p>

```html
<div class="menu">
  <svg class="menu__icon" viewBox="0 0 20 20">
    <path d="M5.34119 4.57509C5.12965 4.36356 4.78669 4.36356 4.57515 4.57509C4.36362 4.78663 4.36362 5.12959 4.57515 5.34113L9.234 9.99997L4.65887 14.5751C4.44734 14.7866 4.44734 15.1296 4.65887 15.3411C4.87041 15.5527 5.21337 15.5527 5.42491 15.3411L10 10.766L14.5752 15.3411C14.7867 15.5527 15.1297 15.5527 15.3412 15.3411C15.5527 15.1296 15.5527 14.7866 15.3412 14.5751L10.7661 9.99997L15.4249 5.34113C15.6364 5.12959 15.6364 4.78663 15.4249 4.57509C15.2134 4.36356 14.8704 4.36356 14.6589 4.57509L10 9.23394L5.34119 4.57509Z" />
  </svg>

  <ul class="menu__nav">
    <li>Home</li>
    <li>About</li>
    <li>Contacts</li>
    <li>Service</li>
  </ul>

  <ul class="menu__profile">
    <li class="menu__profile-item">
      <svg class="menu__icon" viewBox="0 0 20 20">
        <path d="M5.34119 4.57509C5.12965 4.36356 4.78669 4.36356 4.57515 4.57509C4.36362 4.78663 4.36362 5.12959 4.57515 5.34113L9.234 9.99997L4.65887 14.5751C4.44734 14.7866 4.44734 15.1296 4.65887 15.3411C4.87041 15.5527 5.21337 15.5527 5.42491 15.3411L10 10.766L14.5752 15.3411C14.7867 15.5527 15.1297 15.5527 15.3412 15.3411C15.5527 15.1296 15.5527 14.7866 15.3412 14.5751L10.7661 9.99997L15.4249 5.34113C15.6364 5.12959 15.6364 4.78663 15.4249 4.57509C15.2134 4.36356 14.8704 4.36356 14.6589 4.57509L10 9.23394L5.34119 4.57509Z" />
      </svg>
      <span>Exit</span>
    </li>
  </ul>
</div>
```

```css
body {
  font-family: Arial, sans-serif;
  font-size: 14px;
  line-height: 20px;
}

ul {
  margin: 0;
  padding: 0;
}

li {
  list-style: none;
}

.menu {
  width: 600px;
  display: flex;
  margin: 30px auto;
}

.menu__icon {
  width: 20px;
  height: 20px;
}

.menu__nav {
  display: flex;
  gap: 20px;
  margin-left: 40px;
}

.menu__profile {
  margin-left: auto;
}

.menu__profile-item {
  display: flex;
  align-items: center;
}

.menu__profile-item .menu__icon {
  margin-right: 4px;
}
```

</p>
</details>

---

##### 8. Расположите элементы так, как показано на скриншоте

![image](https://user-images.githubusercontent.com/48933270/122696521-ea498900-d24b-11eb-8000-1b7c09aa29da.png)

Макет: [Figma](https://www.figma.com/file/PnnS2RDlKkxS20vZGoKTRy/Tasks?node-id=2%3A12)

<details><summary><b>Решение Flow</b></summary>
<p>

```html
<div class="menu">
  <div class="menu__col">
    <h5 class="menu__title">Get to Know Us</h5>
    <ul class="menu__list">
      <li class="menu__list-item">Careers</li>
      <li class="menu__list-item">Blog</li>
      <li class="menu__list-item">About</li>
      <li class="menu__list-item">Investor</li>
    </ul>
  </div>
  <div class="menu__col">
    <h5 class="menu__title">Let Us Help You</h5>
    <ul class="menu__list">
      <li class="menu__list-item">Your Account</li>
      <li class="menu__list-item">Your Orders</li>
      <li class="menu__list-item">Shipping Rates & Policies</li>
      <li class="menu__list-item">Help</li>
    </ul>
  </div>
</div>
```

```css
body, h5 {
  font-family: Arial, sans-serif;
  font-size: 14px;
  line-height: 20px;
}

h5, ul {
  margin: 0;
  padding: 0;
}

li {
  list-style: none;
}

.menu {
  width: max-content;
  margin: 30px auto;
}

.menu__col {
  margin-right: 90px;
  display: inline-block;
  width: 110px;
  vertical-align: top;
}

.menu__col:last-child {
  margin-right: 0;
}

.menu__list {
  margin-top: 10px;
}

.menu__list-item {
  margin-top: 4px;
}
```

</p>
</details>

<details><summary><b>Решение Flexbox</b></summary>
<p>

```html
<div class="menu">
  <div class="menu__col">
    <h5 class="menu__title">Get to Know Us</h5>
    <ul class="menu__list">
      <li class="menu__list-item">Careers</li>
      <li class="menu__list-item">Blog</li>
      <li class="menu__list-item">About</li>
      <li class="menu__list-item">Investor</li>
    </ul>
  </div>
  <div class="menu__col">
    <h5 class="menu__title">Let Us Help You</h5>
    <ul class="menu__list">
      <li class="menu__list-item">Your Account</li>
      <li class="menu__list-item">Your Orders</li>
      <li class="menu__list-item">Shipping Rates & Policies</li>
      <li class="menu__list-item">Help</li>
    </ul>
  </div>
</div>
```

```css
body, h5 {
  font-family: Arial, sans-serif;
  font-size: 14px;
  line-height: 20px;
}

h5, ul {
  margin: 0;
  padding: 0;
}

li {
  list-style: none;
}

.menu {
  width: max-content;
  margin: 30px auto;
  display: flex;
  gap: 90px;
}

.menu__col {
  width: 110px;
  display: flex;
  flex-direction: column;
}

.menu__list {
  margin-top: 10px;
}

.menu__list-item {
  margin-top: 4px;
}

.menu__list-item:first-child {
  margin-top: 0;
}
```

</p>
</details>

---

##### 9. Расположите элементы так, как показано на скриншоте

![image](https://user-images.githubusercontent.com/48933270/122789251-c7f15300-d2bf-11eb-98a6-30ff2a83c9fd.png)

Макет: [Figma](https://www.figma.com/file/PnnS2RDlKkxS20vZGoKTRy/Tasks?node-id=2%3A13)

<details><summary><b>Решение Flexbox</b></summary>
<p>

```html
<div class="card">
  <div class="card__col">
    <p class="card__price">50 000 ₽</p>
    <p class="card__description">Lorem ipsum dolor sit amet, consectetur adipisicing elit.</p>
    <p class="card__seller">Bill Gates</p>
  </div>
  <div class="card__col">
    <button class="card__button">Buy</button>
  </div>
</div>
```

```css
body {
  font-family: Arial, sans-serif;
  font-size: 14px;
  line-height: 20px;
}

p {
  margin: 0;
}

.card {
  width: max-content;
  margin: 30px auto;
  display: flex;
  gap: 20px;
}

.card__col:first-child {
  width: 170px;
}

.card__price {
  font-size: 16px;
  line-height: 24px;
  font-weight: bold;
}

.card__description {
  margin-top: 4px;
}

.card__seller {
  font-weight: bold;
  margin-top: 4px;
}

.card__button {
  background: #df2f2f;
  padding: 4px 10px;
  border-radius: 4px;
  border: none;
  color: white;
  line-height: 20px;
}
```

</p>
</details>

---

##### 10. Расположите элементы так, как показано на скриншоте

![image](https://user-images.githubusercontent.com/48933270/122791608-0d168480-d2c2-11eb-9656-f496de7de2d3.png)

Макет: [Figma](https://www.figma.com/file/PnnS2RDlKkxS20vZGoKTRy/Tasks?node-id=152%3A137)

<details><summary><b>Решение Flexbox</b></summary>
<p>

```html
<div class="card">
  <div class="card__header">
    <svg class="card__icon" viewBox="0 0 20 20">
      <path d="M5.34119 4.57509C5.12965 4.36356 4.78669 4.36356 4.57515 4.57509C4.36362 4.78663 4.36362 5.12959 4.57515 5.34113L9.234 9.99997L4.65887 14.5751C4.44734 14.7866 4.44734 15.1296 4.65887 15.3411C4.87041 15.5527 5.21337 15.5527 5.42491 15.3411L10 10.766L14.5752 15.3411C14.7867 15.5527 15.1297 15.5527 15.3412 15.3411C15.5527 15.1296 15.5527 14.7866 15.3412 14.5751L10.7661 9.99997L15.4249 5.34113C15.6364 5.12959 15.6364 4.78663 15.4249 4.57509C15.2134 4.36356 14.8704 4.36356 14.6589 4.57509L10 9.23394L5.34119 4.57509Z" />
    </svg>
    <p class="card__title">Lorem ipsum dolor sit amet, consectetur adipisicing elit.</p>
  </div>
  <p class="card__description">Lorem ipsum dolor sit amet, consectetur adipisicing elit.</p>
  <div class="card__buttons">
    <svg class="card__icon" viewBox="0 0 20 20">
      <path d="M5.34119 4.57509C5.12965 4.36356 4.78669 4.36356 4.57515 4.57509C4.36362 4.78663 4.36362 5.12959 4.57515 5.34113L9.234 9.99997L4.65887 14.5751C4.44734 14.7866 4.44734 15.1296 4.65887 15.3411C4.87041 15.5527 5.21337 15.5527 5.42491 15.3411L10 10.766L14.5752 15.3411C14.7867 15.5527 15.1297 15.5527 15.3412 15.3411C15.5527 15.1296 15.5527 14.7866 15.3412 14.5751L10.7661 9.99997L15.4249 5.34113C15.6364 5.12959 15.6364 4.78663 15.4249 4.57509C15.2134 4.36356 14.8704 4.36356 14.6589 4.57509L10 9.23394L5.34119 4.57509Z" />
    </svg>
    <svg class="card__icon" viewBox="0 0 20 20">
      <path d="M5.34119 4.57509C5.12965 4.36356 4.78669 4.36356 4.57515 4.57509C4.36362 4.78663 4.36362 5.12959 4.57515 5.34113L9.234 9.99997L4.65887 14.5751C4.44734 14.7866 4.44734 15.1296 4.65887 15.3411C4.87041 15.5527 5.21337 15.5527 5.42491 15.3411L10 10.766L14.5752 15.3411C14.7867 15.5527 15.1297 15.5527 15.3412 15.3411C15.5527 15.1296 15.5527 14.7866 15.3412 14.5751L10.7661 9.99997L15.4249 5.34113C15.6364 5.12959 15.6364 4.78663 15.4249 4.57509C15.2134 4.36356 14.8704 4.36356 14.6589 4.57509L10 9.23394L5.34119 4.57509Z" />
    </svg>
    <svg class="card__icon" viewBox="0 0 20 20">
      <path d="M5.34119 4.57509C5.12965 4.36356 4.78669 4.36356 4.57515 4.57509C4.36362 4.78663 4.36362 5.12959 4.57515 5.34113L9.234 9.99997L4.65887 14.5751C4.44734 14.7866 4.44734 15.1296 4.65887 15.3411C4.87041 15.5527 5.21337 15.5527 5.42491 15.3411L10 10.766L14.5752 15.3411C14.7867 15.5527 15.1297 15.5527 15.3412 15.3411C15.5527 15.1296 15.5527 14.7866 15.3412 14.5751L10.7661 9.99997L15.4249 5.34113C15.6364 5.12959 15.6364 4.78663 15.4249 4.57509C15.2134 4.36356 14.8704 4.36356 14.6589 4.57509L10 9.23394L5.34119 4.57509Z" />
    </svg>
  </div>
</div>
```

```css
body {
  font-family: Arial, sans-serif;
  font-size: 14px;
  line-height: 20px;
}

p {
  margin: 0;
}

.card {
  width: 252px;
  margin: 30px auto;
}

.card__icon {
  width: 24px;
  height: 24px;
}

.card__header {
  display: flex;
  align-items: center;
}

.card__title {
  margin-left: 8px;
}

.card__header .card__icon {
  flex-shrink: 0;
}

.card__description {
  font-size: 12px;
  line-height: 16px;
  margin-top: 10px;
}

.card__buttons {
  margin-top: 10px;
}

.card__buttons .card__icon {
  margin-right: 8px;
}
.card__buttons .card__icon:last-child {
  margin-right: 0;
}
```

</p>
</details>

---

##### 11. Расположите элементы так, как показано на скриншоте

![image](https://user-images.githubusercontent.com/48933270/122801659-13f6c480-d2cd-11eb-819f-643961b06099.png)

Макет: [Figma](https://www.figma.com/file/PnnS2RDlKkxS20vZGoKTRy/Tasks?node-id=2%3A16)

<details><summary><b>Решение</b></summary>
<p>

```html
<div class="card">
  <div class="card__col">
    <img class="card__image" src="https://picsum.photos/102" alt="card-image">
    <p class="card__title">Good name</p>
  </div>
  <div class="card__col">
    <p class="card__description">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Atque dolore ducimus esse et eveniet explicabo facilis?</p>
    <div class="card__seller-info">
      <svg class="card__icon" viewBox="0 0 20 20">
        <path d="M5.34119 4.57509C5.12965 4.36356 4.78669 4.36356 4.57515 4.57509C4.36362 4.78663 4.36362 5.12959 4.57515 5.34113L9.234 9.99997L4.65887 14.5751C4.44734 14.7866 4.44734 15.1296 4.65887 15.3411C4.87041 15.5527 5.21337 15.5527 5.42491 15.3411L10 10.766L14.5752 15.3411C14.7867 15.5527 15.1297 15.5527 15.3412 15.3411C15.5527 15.1296 15.5527 14.7866 15.3412 14.5751L10.7661 9.99997L15.4249 5.34113C15.6364 5.12959 15.6364 4.78663 15.4249 4.57509C15.2134 4.36356 14.8704 4.36356 14.6589 4.57509L10 9.23394L5.34119 4.57509Z" />
      </svg>
      <div class="card__seller">
        <p class="card__seller-name">Bill Gates</p>
        <p class="card__seller-company">Microsoft</p>
      </div>
    </div>
  </div>
</div>
```

```css
body {
  font-family: Arial, sans-serif;
  font-size: 14px;
  line-height: 18px;
}

p {
  margin: 0;
}

.card {
  width: max-content;
  margin: 30px auto;
  display: flex;
  gap: 15px;
}

.card__col:first-child {
  width: 100px;
}

.card__image {
  width: 100%;
  height: 102px;
}

.card__title {
  margin-top: 4px;
  text-align: center;
}

.card__col:last-child {
  width: 265px;
}

.card__description {
  font-size: 16px;
  line-height: 20px;
}

.card__seller-info {
  margin-top: 8px;
  display: flex;
  align-items: center;
}

.card__icon {
  width: 24px;
  height: 24px;
}

.card__seller {
  margin-left: 8px;
}

.card__seller-name {
  font-weight: bold;
}
```

</p>
</details>


---

##### 12. Расположите элементы так, как показано на скриншоте

![image](https://user-images.githubusercontent.com/48933270/122800287-6afb9a00-d2cb-11eb-9ced-a99ed5658555.png)

Макет: [Figma](https://www.figma.com/file/PnnS2RDlKkxS20vZGoKTRy/Tasks?node-id=2%3A15)

<details><summary><b>Решение</b></summary>
<p>

```html
<div class="messages">
  <span class="messages__text">Messages</span>
  <div class="messages__count">8</div>
</div>
```

```css
body {
  font-family: Arial, sans-serif;
  font-size: 14px;
  line-height: 20px;
}

.messages {
  width: max-content;
  margin: 30px auto;
  position: relative;
}

.messages__count {
  width: 12px;
  height: 12px;
  border-radius: 50%;
  position: absolute;
  right: -14px;
  top: 0;
  font-size: 8px;
  line-height: 13px;
  text-align: center;
  background: #f5222d;
  color: white;
}
```

</p>
</details>


