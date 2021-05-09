<div align="center">

# Работа с DOM

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

##### 1. Калькулятор

Напишите программу, в которой будет два числовых поля ввода, четыре кнопки (`+`, `-`, `*`, `/`) и блок с выводом результата.  
После того, как мы ввели два числа и нажали на одну из кнопок — в блоке с выводом результата должен быть выведен результат сложения/вычитания/умножения/деления (в зависимости от того на какую кнопку нажали).

<img width="228" src="https://user-images.githubusercontent.com/48933270/117586529-64510300-b121-11eb-9d99-5b54447ed453.png">

<details><summary><b>Решение, HTML</b></summary>
<p>

```html
<div>
  <input type="number" id="input1" value="0">
  <input type="number" id="input2" value="0">
  <button id="buttonSum">+</button>
  <button id="buttonSub">-</button>
  <button id="buttonMult">*</button>
  <button id="buttonDiv">/</button>
  <div>Результат: <span id="output">0</span></div>
</div>
```

</p>
</details>

<details><summary><b>Решение, JS</b></summary>
<p>

```js
const input1 = document.getElementById('input1')
const input2 = document.getElementById('input2')
const buttonSum = document.getElementById('buttonSum')
const buttonSub = document.getElementById('buttonSub')
const buttonMult = document.getElementById('buttonMult')
const buttonDiv = document.getElementById('buttonDiv')
const output = document.getElementById('output')

function getInputNumbers() {
  const num1 = input1.valueAsNumber || 0
  const num2 = input2.valueAsNumber || 0
  return [num1, num2]
}

function sum() {
  const [num1, num2] = getInputNumbers()
  output.innerHTML = num1 + num2
}

function sub() {
  const [num1, num2] = getInputNumbers()
  output.innerHTML = num1 - num2
}

function mult() {
  const [num1, num2] = getInputNumbers()
  output.innerHTML = num1 * num2
}

function div() {
  const [num1, num2] = getInputNumbers()
  output.innerHTML = num1 / num2
}

buttonSum.addEventListener('click', sum)
buttonSub.addEventListener('click', sub)
buttonMult.addEventListener('click', mult)
buttonDiv.addEventListener('click', div)
```

</p>
</details>

---

##### 2. Конвертер валют

Напишите программу, в которой будет одно числовое поле ввода (означающее количество рублей) и три кнопки ("Конвертировать в доллары", "Конвертировать в евро", "Конвертировать в йены").  
После того, как мы ввели в поле ввода число и нажали на одну из кнопок, в блоке "Результат" должно отображаться сколько денег у нас в соответствующей валюте (с точностью до двух знаков после запятой).

<img width="225" src="https://user-images.githubusercontent.com/48933270/117587368-4934c200-b126-11eb-9613-984fb6249294.png">

<details><summary><b>Решение, HTML</b></summary>
<p>

```html
<input type="number" id="input" value="0">
<button id="buttonDol">Конвертировать в доллары</button>
<button id="buttonEur">Конверировать в евро</button>
<button id="buttonYen">Конвертировать в йены</button>
<div>Результат: <span id="output">0.00</span></div>
```

</p>
</details>

<details><summary><b>Решение, JS</b></summary>
<p>

```js
const input = document.getElementById('input')
const buttonDol = document.getElementById('buttonDol')
const buttonEur = document.getElementById('buttonEur')
const buttonYen = document.getElementById('buttonYen')
const output = document.getElementById('output')

function convertToDollar() {
  const dollar = 77
  const rubles = input.valueAsNumber || 0
  output.innerHTML = (rubles / dollar).toFixed(2)
}

function convertToEuro() {
  const euro = 90
  const rubles = input.valueAsNumber || 0
  output.innerHTML = (rubles / euro).toFixed(2)
}

function convertToYen() {
  const yen = 0.7
  const rubles = input.valueAsNumber || 0
  output.innerHTML = (rubles / yen).toFixed(2)
}

buttonDol.addEventListener('click', convertToDollar)
buttonEur.addEventListener('click', convertToEuro)
buttonYen.addEventListener('click', convertToYen)
```

</p>
</details>

---

##### 3. Форма авторизации

Напишите программу, в которой будет два текстовых поля ("Логин", "Пароль") и кнопка с надписью "Войти".  
По нажатию на кнопку "Войти", программа должна проверить два условия:
1. Логин равен "admin"
2. Пароль равен "12345"

Если оба условия верны, то под формой должна быть выведена надпись зеленого цвета "Вход разрешен". Если хотя бы одно из условий не выполняется — то под формой должна быть выведена надпись красного цвета "Неверный логин или пароль".

Начальное состояние:  
<img width="186" alt="Снимок экрана 2021-05-10 в 00 41 17" src="https://user-images.githubusercontent.com/48933270/117587846-931ea780-b128-11eb-8b86-2506852e3ee9.png">

Логин и пароль верны:  
<img width="186" alt="Снимок экрана 2021-05-10 в 00 42 06" src="https://user-images.githubusercontent.com/48933270/117587863-a29df080-b128-11eb-94ae-22a61601c18c.png">

Неверный логин или пароль:  
<img width="188" alt="Снимок экрана 2021-05-10 в 00 41 50" src="https://user-images.githubusercontent.com/48933270/117587868-acbfef00-b128-11eb-80fb-882d16ce1c82.png">


<details><summary><b>Решение, HTML</b></summary>
<p>

```html
<input type="text" id="login" placeholder="Введите логин">
<input type="password" id="password" placeholder="Введите пароль">
<button id="button">Войти</button>
<div id="output"></div>
```

</p>
</details>


<details><summary><b>Решение, JS</b></summary>
<p>

```js
const inputLogin = document.getElementById('login')
const inputPassword = document.getElementById('password')
const button = document.getElementById('button')
const output = document.getElementById('output')

const user = {
  login: 'admin',
  password: '12345'
}

function validate() {
  const login = inputLogin.value
  const password = inputPassword.value

  if (login === user.login && password === user.password) {
    output.style.color = 'green'
    output.innerHTML = 'Вход разрешен'
  } else {
    output.style.color = 'red'
    output.innerHTML = 'Неверный логин или пароль'
  }
}

button.addEventListener('click', validate)

```

</p>
</details>


