---
id: 37
title: Описание displayName - Общее - Мета свойства
displayName: displayName
order: 30
published: true
historyName: Описание мета свойства displayName
historyDescription: Мета-свойство displayName задает краткое название статьи для отображения в меню и навигации документации.
---

# Свойство displayName

**Мета свойство:** `displayName`

**Тип данных:** Строка

**Максимальное количество символов:** `40`

**Область влияния:**
![Влияние cвойства](https://raw.githubusercontent.com/SolarSpaceTech/product-documentation-help/refs/heads/main/ru/images/display-name.png)


<br/>

## [Описание](description)

Мета свойство `displayName` используется для задания названия статьи или раздела, которое будет отображаться в элементах навигации документации,
таких как меню и хлебные крошки. Это свойство играет ключевую роль в организации и представлении документации, помогая пользователям быстро
ориентироваться и находить нужные разделы или статьи.

<br/>

### [Основные функции](basic-functions)

- **Отображение в меню:** Значение `displayName` используется в качестве названия пункта меню для соответствующей статьи или раздела, позволяя
пользователям видеть понятные и удобные названия при навигации по документации.
- **Хлебные крошки:** В хлебных крошках, которые показывают путь пользователя через структуру документации, `displayName` отображается на каждом
уровне, предоставляя ясное представление о текущем местоположении.
- **Организация структуры:** Помогает структурировать документацию, обеспечивая логичные и последовательные названия разделов и статей.

<br/>

### [Как работает вместе с другими мета свойствами](with-other-properties)

- **`title`:** В то время как `title` отображается на вкладке браузера и может быть более подробным или содержать дополнительные детали,
`displayName` обычно короче и предназначен для быстрого восприятия в элементах навигации.
- **`order`:** Определяет порядок отображения статьи или раздела в меню, но не влияет на `displayName`.
- **`published`:** Определяет, будет ли статья или раздел отображаться в меню и других навигационных элементах. Если `published` установлено
в `false`, элемент не будет отображаться, независимо от значения `displayName`.
- **`headerName` и `footerName`:** Используются для отображения названия статьи в шапке и подвале сайта соответственно, могут отличаться от `displayName`.
- **`historyName`:** Используются для отображения названия статьи в блоке истории, может отличаться от `displayName`.
- **`categoryName`:** Используются для отображения названия статьи одной из секций со статьями на главной странице, может отличаться от `displayName`.

<br/>

### [Важные замечания](notes)

- **Краткость и ясность:** Рекомендуется использовать короткие и понятные названия в `displayName`, чтобы облегчить навигацию
и улучшить пользовательский опыт.
- **Согласованность:** Сохраняйте единый стиль написания `displayName` по всей документации для профессионального вида и удобства использования.
- **Уникальность:** Убедитесь, что каждое значение `displayName` уникально в контексте родительского раздела, чтобы избежать путаницы.

<br/>

### [Когда следует использовать](when-to-use)

- **Всегда при создании статьи или раздела:** Это основное свойство для отображения названия в меню и хлебных крошках.
- **Для упрощения навигации:** Когда необходимо предоставить пользователям понятные и лаконичные названия для быстрого доступа к разделам документации.
- **Для сокращения длинных названий:** Если `title` слишком длинный или содержит детали, не нужные в меню, `displayName` может быть использован для предоставления краткой версии.

<br/>

### [Советы по использованию](advice)

- **Используйте понятные термины:** Названия должны быть интуитивно понятными для целевой аудитории.
- **Избегайте избыточности:** Не включайте в `displayName` ненужные слова или фразы.
- **Следуйте стилю документации:** Используйте единый регистр и форму написания (например, все названия в единственном числе).
- **Краткость:** Старайтесь, чтобы название было коротким, обычно не более 2-3 слов.
- **Информативность:** Название должно точно отражать содержание раздела или статьи.
- **Последовательность:** Используйте одинаковый стиль написания по всей документации (например, все названия в повелительном наклонении
  или в форме существительных).

<br/>

## [Заключение](conclusion)

Мета свойство `displayName` является важным элементом при генерации документации, так как оно напрямую влияет на то, как пользователи будут
навигировать по вашему сайту. Правильное и продуманное использование `displayName` улучшает удобство использования документации, делая ее более
доступной и понятной для пользователей.

<br/>

## [Примеры использования](examples)

### Пример 1: Статья о настройке окружения

```md
---
title: Настройка окружения разработки для проекта
displayName: Настройка окружения
order: 2
published: true
---
# Настройка окружения разработки

В этом разделе описывается, как настроить окружение для разработки нашего проекта...
```

- **`displayName`:** "Настройка окружения" будет отображаться в меню и хлебных крошках, обеспечивая краткое и понятное название.
- **`title`:** "Настройка окружения разработки для проекта" будет отображаться на вкладке браузера, предоставляя более полное описание.

<br/>

### Пример 2: Раздел с несколькими подстатьями

**Файл `metadata.md` для раздела:**

```md
---
displayName: Руководства
order: 1
published: true
---
```

**Файл статьи `installation.md`:**

```md
---
title: Установка продукта — Пошаговое руководство
displayName: Установка
order: 1
published: true
---
# Установка продукта

Следуйте этим шагам для установки нашего продукта...
```

- **`displayName` раздела:** "Руководства" отображается в меню как название раздела.
- **`displayName` статьи:** "Установка" отображается как подэлемент в меню под разделом "Руководства".