<div align="center">

# Исправление популярных ошибок

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

<div align="center">

`A component is changing an uncontrolled input to be controlled`

</div>

---

Пример, в котором возникает такая ошибка:

```jsx
export function Component() {
  const [text, setText] = useState()

  function handleChange(e) {
    setValue(e.target.value)
  }

  return <input type="text" onChange={handleChange} value={text} />
}
```

#### Проблема

Проблема в строчке `const [text, setText] = useState()`.  
Изначально `text = undefined`. Передавая в `input` в свойство `value` значение `undefined` мы говорим полю о том, что внешне на его значение мы никак не влияем и он должен сам управлять своим `value`.

Далее мы изменяем `text` и опять передаем его в `value` для `input`. Таким движением мы говорим полю о том, что теперь его значением `value` управляют снаружи. Это и вызывает ошибку.

##### Решение

Не передавайте в качестве `value` значение `undefined`. Например, сделав так:  
`const [text, setText] = useState('')`

- [Объяснение на Stack Overflow](https://stackoverflow.com/questions/47012169/a-component-is-changing-an-uncontrolled-input-of-type-text-to-be-controlled-erro)
