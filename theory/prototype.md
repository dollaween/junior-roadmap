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

Для того, чтобы создать объект с тем же набором свойств и методов, воспользуемся методом `Object.create()`:
```js
const houseOfJohn = Object.create(house)
```

Попробуем вывести объект `houseOfJohn` в консоль и посмотреть что получилось:
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

Сам наш объект `houseOfJohn` пустой, но у него появилось свойство `__proto__`, в котором содержатся все свойства и методы объекта `house`.
```js
// Теперь мы можем доставать то, что хранится в house таким путем:
console.log(houseOfJohn.__proto__.city)          // 'Moscow'
console.log(houseOfJohn.__proto__.getAddress())  // 'Moscow, Gorodskaya'

// Писать __proto__ необязательно
console.log(houseOfJohn.city)    // 'Moscow'
console.log(houseOfJohn.street)  // 'Gorodskaya'
```

Каким образом работает `houseOfJohn.city`:
1. Javascript смотрит, есть ли у объекта `houseOfJohn` свойство `city`.
2. Если такого свойства нет, то он идет в объект `__proto__` и ищет свойство `city` там.
3. Второй пункт будет повторяться до тех пор, пока свойство не будет найдено, либо пока не закончится вся цепочка прототипов.

---

<div align="center">

### Работа с прототипами

</div>

---

Каждый раз, когда мы будем что-то изменять в корневом объекте, все прототипы этого объекта будут получать эти изменения.

```js
const user = {
  role: 'admin'
}

const anotherUser = Object.create(user)

user.role = 'moderator'

console.log(anotherUser.role)  // 'moderator'
```

---

В протатипах мы можем переопределять все поля и добавлять новые — это никак не скажется на корневом объекте:

```js
const car = {
  model: 'BMW',
  hasWheels: true
}

const anotherCar = Object.create(car)

anotherCar.model = 'Lexus'
anotherCar.year = 2010

console.log(car.model)             // 'BMW'
console.log(car.hasWheels)         // true
console.log(car.year)              // undefined
console.log(anotherCar.model)      // 'Lexus'
console.log(anotherCar.hasWheels)  // true
console.log(anotherCar.year)       // 2010
```

---

Источники:
* [Наследование и цепочка прототипов](https://developer.mozilla.org/ru/docs/Web/JavaScript/Inheritance_and_the_prototype_chain)
