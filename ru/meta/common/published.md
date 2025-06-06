---
id: 46
displayName: published
order: 50
published: true
historyName: Описание мета свойства published
historyDescription: Мета-свойство published контролирует видимость статьи или раздела в меню, шапке и на главной странице документации.
seoTitle: Описание published - Общее - Мета свойства
---

# Свойство published

**Мета свойство:** `published`

**Тип данных:** Логическое значение

**Возможные значения:**  `true` или `false`


## [Описание](description)

Мета свойство `published` используется для управления видимостью разделов и статей в сгенерированной документации. Оно определяет, будут ли соответствующие
разделы или статьи отображаться в различных элементах пользовательского интерфейса, таких как меню, шапка, подвал и главная страница.


### [Основные функции](basic-functions)

- **Управление отображением в меню:** Если `published` установлено в `true`, раздел или статья отображаются в меню. Если `false` или свойство отсутствует, элемент не отображается.
- **Контроль видимости в шапке и подвале:** Для статей `published` влияет на отображение ссылок в шапке и подвале сайта.
- **Исключение из главной страницы:** Статьи с `published: false` не отображаются в секциях на главной странице, даже если указаны `category` и связанные свойства.
- **Скрытие от пользователей:** Позволяет скрывать определённые разделы или статьи от пользователей без их удаления из файловой структуры.


### [Как работает вместе с другими мета свойствами](with-other-properties)

- **С `displayName`:** Если `published: false`, значение `displayName` не отображается в меню и хлебных крошках.
- **С `headerName` и `headerOrder`:** Даже если эти свойства указаны, статья не появится в шапке, если `published: false`.
- **С `footerName` и `footerOrder`:** Аналогично, статья не будет отображаться в подвале при `published: false`.
- **С `category` и связанными свойствами:** Статьи с `published: false` не будут отображаться в соответствующих секциях на главной странице.
- **С вложенными элементами:** Если раздел имеет `published: false`, все его вложенные разделы и статьи также не будут отображаться, независимо от их собственных свойств `published`.


### [Важные замечания](notes)

- **По умолчанию:** Если свойство `published` отсутствует, считается, что оно имеет значение `false`, и элемент не будет отображаться.
- **Влияние на навигацию:** Элементы с `published: false` не появляются в меню, шапке, подвале и на главной странице, но могут быть доступны по прямой ссылке.


### [Когда следует использовать](when-to-use)

- **В процессе разработки:** При создании новых разделов или статей, которые ещё не готовы для общего доступа.
- **Для снятия с публикации:** Когда нужно временно или постоянно скрыть материал от пользователей.
- **Для внутренних документов:** Если существуют статьи или разделы, предназначенные только для внутреннего использования и не должны быть видимы пользователям.


### [Советы по использованию](advice)

- **Управление контентом:** Используйте `published: false` для управления видимостью материалов без их удаления.
- **Рабочий процесс:** Включайте `published: false` в качестве части процесса создания и рецензирования новых материалов.
- **Согласованность:** Обеспечьте согласованное использование `published` по всей документации для упрощения управления контентом.
- **Явное указание:** Рекомендуется всегда явно указывать `published: true` или `published: false` для ясности.
- **Проверка вложенности:** Помните, что `published: false` у раздела скрывает все вложенные элементы, независимо от их собственных настроек.
- **Обновление статуса:** Не забывайте менять значение `published` на `true` при готовности материала к публикации.


## [Заключение](conclusion)

Мета свойство `published` является ключевым инструментом для контроля видимости разделов и статей в документации. Оно позволяет гибко управлять контентом,
обеспечивая показ пользователям только актуальной и готовой к использованию информации. Правильное использование `published` улучшает качество документации.


## [Примеры использования](examples)

### Пример 1: Скрытие раздела из меню

**Файл `metadata.md` для раздела:**

```md
---
displayName: Черновики
order: 99
published: false
---
```

- **Результат:** Раздел "Черновики" и все его содержимое не будут отображаться в меню и навигации.

### Пример 2: Скрытие статьи из всех элементов интерфейса

**Статья `upcoming-features.md`:**

```md
---
seoTitle: Будущие возможности
displayName: Будущие возможности
order: 10
published: false
category: start
categoryName: Скоро в версии 2.0
categoryDescription: Предварительный обзор новых функций
categoryOrder: 1
categoryIcon: /icons/coming-soon.svg
headerName: Будущие возможности
headerOrder: 50
footerName: Будущие возможности
footerOrder: 50
---
# Будущие возможности

*Эта статья находится в разработке и будет опубликована в ближайшее время.*
```

- **Результат:** Статья "Будущие возможности" не будет отображаться ни в меню, ни в шапке, ни в подвале, ни на главной странице.

---
