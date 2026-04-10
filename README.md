# JaneOtabaeva.ru — сайт

Статичный сайт Евгении Отабаевой (психолог, гипнотерапевт, краткосрочная терапия).

Исходно сделан в Tilda, перенесён на GitHub Pages с переписыванием внутренних ссылок.

## Точка входа

**`index.html`** — главная страница.

Сайт открывается тут: **https://alexotabaev.github.io/JaneOtabaeva/**

## Структура

- 🗺️ **Карта сайта и архитектура** → [`SITEMAP.md`](SITEMAP.md)
- 📋 **Реестр всех страниц с описанием** → [`PAGES.md`](PAGES.md)
- 📄 **38 HTML-страниц** в корне репо (с человекочитаемыми именами: `about.html`, `blog.html`, `peresborka.html` и т.д.)
- 🎨 **Ассеты Tilda:** `css/`, `js/`, `images/`, `files/`
- 🚫 **`404.html`** — кастомная страница ошибки

## Основные страницы (в меню)

| Пункт меню | Файл |
|---|---|
| Главная | `index.html` |
| Метод «Пересборка» | `peresborka.html` |
| Диагностика | `diagnostic.html` |
| Обо мне | `about.html` |
| Ближайший вебинар | `intensivo.html` |
| Блог | `blog.html` |

## Что было сделано при импорте из Tilda

1. **Переименованы страницы** — `pageXXXXX.html` → человекочитаемые (`about.html`, `peresborka.html`, …). Маппинг взят из `.htaccess`, который Tilda положила в экспорт.
2. **Переписаны внутренние ссылки** — все `href="https://janeotabaeva.ru/about"` и `href="/about"` переделаны на `href="about.html"`, чтобы работали локально и на GitHub Pages без собственного домена.
3. **Проверено 146 ассетов** — все найдены, битых ссылок на картинки/CSS/JS нет.
4. **Проверено 0 битых внутренних `.html` ссылок** — меню полностью кликабельны.
5. **Дубли и устаревшее** помечены в `PAGES.md` с рекомендацией «в архив» или «удалить».
6. **Создана кастомная `404.html`** вместо дефолтной Тильдовской заглушки.
7. **Наш лид-магнит `5prichin.html`** сохранён как отдельная страница, CTA перенастроен на локальный `intensiv.html`.

## Локальный запуск

Любой статический сервер подойдёт — нет ни сборки, ни зависимостей:

```bash
python3 -m http.server 8000
# http://localhost:8000
```

Или просто открой `index.html` в браузере (но некоторые Tilda-скрипты могут не отработать из-за `file://` — лучше через сервер).

## Публикация на GitHub Pages

Уже включено:

- Settings → Pages → Source: `Deploy from a branch` → `main` → `/ (root)`
- URL: https://alexotabaev.github.io/JaneOtabaeva/

После каждого `git push` в `main` GitHub Pages пересобирается автоматически (1–3 минуты).

## Подключение своего домена

См. отдельный разговор в сессии — краткая инструкция:

1. DNS: A-записи apex → 4 IP GitHub (`185.199.108.153`…`111.153`) + CNAME `www` → `alexotabaev.github.io.`
2. Settings → Pages → Custom domain: `janeotabaeva.ru`
3. Enforce HTTPS — когда DNS дойдёт.

## Технологии

- Статичный HTML (экспорт Tilda)
- Tilda CSS/JS (`tilda-blocks-*.min.css`, `tilda-scripts-3.0.min.js`)
- jQuery 1.10.2 (под капотом Tilda)
- Google Fonts: Lora, Noto Sans, Cormorant Garamond (для нашего лид-магнита)

## Автор

Евгения Отабаева · психолог, гипнотерапевт
