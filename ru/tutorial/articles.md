---
id: 75
displayName: Создание статей
order: 40
published: true
historyName: Создание статей
historyDescription: Добавление статей в разделы, настройка мета-свойств и управление отображением.
seoTitle: Туториал - Создание статей
---

# Создание статей

На этом этапе мы создадим статьи, добавим их в разделы, настроим отображение в интерфейсе и обеспечим синхронизацию между языками.

## [Пошаговое руководство для создания статей](steps)

### [Статья 1: Введение / Introduction](article-1)

Рассмотрим поэтапно, как добавлять мета-свойства в статью. Для начала создадим два файла:

```
/ru/guides/basic/intro.md
/en/guides/basic/intro.md
````


Пошаговое добавление мета-свойств:

- Добавим уникальный идентификатор статьи `id`. Он должен совпадать в обоих языках.
```md
id: 1001
```

- Добавим название статьи, отображаемое в меню и других интерфейсах `displayName`.
```md
displayName: Введение
```

```md
displayName: Introduction
```

- Добавим порядок отображения статьи внутри раздела `order`.
```md
order: 10
```

- Добавим флаг публикации `published`. Если `false`, статья не будет отображаться нигде.
```md
published: true
```

- Добавим статьи в блок истории:
  - название статьи с помощью `historyName`
  - краткое описание статьи с помощью `historyDescription`
```md
historyName: Введение
historyDescription: Стартовая статья
```

```md
historyName: Introduction
historyDescription: Initial article
```

- Добавим отображение статьи на главной странице в одной из секций `categories`:
  - название секции `category` из списка `categories` в `metadata.md` текущего языка;
  - название статьи `categoryName`;
  - описание статьи `categoryDescription`;
  - порядковый номер статьи `categoryOrder`;
  - иконка отображаемая рядом со статьёй `categoryIcon`;

```md
category: Начало работы
categoryName: Введение
categoryDescription: Начальный шаг
categoryOrder: 10
categoryIcon: https://img.solarspace.pro/docs/internet.svg
```

```md
category: Getting Started
categoryName: Introduction
categoryDescription: First step
categoryOrder: 10
categoryIcon: https://img.solarspace.pro/docs/internet.svg
```


- Отображение ссылки на статью в шапке сайта.
  - название статьи в шапке `headerName`;
  - порядок статьи в шапке `headerOrder`;

```md
headerName: Введение
headerOrder: 10
```

```md
headerName: Introduction
headerOrder: 10
```


- Отображение ссылки на статью в подвале сайта.
  - название статьи в подвале `footerName`;
  - порядок статьи в подвале `footerOrder`;

Отображение ссылки на статью в подвале сайта.

```md
footerName: Введение
footerOrder: 20
```

```md
footerName: Introduction
footerOrder: 20
```


- Добавим заголовок страницы и мета-тег SEO `seoTitle`

```md
seoTitle: Введение
```

```md
seoTitle: Introduction
```

- Добавим содержимое статей в markdown-разметке:
```md
# Введение

Это первая статья, в которой описан основной подход к документации.
```

```md
# Introduction

This is the first article that introduces the documentation approach.
```


По результатам действий выше, получим следующее:
  - в `ru/guides/basic/intro.md`
```md
---
id: 1001
displayName: Введение
order: 10
published: true
historyName: Введение
historyDescription: Стартовая статья
category: Начало работы
categoryName: Введение
categoryDescription: Начальный шаг
categoryOrder: 10
categoryIcon: https://img.solarspace.pro/docs/internet.svg
headerName: Введение
headerOrder: 10
footerName: Введение
footerOrder: 20
seoTitle: Введение
---

# Введение

Это первая статья, в которой описан основной подход к документации.
```

  - в `en/guides/basic/intro.md`
```md
---
id: 1001
displayName: Introduction
order: 10
published: true
historyName: Introduction
historyDescription: Initial article
category: Getting Started
categoryName: Introduction
categoryDescription: First step
categoryOrder: 10
categoryIcon: https://img.solarspace.pro/docs/internet.svg
headerName: Introduction
headerOrder: 10
footerName: Introduction
footerOrder: 20
seoTitle: Introduction
---

# Introduction

This is the first article that introduces the documentation approach.
```


### Статья 2: Контакты / Contacts
### [Статья 2: Контакты / Contacts](article-2)

Создадим файлы:

```
/ru/contacts.md
/en/contacts.md
```

- Добавим уникальный идентификатор статьи `id`. Он должен совпадать в обоих языках.
```md
id: 1002
```

- Добавим название статьи, отображаемое в меню и других интерфейсах `displayName`.
```md
displayName: Контакты
```

```md
displayName: Contacts
```

- Добавим порядок отображения статьи внутри раздела `order`.
```md
order: 20
```

- Добавим флаг публикации `published`. Если `false`, статья не будет отображаться нигде.
```md
published: true
```

- Отображение ссылки на статью в шапке сайта.
  - название статьи в шапке `headerName`;
  - порядок статьи в шапке `headerOrder`;

```md
headerName: Контакты
headerOrder: 30
```

```md
headerName: Contacts
headerOrder: 30
```

- Добавим свойство `ignoreInterfaces` для его сокрытия в определённой части интерфейса, в нашем случае нужно скрыть в меню, блоке истории, категориях и подвале.
```md
ignoreInterfaces:
  - menu
  - history
  - category
  - footer
```

- Добавим заголовок страницы и мета-тег SEO `seoTitle`

```md
seoTitle: Контакты
```

```md
seoTitle: Contacts
```


По результатам действий выше, получим следующее:
- в `ru/contacts.md`
```md
---
id: 1002
displayName: Контакты
order: 20
published: true
headerName: Контакты
headerOrder: 30
ignoreInterfaces:
  - menu
  - history
  - category
  - footer
seoTitle: Контакты
---

# Контактная информация

Здесь вы можете указать контактные данные вашей компании.
```

- в `en/contacts.md`
```md
---
id: 1002
displayName: Contacts
order: 20
published: true
headerName: Contacts
headerOrder: 30
ignoreInterfaces:
  - menu
  - history
  - category
  - footer
seoTitle: Contacts
---

# Contact Information

Here you can provide contact details for your company.
```


Вот оформленный раздел для **Статьи 3: История / History**, приведённый к такому же формату, как статья 1:

---

### [Статья 3: История / History](article-3)

Создадим два файла для статьи:

```
/ru/guides/advanced/history.md
/en/guides/advanced/history.md
```

Пошаговое добавление мета-свойств:

- Добавим уникальный идентификатор статьи `id`, одинаковый для обоих языков.

```md
id: 1003
```

- Добавим название статьи `displayName`.

```md
displayName: История
```

```md
displayName: History
```

- Добавим порядок отображения статьи внутри раздела `order`.

```md
order: 10
```

- Укажем флаг публикации `published`.

```md
published: true
```

- Укажем отображение статьи в блоке истории с помощью:

  - `historyName` — название;
  - `historyDescription` — краткое описание.

```md
historyName: История
historyDescription: Пример блока истории
```

```md
historyName: History
historyDescription: History block example
```

- Укажем отображение статьи на главной странице:

  - секция — `category`;
  - название — `categoryName`;
  - описание — `categoryDescription`;
  - порядок — `categoryOrder`;
  - иконка — `categoryIcon`.

```md
category: Основы
categoryName: История
categoryDescription: Демонстрация истории
categoryOrder: 20
categoryIcon: https://img.solarspace.pro/docs/internet.svg
```

```md
category: Fundamentals
categoryName: History
categoryDescription: History demo
categoryOrder: 20
categoryIcon: https://img.solarspace.pro/docs/internet.svg
```

- Добавим заголовок страницы `seoTitle`.

```md
seoTitle: История
```

```md
seoTitle: History
```

- Добавим содержимое статьи:

```md
# Блок истории

Пример отображения статьи в блоке истории и на главной странице.
```

```md
# History Block

An example of a documentation article shown in the viewing history and homepage category.
```

---

По результатам получим:

- в `ru/guides/advanced/history.md`

```md
---
id: 1003
displayName: История
order: 10
published: true
historyName: История
historyDescription: Пример блока истории
category: Основы
categoryName: История
categoryDescription: Демонстрация истории
categoryOrder: 20
categoryIcon: https://img.solarspace.pro/docs/internet.svg
seoTitle: История
---

# Блок истории

Пример отображения статьи в блоке истории и на главной странице.
```

- в `en/guides/advanced/history.md`

```md
---
id: 1003
displayName: History
order: 10
published: true
historyName: History
historyDescription: History block example
category: Fundamentals
categoryName: History
categoryDescription: History demo
categoryOrder: 20
categoryIcon: https://img.solarspace.pro/docs/internet.svg
seoTitle: History
---

# History Block

An example of a documentation article shown in the viewing history and homepage category.
```



Вот оформленный раздел для **Статьи 4: Завершение / Summary**, аналогично предыдущим:

---

### [Статья 4: Завершение / Summary](article-4)

Создадим два файла:

```
/ru/guides/advanced/summary.md
/en/guides/advanced/summary.md
```

Пошаговое добавление мета-свойств:

* Укажем уникальный `id`, одинаковый для обоих языков.

```md
id: 1004
```

* Название статьи `displayName`.

```md
displayName: Завершение
```

```md
displayName: Summary
```

* Порядок отображения статьи в разделе `order`.

```md
order: 20
```

* Флаг публикации `published`.

```md
published: true
```

* Отображение в подвале сайта:

  * название ссылки `footerName`;
  * порядок отображения `footerOrder`.

```md
footerName: Завершение
footerOrder: 10
```

```md
footerName: Summary
footerOrder: 10
```

* Исключение статьи из других интерфейсов с помощью `ignoreInterfaces`:

```md
ignoreInterfaces:
  - menu
  - header
  - history
  - category
```

* Дополнительно можно указать `historyName` и `historyDescription` (хотя статья не будет отображаться в истории — это сохраняет консистентность структуры).

```md
historyName: Завершение
historyDescription: Заключительная статья
```

```md
historyName: Summary
historyDescription: Final article
```

* SEO-заголовок страницы `seoTitle`.

```md
seoTitle: Завершение
```

```md
seoTitle: Summary
```

* Содержимое статьи:

```md
# Завершение

Спасибо за ознакомление с документацией! Здесь может быть размещён финальный призыв к действию.
```

```md
# Summary

Thanks for reading the documentation! This could be a final call to action.
```

По результатам получим:

* в `ru/guides/advanced/summary.md`

```md
---
id: 1004
displayName: Завершение
order: 20
published: true
footerName: Завершение
footerOrder: 10
ignoreInterfaces:
  - menu
  - header
  - history
  - category
historyName: Завершение
historyDescription: Заключительная статья
seoTitle: Завершение
---

# Завершение

Спасибо за ознакомление с документацией! Здесь может быть размещён финальный призыв к действию.
```

* в `en/guides/advanced/summary.md`

```md
---
id: 1004
displayName: Summary
order: 20
published: true
footerName: Summary
footerOrder: 10
ignoreInterfaces:
  - menu
  - header
  - history
  - category
historyName: Summary
historyDescription: Final article
seoTitle: Summary
---

# Summary

Thanks for reading the documentation! This could be a final call to action.
```


## [Результат](result)

В конечном итоге проект имеет следующую файловую структуру:

```
/content/
  ├── en/
  |    └── guides/
  |         ├── contacts.md
  |         ├── basic/
  |         |     ├── intro.md
  |         |     └── metadata.md
  |         ├── advanced/
  |         |     ├── history.md
  |         |     ├── summary.md
  |         |     └── metadata.md
  |         └── metadata.md
  └── ru/
       └── guides/
            ├── contacts.md
            ├── basic/
            |     ├── intro.md
            |     └── metadata.md
            ├── advanced/
            |     ├── history.md
            |     ├── summary.md
            |     └── metadata.md
            └── metadata.md
```


Интерфейс будет выглядеть следующим образом:
- Меню:

```
  ├── (Основы / Basics)
  |     └── (Введение / Introduction)
  └── (Продвинутые темы / Advanced)
        └── (История / History)
```

- Шапка сайта (ru/en):
  - Введение / Introduction
  - Контакты / Contacts

- Подвал сайта (ru/en):
  - Введение / Introduction
  - Завершение / Summary

- Главная страница (ru/en):
  - Категория "Начало работы" / "Getting Started":
    - Введение / Introduction
  - Категория "Основы" / "Fundamentals":
    - История / History

- История посещений (ru/en):
  - Введение / Introduction
  - История / History

    

## [Рекомендации](recommendations)

- Используйте **одинаковый `id`** для каждой пары статей на разных языках — это обеспечит корректные короткие ссылки и историю посещений.
- Всегда заполняйте **обязательные мета-свойства** (`id`, `published`, `displayName`, `order`, `historyName`, `historyDescription`, `seoTitle`).
- Управляйте отображением статьи в интерфейсе с помощью **`ignoreInterfaces`** — удобно для скрытых страниц вроде "Контакты".
- Проверяйте, что категории статьи (`category`) соответствуют списку `categories` в языковом `metadata.md`.
- Поддерживайте **симметрию структуры** между языками: одинаковые директории, названия файлов и `id`.
- Используйте **разные значения `order`** в рамках одной директории, чтобы избежать конфликтов сортировки.


## [Заключение](conclusion)

Теперь вы умеете создавать статьи, настраивать их мета-свойства и управлять отображением в различных элементах
интерфейса — меню, шапке, подвале, главной странице и истории посещений. Вы также научились синхронизировать статьи
между языками, формируя полноценную мультиязычную структуру документации. Этот шаг завершает базовую настройку
документационного проекта.


## [Дополнительные ресурсы](additional-resources)

### По мета-свойствам:

- [Подробное описание мета свойства `id`]([44])
- [Подробное описание мета свойства `displayName`]([37])
- [Подробное описание мета свойства `order`]([45])
- [Подробное описание мета свойства `published`]([46])
- [Подробное описание мета свойства `historyName`]([43])
- [Подробное описание мета свойства `historyDescription`]([42])
- [Подробное описание мета свойства `categories`]([30])
- [Подробное описание мета свойства `category`]([31])
- [Подробное описание мета свойства `categoryDescription`]([32])
- [Подробное описание мета свойства `categoryIcon`]([33])
- [Подробное описание мета свойства `categoryName`]([34])
- [Подробное описание мета свойства `categoryOrder`]([35])
- [Подробное описание мета свойства `headerName`]([40])
- [Подробное описание мета свойства `headerOrder`]([41])
- [Подробное описание мета свойства `footerName`]([38])
- [Подробное описание мета свойства `footerOrder`]([39])
- [Подробное описание мета свойства `ignoreInterfaces`]([54])
- [Подробное описание мета свойства `seoTitle`]([59])

### По элементам интерфейса:

- [Подробное описание меню документации]([10])
- [Подробное описание шапки сайта]([7])
- [Подробное описание подвала сайта]([6])
- [Подробное описание блоков главной страницы]([9])
- [Подробное описание блока истории посещений]([8])
