بِسْمِ اللهِ في أَوَّلِهِ وَآخِـرِه
# Tree Architecture Specification

Во Имя Аллаха Милостевого Милосердного

Основано на HTML DOM, FSD, Atomic Design

Hightload and/or Accessibility version "Kiparis"

Any interface can simplify to resource value and has principles of accessibility.


- [x] легкое расширение функционала приложения;
- [x] безболезненное внесение изменений в существующий функционал;
- [x] унифицированная структура приложения;
- [x] быстрый onboarding новых разработчиков на проект;
- [x] понятный и прозрачный код (DRY, KISS);
- [x] всегда понятно где в структуре файлов расположить ту или иную функциональность;



Архитектурное естествознание систем помогает проведенной аналогией осознать взаимодействие подсистем в приложениях.
Не абстрактные слои, понятия, а органичная структура в которой отраженно взаимодействие частей.


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
