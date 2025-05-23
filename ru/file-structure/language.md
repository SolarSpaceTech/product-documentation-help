---
id: 2
displayName: Новый язык
order: 20
published: true
historyName: Добавление нового языка
historyDescription: Подробное объяснение добавления нового языка на сайт, сохраняя структуру и корректно переводя контент.
seoTitle: Новый язык - Файловая структура
---

# Новый язык

Система документации поддерживает мультиязычность. Каждый язык оформляется как отдельная корневая директория,
содержащая `metadata.md`, статьи и структуру, идентичную другим языкам. Все языки отображаются в списке выбора, если они
опубликованы.


## [Основные функции](basic-functions)

- **Локализация интерфейса:** пользователь может выбрать язык отображения контента.
- **SEO-настройки по каждому языку:** уникальные `title`, `description`, `robots`.
- **Гибкое управление:** отдельные настройки, порядок и иконка для каждого языка.


## [Настройка с помощью мета свойств](customization-using-meta-properties)

Файл `metadata.md` в корневой папке языка содержит мета свойства:

```md
---
displayName: Русский
published: true
defaultLanguage: true
languageIcon: /assets/languages/ru.png
languageOrder: 10
categories:
  - Начало работы
  - Сервисы
  - Настройка ресурсов
---
````

* **`displayName`** — название языка в списке.
* **`published`** — если `false`, язык не отображается.
* **`defaultLanguage`** — один язык должен быть по умолчанию.
* **`languageIcon`** — иконка, отображаемая рядом с названием.
* **`languageOrder`** — порядок отображения в списке языков.
* **`categories`** — секции, отображаемые на главной странице.


## [Влияние мета свойств](impact-of-meta-properties)

* `published: false` — язык не будет отображаться.
* `defaultLanguage: true` — определяет URL без префикса языка.
* `languageOrder` — влияет на сортировку списка языков.
* `categories` — задают секции главной страницы конкретного языка.
* `seoRobots`, `verificationGoogle`, `verificationYandex` — задают поведение поисковых систем и верификацию.


## [Пошаговое руководство по настройке](step-by-step-setup-guide)

### Шаг 1: Создайте директорию языка

Например: `/fr` — для французского языка.

### Шаг 2: Вставьте в неё `metadata.md`

```md
---
displayName: Français
published: true
languageOrder: 30
languageIcon: /assets/languages/fr.png
categories:
  - Démarrage
  - Services
  - Configuration
---
```

### Шаг 3: Скопируйте структуру других языков

Все статьи должны быть с теми же путями и одинаковыми `id`.

### Шаг 4: Переведите содержимое и мета данные статей

Соблюдайте лимиты символов и используйте одинаковые идентификаторы `id`.


## [Рекомендации](recommendations)

* **Только один язык может быть `defaultLanguage: true`.**
* **Проверяйте, что структура файлов и `id` соответствуют другим языкам.**
* **Используйте нейтральные иконки — флаги, аббревиатуры.**
* **Сначала добавьте язык с `published: false`, чтобы протестировать.**


## [Пример использования](examples)

```md
---
displayName: English
published: true
defaultLanguage: false
languageOrder: 20
languageIcon: /assets/languages/en.png
categories:
  - Getting Started
  - Services
  - Resource Setup
---
```


## [Заключение](conclusion)

Добавление нового языка требует дублирования структуры, перевода контента и корректной настройки мета свойств
в `metadata.md`. Это позволяет пользователям легко переключаться между языками и обеспечивает соответствие
требованиям SEO и верификации.

