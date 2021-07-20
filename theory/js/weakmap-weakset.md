<div align="center">

# WeakMap и WeakSet

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

Объект `WeakMap` — это коллекция пар `ключ: значение`.

Особенности `WeakMap`:
- В качестве ключей, у `WeakMap` могут быть использованы только объекты (примитивы, включая `Symbol`, запрещены).
- Ключи `WeakMap` не перечисляемы (то есть нет метода, который возвращает список ключей).

#### Зачем нужен `WeakMap`?

Объект `WeakMap` нужен для оптимизации работы с памятью и предотвращению потенциальных утечек памяти.

#### Каким образом это достигается?

Сборщик мусора не удалит объект из памяти до тех пор, пока он где-то используется. При использовании в качестве ключа объект, в коллекции `Map`, этот объект будет находиться в памяти до тех пор, пока существует эта коллекция `Map`.

В этом плане `WeakMap` отличается от `Map` и `Array`: если объект будет удален, то и из коллекции `WeakMap` этот объект будет удален. То есть `WeakMap` никак не препятствует работе сборщика мусора.

Пример:
```js
const user = { login: 'Aragorn' }
const arr = [user]

user = null

// хоть мы и удалили ссылку на объект user, в памяти этот объект всё ещё будет существовать,
// так как он находится в массиве.
```

```js
const user = { login: 'Frodo' }
const weakMap = new WeakMap()

weakMap.set(user, 'online')

user = null

// теперь объект user удалится и из памяти, и из объекта weakMap
```

---

Источники:
- [`WeakMap` и `WeakSet`](https://learn.javascript.ru/weakmap-weakset)
- [MDN: `WeakMap`](https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/WeakMap)
