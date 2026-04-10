# JaneOtabaeva — Лендинг

Сайт-лендинг Евгении Отабаевой (психолог, краткосрочная терапия).

## Страницы

- **`index.html`** — главная страница сайта (лид-магнит «5 типов невротического голода»)
- **`lead-magnet-neurotic-hunger.html`** — та же страница под отдельным URL для прямых ссылок из рекламы/рассылок

Обе страницы идентичны, чтобы работали любые входящие ссылки.

## Запуск локально

Откройте `index.html` в браузере. Никаких сборок и зависимостей не требуется — это чистый HTML/CSS/JS.

Либо поднимите локальный сервер:

```bash
python3 -m http.server 8000
# откройте http://localhost:8000
```

## Публикация на GitHub Pages

1. Settings → Pages
2. Source: `Deploy from a branch`
3. Branch: `main` / `/ (root)`
4. Сайт будет доступен по адресу `https://<username>.github.io/JaneOtabaeva/`

## Адаптивность

Сайт протестирован и работает на всех экранах:

- **<360px** — компактные телефоны
- **360–480px** — стандартные телефоны
- **768px+** — планшеты
- **1024px+** — десктоп
- **1200px+** — большие экраны

Используются `clamp()`, `meta viewport`, `overflow-x: hidden`, поддержка `prefers-reduced-motion` и `safe-area-inset` для iPhone с вырезом.

## Технологии

- HTML5
- CSS3 (custom properties, grid, media queries)
- Vanilla JavaScript (интерактивный тест с подсчётом признаков)
- Google Fonts: Cormorant Garamond, Nunito Sans

## Автор

Евгения Отабаева · [janeotabaeva.ru](https://janeotabaeva.ru)
