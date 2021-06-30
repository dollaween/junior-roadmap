<div align="center">

# `useEffect()`

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

Хук `useEffect(fn, deps)` — это функция, которая запускается в зависимости от массива зависимостей.

---

<div align="center">

### Проблема

</div>

---

---

<div align="center">

### Как использовать?

</div>

---

`useEffect(fn, deps)` принимает два параметра:
- `fn` — функция, которая будет выполнена.
- `deps` — массив зависимостей:
  - Отсутствует значение — функция `fn` будет срабатывать на каждый рендер.
  - `[]` (пустой массив) — функция `fn` сработает один раз после первого рендера.
  - `[elem1, elem2]` — функция `fn` будет срабатывать каждый раз, когда элементы внутри массива будут меняться.

---

Источники:
- [Справочник API хуков](https://ru.reactjs.org/docs/hooks-reference.html#useeffect)
- [Использование хука эффекта](https://ru.reactjs.org/docs/hooks-effect.html)
- [Полное руководство по `useEffect`](https://habr.com/ru/company/ruvds/blog/445276/)

