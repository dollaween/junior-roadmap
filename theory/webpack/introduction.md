<div align="center">

# Введение в Webpack

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

**Webpack** — это инструмент, который помогает собирать проекты.

С помощью Webpack можно:
- Объединять несколько файлов в один.
- Преобразовывать файлы. Например, SASS в CSS или Typescript в Javascript.
- Перемещать файлы.
- Минифицировать файлы.
- Находить и удалять неиспользуемый код.

---

<div align="center">

### Установка

</div>

---

```bash
mkdir webpack-demo
npm init
npm i webpack webpack-cli --save-dev
```

---

<div align="center">

### CLI команды

</div>

---

```bash
# Запускает процесс сборки с указанием конфигурационного файла
npx webpack --config webpack.config.js
```

---

<div align="center">

### Конфиг

</div>

---

`mode`:
- `development` — не минифицирует итоговый бандл.
- `production` — миницифирует итоговый бандл.
