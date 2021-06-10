<div align="center">

# Watch и LiveReload

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

Для автоматической компиляции кода есть следующие инструменты:
1. Webpack Watch Mode
2. webpack-dev-server
3. webpack-dev-middleware

---

<div align="center">

### Webpack Watch Mode

</div>

---

[Watch Mode](https://webpack.js.org/guides/development/#using-watch-mode) — позволяет отслеживать зависимые файлы и запускать процесс сборки при их изменении.

Для этого запустите команду `webpack` с флагом `--watch`. Эту команду можно добавить в `package.json`:

```json
{
  "name": "webpack-demo",
  "version": "1.0.0",
  "scripts": {
    "build": "webpack",
    "watch": "webpack --watch"
  },
}
```
