# Tree Architecture Manifest

Во Имя Аллаха Милостевого Милосердного


Hightload and/or Accessibility version "Topol"

Any interface can simplify to resource value and has principles of accessibility.

Пример vuejs tree архитектуры 

- roots (api list to backend)
    - index.js
- copillars (store pinia/vuex)
- branches (components)
    - twigs (basic components)
- bark (pages)
- trunk (layouts)

Продолжая аллегорию дерева мы можем понять архитектуру. 

- [x] легкое расширение функционала приложения;
- [x] безболезненное внесение изменений в существующий функционал;
- [x] унифицированная структура приложения;
- [x] быстрый onboarding новых разработчиков на проект;
- [x] понятный и прозрачный код;
- [x] всегда понятно где в структуре файлов расположить ту или иную функциональность;

Архитектурное естествознание систем помогает проведенной аналогией осознать взаимодействие подсистем в приложениях.
Не абстрактные слои, понятия, я органичная система в которой отраженно взаимодействие частей.


Давайте разберём строение дерева, основные части:
- крона
- ствол
- корень
  
Получаем 3 слоя ответственности

Где:
- крона: отвечает за отображаемые страницы, стили, асеты.
- ствол: библиотеки, хранилище, куки.
- корень: за взаимодействие с api любое взаимодействие с сервером(ами), URL, HTTP.

Проанализировав аллегорию дерева и абстрагировав его части мы можем обобщить во едино архитектуру:

Представим структуру папок для проекта на vue:

<code>
├── tree (src)
│   ├── crown
│   │   ├── foliage (pages)
│   │   ├── flowers (styles)
│   │   ├── fruits (assets, fonts)
│   │   ├── branches (components)
│   │   │   ├── branches (basic)
│   │   │   ├── branches (composite)
│   ├── roots
│   │   ├── api
│   │   ├── router
│   ├── trunk
│   │   ├── store
│   │   ├── localstorage
│   │   ├── libs
├── main.js
├── package.json
└── tsconfig.json
</code>
