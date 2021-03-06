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

**Прототип** — это объект, от которого будут унаследованы свойства и методы.

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
// Теперь мы можем доставать то, что хранится в house таким путем (такие свойства называются унаследованными):
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

Каждый раз, когда мы будем что-то изменять в корневом объекте, все дочерние объекты будут получать эти изменения.

```js
const user = {
  role: 'admin'
}

const anotherUser = Object.create(user)

user.role = 'moderator'

console.log(anotherUser.role)  // 'moderator'
```

---

В дочерних объектах мы можем переопределять все поля и добавлять новые — это никак не скажется на корневом объекте:

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

<div align="center">

### Зачем нужны прототипы?

</div>

---

С помощью прототипов мы можем создавать множество однотипных объектов, или объектов с общими свойствами и методами.

Чтобы каждый раз вручную не создавать много однотипных объектов:
```js
const firstArticle = {
  title: 'How to Code',
  year: 2021,
  author: 'John Smith',
  getInfo: function() {
    return `${this.title} by ${this.author}, ${this.year}`
  }
}

const secondArticle = {
  title: 'What is Closure?',
  year: 2021,
  author: 'Brad Force',
  getInfo: function() {
    return `${this.title} by ${this.author}, ${this.year}`
  }
}

const thirdArticle = {
  title: 'The Secret of Objects',
  year: 2020,
  author: 'John Smith',
  getInfo: function() {
    return `${this.title} by ${this.author}, ${this.year}`
  }
}
```

Мы можем написать объект, от которого будут наследоваться все остальные. Например, таким образом:
```js
const Article = {
  constructor: function(title, year, author) {
    this.title = title
    this.year = year
    this.author = author
  }
  getInfo: function() {
    return `${this.title} by ${this.author}, ${this.year}`
  }
}

const firstArticle = Object.create(Article).constructor('How to Code', 2021, 'John Smith')
const secondArticle = Object.create(Article).constructor('What is Closure?', 2021, 'Brad Force')
const thirdArticle = Object.create(Article).constructor('The Secret of Objects', 2020, 'John Smith')
```

1. Теперь мы можем создавать множество похожих объектов в более удобной форме.
2. Чтобы изменить поведение метода `getInfo()` — нам достаточно отредактировать его только в корневом объекте `Article` и изменения сразу получат все дочерние объекты.
3. Чтобы расширить функционал — нам опять же достаточно только внести изменения в `Article`.

---

<div align="center">

### Собственные свойства

</div>

---

Если вам необходимо проверить, определено ли свойство у самого объекта, а не где-то в его цепочке прототипов, вы можете использовать метод `hasOwnProperty()`.

```js
const plant = {
  color: 'green'
}

const anotherPlant = Object.create(plant)
anotherPlant.name = 'cactus'

console.log(anotherPlant.color)                    // 'green'
console.log(anotherPlant.hasOwnProperty('color'))  // false
console.log(anotherPlant.hasOwnProperty('name'))   // true
```

---

Источники:
* [Наследование и цепочка прототипов](https://developer.mozilla.org/ru/docs/Web/JavaScript/Inheritance_and_the_prototype_chain)
