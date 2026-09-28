# CentreOS — Obsidian theme

Тема собрана из сниппетов CENTREOS (`obsidian theme cattpuccin.css`,
`home page + daily notes.css`, `tablet-top-ribbon.css`), переписана на
переменные Obsidian. Одна тема содержит **тёмную** (void + mauve) и
**светлую** (paper) версии — переключаются штатной кнопкой темы.

## Installation

1. Скопируй папку `CentreOS` в `<vault>/.obsidian/themes/CentreOS/`
   (файлы `theme.css` + `manifest.json`).
   - На ПК: уже установлена в `Memory\.obsidian\themes\CentreOS\`.
   - На телефоне/планшете: скопируй папку вручную (`.obsidian` не синкается).
2. Obsidian → Settings → Appearance → Themes → выбери **CentreOS**.
3. Dark/Light — кнопкой темы.

> BRAT устанавливает только **плагины**, темы он не умеет. Файлы из релиза
> (`theme.css` + `manifest.json`) — это ровно то, что нужно для ручной установки.

## Changelog


### 1.0.4
- Добавлена **базовая раскладка дашборда** (`.dashboard-grid`, `.col-left`/`.col-right`, `.tablet-two-col`/`.tablet-three-col`): на ноутбуке/десктопе Home Page снова двухколоночный (левая колонка `1fr`, правая `2fr`). Блок phone/tablet ниже по-прежнему складывает всё в один столбец.
- Home-страницы теперь регистрируют **device-классы** `.dashboard-laptop` / `.dashboard-phone` — благодаря этому адаптивные правила темы реально применяются (раньше они не срабатывали).
- Базовые стили `details.mobile-collapsible` перенесены на уровень темы, а не только внутри `.dashboard-phone`.

### 1.0.2
- Селекторы кнопок уточнены (`.centreos-dashboard .tech-button-main`), чтобы стили Obsidian не перебивали тему — кнопка `OPEN_DAILY_NOTE` снова горит.

### 1.0.1
- Кнопка `tech-button-main` (кнопка открытия daily-заметки) снова акцентная: градиент + свечение и hover.

### 1.0.0
- Единая тема из трёх CENTREOS-сниппетов, переписана на переменные Obsidian.
- Тёмная (void + mauve/blue/green) и светлая (paper) версии в одном файле.
- Компоненты сохранены: `hud-card`, `habit-card` (active/failed/neutral),
  `rpg-card`, `skill-*`, `inventory-*`, `avatar-frame`, `character-nick`,
  `hud-mini-btn`, `handwriting-link-btn`, прогресс-бары.
- Планшетный верхний ribbon, адаптив `dashboard-phone` / `dashboard-tablet`.
- Доступность: `:focus-visible`, `prefers-reduced-motion`.

## Палитра

| Роль | Тёмная | Светлая |
|---|---|---|
| background | `#0d0d1c` | `#ffffff` |
| secondary  | `#0a0a16` | `#f3f1f9` |
| card       | `#18182a` | `#ffffff` |
| primary (mauve) | `#d1abfd` | `#7b4ddb` |
| secondary (blue) | `#85b7eb` | `#2f6fb5` |
| tertiary (green) | `#5dcaa5` | `#12876a` |
| danger | `#f07070` | `#cf4040` |
| text | `#e6e3fa` | `#1c1a2e` |

## Правки

- Цвета — в блоках `body.theme-dark` / `body.theme-light`.
- Заголовки (капс, межбуквенный интервал, свечение) — секция HEADINGS.
- Компоненты — секция CENTREOS COMPONENTS (классы сохранены как в сниппетах).

Автор: Ilmir.
