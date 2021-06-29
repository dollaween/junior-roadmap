<div align="center">

# Базовые тесты по React

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

##### 1. Стоит ли использовать хук `useCallback()` в данной ситуации?

```js
export function Parent() {
  const handleClick = useCallback(() => {
    console.log('Clicked')
  }, [])

  return <Child onClick={handleClick} />
}

export function Child({ onClick }) {
  return <div onClick={onClick}>Example text</div>
}
```

1. Да
2. Нет
3. Нет никакой разницы, что с ним, что без него
4. Будет ошибка

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 2**

  Это пример, когда оптимизация стоит дороже, чем её отсутствие. Компонент `Child` — простой и не создает проблем для производительности. В этом случае `useCallback()` только усложнит код.

</p>
</details>



