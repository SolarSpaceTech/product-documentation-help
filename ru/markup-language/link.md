---
id: 25
displayName: Ссылки
order: 30
published: true
historyName: Ссылки
historyDescription: Примеры и правила использования ссылок в Markdown-разметке
seoTitle: Ссылки - Markdown-разметка
---

# Ссылки

Ссылки позволяют вставлять переходы на внешние и внутренние страницы, делая текст более интерактивным и структурированным.

## Описание

Синтаксис ссылок в Markdown предполагает размещение текста ссылки в квадратных скобках `[]`, а URL — в круглых скобках `()`.
Дополнительно можно указывать атрибут `rel`, который будет добавлен в HTML-вывод, через квадратные скобки внутри ссылки.

Также поддерживаются короткие ссылки на статьи, если у них указан `id` в мета-данных. Они задаются через `[Название ссылки]([id])`.

## Пример использования

```md
[Внешняя ссылка](https://example.com)

[Внешняя с атрибутом](https://example.com[nofollow])

[Внутренняя ссылка](/intro)

[Короткая ссылка]([42])
```

## Результат

- [Внешняя ссылка](https://example.com)
- [Внешняя с атрибутом](https://example.com[nofollow])
- [Внутренняя ссылка](/intro)
- Короткая ссылка, ведущая на статью с `id: 42`, например: [Короткая ссылка]([42])
