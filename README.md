# CentreOS — Obsidian theme

Тема для Obsidian: **тёмная** (void + mauve) и **светлая** (paper) в одном файле,
переключаются штатной кнопкой темы. Собрана из сниппетов CENTREOS
(`obsidian theme cattpuccin.css`, `home page + daily notes.css`, `tablet-top-ribbon.css`)
и переписана на переменные Obsidian.

## Установка

### Через BRAT (рекомендуется)
1. В Obsidian установи плагин **BRAT** (Beta Reviewers Auto-update Tool).
2. Открой настройки BRAT → **Add Beta theme** → вставь `and50005000/theme_obsidian`.
3. Settings → Appearance → Themes → выбери **CentreOS**.
4. Обновления — кнопкой **Check for updates** в BRAT.

### Вручную
1. Скопируй папку в `<vault>/.obsidian/themes/CentreOS/` (файлы `theme.css` + `manifest.json`).
   - На ПК уже установлена в `Memory\.obsidian\themes\CentreOS\`.
   - На телефоне/планшете скопируй папку вручную (`.obsidian` не синкается) — либо через BRAT.
2. Settings → Appearance → Themes → выбери **CentreOS**.

## Репозиторий и релизы
- GitHub: `and50005000/theme_obsidian`
- Ассеты релиза: `theme.css` + `manifest.json`. Тег = значение `version` в `manifest.json`.

## Changelog


### 1.2.1
- Исправлено: на планшете и телефоне пустая полоса над вкладками больше не резервируется — горизонтальная лента наверху рисуется только если в ней есть кнопки; если лента пустая, вкладки прижаты к верхнему краю экрана.

### 1.2.0
- Домашняя страница переведена на спокойную раскладку «Quiet Console»: командная панель (дата, счётчик дней до 2030, кнопка дневника), разделы Contour / Operations / Knowledge / Planning.
- Карточки стали тише: ровные границы, мягкие тени; свечения остались только у прогрессов, кнопки дневника и срочных статусов.
- Сроки теперь с чипами (overdue / N d left), операции и проекты с приоритетами; книги и заметки — компактными строками.
- TEMPORAL_PHASE: спокойная ось «прошлое → сейчас → будущее», статика без анимаций.
- Новые стили изолированы классами `q-*`; старые компоненты (habit-card и другие) не затронуты.
- Обновите также скрипты: `System/Scripts/dashboard_laptop.js` и `System/Scripts/dashboard_tablet.js`.

### 1.0.5
- **Фикс кнопки `OPEN_DAILY_NOTE` и всего дашборда.** Внутри `.centreos-dashboard` была самоссылка переменной `--c-primary: var(--c-primary)`, из-за которой переменная становилась невалидной в этой области: кнопка не «горела» (без градиента и свечения), а все элементы с `--c-primary` внутри дашборда (акцентные полоски, прогресс-бары) оставались без стилей. Строка удалена — переменная снова наследуется от `body.theme-dark/light`.

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
