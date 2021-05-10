<div align="center">

# Прототипы

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

> В плане наследования, Javascript работает только с одной сущностью — объектами.

**Наследование** — это передача свойств и методов из одного объекта в другой.

Допустим, у нас есть объект:
```js
const house = {
  city: 'Moscow',
  street: 'Gorodskaya',
  getAddress: function() {
    return `${this.city}, ${this.street}`
  }
}
```

Для того, чтобы создать объект с теми же свойствами и методами, воспользуемся методом `create()`:
```js
const houseOfJohn = Object.create(house)
```

Теперь `houseOfJohn` связан с `house`. Попробуем вывести объект `houseOfJohn` в консоль и посмотреть что получилось:
```js
console.log(houseOfJohn)
/*
  {
    __proto__: {
      city: "Moscow",
      getAddress: ƒ (),
      street: "Gorodskaya",
      __proto__: Object
    }
  }
*/
```

Сам наш объект `houseOfJohn` пустой, но у него появилось свойство `__proto__`, в котором содержаться все свойства и методы объекта `house`.
```js
// Теперь мы можем доставать то, что храниться в house таким путем:
console.log(houseOfJohn.__proto__.city)          // 'Moscow'
console.log(houseOfJohn.__proto__.getAddress())  // 'Moscow, Gorodskaya'

// Писать __proto__ необязательно
console.log(houseOfJohn.city)    // 'Moscow'
console.log(houseOfJohn.street)  // 'Gorodskaya'
```

---

Источники:
* [Наследование и цепочка прототипов](https://developer.mozilla.org/ru/docs/Web/JavaScript/Inheritance_and_the_prototype_chain)
