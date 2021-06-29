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

Хук `useCallback()` — возвращает мемоизированный колбэк.

### Проблема

Функции, которые написаны внутри компонента — создаются заново на каждый рендер.

В примере ниже, функция `handleClick` будет создана столько раз, сколько произойдет рендеров компонента `Cars`. В целом — это нормально, создание функций — достаточно дешевый процесс.

```js
export function Cars() {
  const handleClick = () => {}

  return <Car onClick={handleClick} />
}
```

Постоянное пересоздание функции `handleClick` означает, что каждый раз ссылка на эту функцию будет меняться. Если ссылка постоянно меняется — значит компоненты, в которые мы передаем функцию, будут всегда перерисовываться на каждый рендер, даже если мы их обернем в `React.memo()`.

### Когда использовать?

Хук `useCallback()` стоит использовать в следующих ситуациях:
1. Когда мы передаем функцию как `props` и при этом важно, чтобы дочерний компонент не перерисовывался.
2. Когда используем `React.memo()` на дочерних элементах.
3. Когда функция является зависимостью для других хуков (например, `useEffect()`)

---

Источники:
* [React Documentation | useCallback()](https://ru.reactjs.org/docs/hooks-reference.html#usecallback)
* [Всё ли вы знаете о useCallback()](https://habr.com/ru/post/529950/)
* [Your Guide to React.useCallback()](https://dmitripavlutin.com/dont-overuse-react-usecallback/)
