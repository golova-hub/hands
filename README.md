# Верстка для проекта hands для 1С-Битрикс

## Общая структура

hands/
├─ html/                  # Страницы-примеры (статическая верстка)
│   ├─ index.html
│   ├─ catalog.html
│   ├─ product.html
│   ├─ news.html
│   └─ 404.html
│
├─ src/
│   └─ scss/
│       ├─ app.scss       # Точка входа для сборки CSS
│       ├─ _variables.scss  # Переопределения Bootstrap
│       ├─_fonts.scss      # Подключение шрифтов
│
│
├─ assets/
│   ├─ fonts/nunito-sans/   # Локальные шрифты
│   ├─ images/
│   └─ js/
│
├─ dist/
│   └─ css/app.css          # Скомпилированный итоговый CSS
│
├─ package.json
├─ .gitignore
└─ README.md

---

## Сборка и локальный просмотр

### Установка

npm install

### Запуск режима разработки (автообновление + сервер)

npm run dev
Откроется страница: <http://localhost:5173/html/index.html￼>
Все изменения в .scss, .html и assets/ пересобираются автоматически.

### Финальная сборка CSS

npm run build
Результат:
dist/css/app.css

## Используемые технологии

Bootstrap 5.3.8 — сетка и базовые компоненты
Sass (dart-sass) — препроцессор
BrowserSync — локальный сервер и автообновление
Nunito Sans — variable-шрифт (WOFF2)
Без бандлера (простая сборка, чистый Sass)

## Шрифты: Nunito Sans Variable

Используется вариативный шрифт (variable font) с осями:
wght, wdth, opsz, YTLC.
файл assets/fonts/nunito-sans/NunitoSans-Variable.woff2

Подключение — src/scss/_fonts.scss
Bootstrap настроен на Nunito Sans в src/scss/_variables.scss

## Настройки Bootstrap (кастомизация)

src/scss/_variables.scss содержит основные переопределения
Bootstrap установлен через npm и импортируется в src/scss/app.scss

## BX-разметка

В HTML добавлены пометки для интегратора <!-- BX:  -->
