---
id: 18
displayName: Заголовки
order: 10
published: true
historyName: Заголовки
historyDescription: Использование в Markdown-разметки
seoTitle: Заголовки - Markdown-разметка
---

# Заголовки
В данном разделе рассмотрены заголовки и как их использовать.


## [Описание](description)
Существует 6 уровней заголовков:

| MD разметка | Преобразуется в HTML | Описание           |
|:------------|:---------------------|:-------------------|
| #           | h1                   | Заголовок 1 уровня |
| ##          | h2                   | Заголовок 2 уровня |
| ###         | h3                   | Заголовок 3 уровня |
| ####        | h4                   | Заголовок 4 уровня |
| #####       | h5                   | Заголовок 5 уровня |
| ######      | h6                   | Заголовок 6 уровня |


## [Заголовки в оглавлении](heading-in-table-of-contents)
Для создания заголовка который будет добавлен в оглавление в заголовок нужно добавить ссылку. При этом если помимо ссылки будет
присутствовать другая разметка, то она не будет учитываться.

Схема построения заголовка связанного с оглавлением:
```md
# [Контент отображаемый в заголовке](ссылка-на-заголовок "Название в оглавлении")
```

- `Контент отображаемый в заголовке` будет виден в качестве заголовка после генерации контента;
- `ссылка-на-заголовок` будет использоваться для навигации на неё и также будет меняться hash в URL при прокрутке до заголовка;
- `Название в оглавлении` - не обязательная часть. Используется в оглавлении для отображения отличного от контентного заголовка.
Если его опустить, то в оглавлении отобразится `Контент отображаемый в заголовке`. **Максимальное количество символов:** `50`


## [Применение](using)
На странице может быть только 1 заголовок 1-го уровня, иначе оглавление страницы будет формироваться некорректно.
Если какой-то заголовок не нужно отображать в оглавлении, то вместо:
```
# [Контент отображаемый в заголовке](ссылка-на-заголовок "Название в оглавлении")
```
можно использовать:
```
# Контент отображаемый в заголовке
```
При этом заголовок может быть любого уровня.


## Пример использования

```
## Заголовок 2
### Заголовок 3
#### Заголовок 4
##### Заголовок 5
###### Заголовок 6
```


## Результат

## Заголовок 2
### Заголовок 3
#### Заголовок 4
##### Заголовок 5
###### Заголовок 6
