<div align="center">

# `useCallback()`

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

Хук `useCallback(fn, deps)` — возвращает мемоизированный колбэк.

---

<div align="center">

### Проблема

</div>

---

Функции, которые написаны внутри компонента — создаются заново на каждый рендер.

В примере ниже, функция `handleClick` будет создана столько раз, сколько произойдет рендеров компонента `Cars`. В целом — это нормально, создание функций — достаточно дешевый процесс.

```js
export function Cars() {
  const handleClick = () => {}

  return <Car onClick={handleClick} />
}
```

Нюанс в следующем:

Постоянное пересоздание функции `handleClick` означает, что каждый раз ссылка на эту функцию будет меняться. Если ссылка постоянно меняется — значит компоненты, в которые мы передаем функцию, будут всегда перерисовываться на каждый рендер, даже если мы их обернем в `React.memo()`.

Функции обернутые в `useCallback` не пересоздаются на каждый рендер до тех пор, пока не поступят изменения в зависимости.

---

<div align="center">

### Когда использовать?

</div>

---

Хук `useCallback()` стоит использовать в следующих ситуациях:
1. Когда мы передаем функцию как `props` и при этом важно, чтобы дочерний компонент не перерисовывался.
2. Когда используем `React.memo()` на дочерних элементах.
3. Когда функция является зависимостью для других хуков (например, `useEffect()`)

---

<div align="center">

### Как использовать?

</div>

---

`useCallback(fn, deps)` принимает два параметра:
- `fn` — функция, которую нужно мемоизировать.
- `deps` — массив зависимостей. Если элементы этого массива меняются — функция пересоздается заново.

---

<div align="center">

### Пример

</div>

---

Идеальное место использования `useCallback()` — большие списки из 100+ элементов.

```js
import React, { useCallback } from 'react'

export function Articles(titles) {
  const handleClick = useCallback(() => {
    console.log('Clicked')
  }, [])

  return (
    <div>
      {titles.map((title) => (
        <Article onClick={handleClick} title={title} />
      ))}
    </div>
  )
}

export function Article({ onClick, title }) {
  return <div onClick={onClick}>{title}</div>
}
```

Благодаря `useCallback()` — все компоненты `Article` не будут перерисовываться лишний раз.

---

<div align="center">

### Плохой пример когда использовать `useCallback()` не нужно

</div>

---

В данном случае, компонент `Car` один и очень простой. Его перересовка стоит дешево и не создает проблемы для производительности.

А вот чрезмерная оптимизация через `useCallback()` увеличивает сложность кода и добавляет лишние проверки.

```js
export function Cars(data) {
  const handleClick = useCallback(() => {
    console.log('Clicked')
  }, [])

  return <Car onClick={handleClick} data={data} />
}

export function Car({ onClick, data }) {
  return <div onClick={onClick}>{data}</div>
}
```

---

<div align="center">

### Зависимости

</div>

---

Так как `useCallback()` создает мемоизированную функцию, то и внешние данные для неё обновляться не будут.

```js
export function Component() {
  const num = Math.random()

  const callback = useCallback(() => {
    // Здесь num — всегда будет одинаковым, сколько бы раз рендер компонента ни произошел
    console.log(num)
  }, [])

  callback()
  return null
}
```

Для обновления внешних переменных внутри `useCallback`, нам нужно прокинуть их в массив зависимостей:
```js
export function Component() {
  const num = Math.random()

  const callback = useCallback(() => {
    // Теперь num будет таким же, как и снаружи
    console.log(num)
  }, [num])

  callback()
  return null
}
```

Но что если нам нужна внешняя переменная, и при этом в массив зависимостей её передавать нельзя? С такой ситуацией ничего не сделать, необходимо менять логику работы колбэка. Например, чтобы колбэк просто изменял стейт, а `useEffect` обрабатывал изменения стейта с использованием любых переменных.

Пример:

```js
export function Component() {
  const [value, setValue] = useState()
  const num = Math.random()

  const handleChange = useCallback((option) => {
    setValue(option)
  }, [])

  useEffect(() => {
    console.log(num)
  }, [value])

  return null
}
```

---

Источники:
* [React Documentation | useCallback()](https://ru.reactjs.org/docs/hooks-reference.html#usecallback)
* [Всё ли вы знаете о useCallback()](https://habr.com/ru/post/529950/)
* [Your Guide to React.useCallback()](https://dmitripavlutin.com/dont-overuse-react-usecallback/)
