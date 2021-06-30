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

---

##### 2. В каком компоненте функция `handleClick` создается реже?

```js
function ComponentA() {
  const handleClick = () => {}
  return null
}

function ComponentB() {
  const handleClick = useCallback(() => {}, [])
  return null
}
```

1. В `ComponentA`
2. В `ComponentB`
3. В обоих одинаково
4. Будет ошибка

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 3**

  В `ComponentA` функция будет создаваться при каждом рендере компонента.  
  В `ComponentB` — функция через `useCallback` так же будет создаваться при каждом рендере.

  `useCallback` — это самая обычная функция, которая внутри себя имеет в довесок место для хранения состояний и встроенные проверки. Каждый рендер она создается заново, получает **новую** функцию для мемоизации и **новый** массив зависимостей, и заново делает проверки.

  Подробнее: [Все ли вы знаете о useCallback](https://habr.com/ru/post/529950/).

</p>
</details>

---

##### 3. Какой будет вывод?

```js
function Component() {
  const [count, setCount] = useState(0)
  
  function showCount() {
    setTimeout(() => console.log(count), 3000)
  }

  if (count === 0) {
    setCount(count + 1)
    showCount()
  }
}
```

1. `0`
2. `1`
3. `2`
4. `3`

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 1**

  `count` является константой для каждого конкретного рендера. Функция `showCount` вызывается только на первом рендере, поэтому для нее `count` будет равен нулю.
  
  Это пример побочного эффекта (side effect), который должен решаться с помощью хука `useEffect`.

</p>
</details>

---

##### 4. Если по элементу `button` быстро кликнуть 2 раза — какой будет вывод в консоль?

```js
function Component() {
  const [count, setCount] = useState(0)

  useEffect(() => {
    setTimeout(() => {
      console.log(count)
    }, 3000);
  })

  return <button onClick={() => setCount(count + 1)}>Click me</button>
}
```

1. Одно сообщение: `0`
2. Два сообщения: `1`, `2`
3. Одно сообщение: `2`
4. Два сообщения: `0`, `1`

<details><summary><b>Ответ</b></summary>
<p>

  **Ответ: 2**

</p>
</details>
