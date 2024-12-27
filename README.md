بِسْمِ اللهِ في أَوَّلِهِ وَآخِـرِه
# Tree Architecture Specification

Во Имя Аллаха Милостевого Милосердного

Основано на HTML DOM, FSD, Atomic Design

version "Kiparis"

Any interface can simplify to resource value and has principles of accessibility.

- [x] Лёгкое расширение функционала;
- [x] Простое внесение нового функционала;
- [x] Унифицированная структура приложения;
- [x] Лёгкий Onboarding;
- [x] Поддержка DRY, KISS, etc.;
- [x] Прексказуемое расположение функциональности;

Естествознание систем помогает проведенной аналогией осознать взаимодействие подсистем в приложениях.
Не абстрактные слои, понятия, а органичная структура понятная с детства - в которой отраженно взаимодействие частей.

Давайте разберём строение дерева, основные части:
- крона
- ствол
- корень
  
Получаем 3 слоя ответственности

Где:
- крона: отвечает за отображаемые страницы, стили, асеты.
- ствол: библиотеки, хранилище, куки.
- корень: за взаимодействие с api любое взаимодействие с сервером(ами), URL, HTTP.

##### Проанализировав аллегорию дерева и абстрагировав его части мы можем обобщить во едино архитектуру:

### Пример абстрактного проекта:
```md
├── tree
│   ├── crown
│   │   ├── foliage
│   │   ├── flowers
│   │   ├── fruits
│   │   ├── branches
│   │   │   ├── branches
│   │   │   │   └── bud.jsx
│   │   │   ├── branches
│   │   │   │   └── bud.jsx
│   ├── roots(core)
│   │   ├── file.js
│   │   └── file.js
│   ├── trunk
│   │   ├── rings
│   │   ├── bark
│   │   └── cork
├── main.js
└── package.json
```
Структура вариативна, расширяема. 

### Пример для проекта на vue:

```md
├── tree (src)
│   ├── view
│   │   ├── pages
│   │   ├── assets
│   │   ├── components
│   │   │   ├── basic
│   │   │   │   ├── cButton.vue
│   │   │   │   └── cInput.vue
│   │   │   ├── composite
│   │   │   │   └── cUploadFile.vue
│   ├── roots
│   │   ├── vendor.js
│   │   ├── router.js
│   ├── trunk
│   │   ├── store
│   │   └── composables
├── main.js
├── package.json
└── tsconfig.json
```
Продолжая аллегорию дерева можно расширять архитектуру.

### Пример для проекта на react:

```md
├── src
│   ├── view
│   │   ├── pages
│   │   ├── assets
│   │   ├── components
│   │   │   ├── input
│   │   │   │   ├── index.jsx
│   │   │   │   ├── input-date
│   │   │   │   │   └── index.jsx
│   │   │   ├── button
│   │   │   │   ├── index.jsx
│   │   │   │   ├── button-upload
│   │   │   │   │   └── index.jsx
│   │   │   │   ├── button-download
│   │   │   │   │   └── index.jsx
│   ├── core
│   │   ├── vendor.jsx
│   │   ├── router.jsx
│   ├── libs
│   │   ├── store
│   │   ├── utils
├── main.js
├── package.json
└── tsconfig.json
```
