<div align="center">

# `useCallback`

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

Хук `useCallback` — возвращает мемоизированный колбэк.

### Проблема

Функции, которые написаны внутри компонента — создаются заново на каждый рендер.

В примере ниже, функция `handleClick` будет создана столько раз, сколько произойдет рендеров компонента `Cars`. А это значит, что каждый раз ссылка `handleClick` будет меняться.

```js
export function Cars() {
  const handleClick = () => {}

  return <Car onClick={handleClick} />
}
```

В целом — это нормально. Создание функций — это достаточно дешевый процесс.

### Когда использовать?
