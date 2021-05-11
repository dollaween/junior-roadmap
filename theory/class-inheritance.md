<div align="center">

# Наследование классов

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

Для наследования свойств и методов одного класса из другого, используется ключевое слово `extends`.

```js
class Animal {
  constructor(name) {
    this.name = name
  }

  speak() {
    console.log(`${this.name} издает звук`)
  }

  jump() {
    console.log(`${this.name} прыгает`)
  }
}

class Dog extends Animal {
  constructor(name) {
    super(name)
  }

  speak() {
    console.log(`${this.name} лает`)
  }
}

const dog = new Dog('Шарик')

dog.speak()  // 'Шарик лает'
dog.jump()   // 'Шарик прыгает'
```

В примере выше мы расширили класс `Dog`, добавив в него методы класса `Animal`.

Мы можем наследовать классы цепочкой друг от друга. В примере ниже класс `Buldog` имеет свойства и методы и класса `Dog`, и класса `Animal`.

```js
class Animal { /* ... */ }
class Dog extends Animal { /* ... */ }
class Buldog extends Dog { /* ... */ }
```
