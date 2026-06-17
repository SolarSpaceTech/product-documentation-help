---
id: 21
displayName: Изображения
order: 110
published: true
historyName: Изображения
historyDescription: Использование в Markdown-разметки
seoTitle: Изображения - Markdown-разметка
---

# Изображения
В этом разделе рассмотрены изображения и как их использовать.


## Описание
Для создания изображения используют синтаксис:
```md
![Название изображения (ширина:высота|позиционирование)](путь/до/превью|путь/до/изображения "Скрытый текст изображения")
```
- `Название изображения` это отображаемый текст, который увидит пользователь в случае, если произойдёт ошибка загрузки изображения;
- `ширина` - ширина изображения, можно задавать любую css единицу измерения (по умолчанию изображение растягивается на всю ширину);
- `высота` - высота изображения, можно задавать любую css единицу измерения (по умолчанию изображение учитывает пропорции
в соответствии с высотой и исходным изображением)
- `позиционирование` - может принимать значения:
    - `left`(по умолчанию) - помещает изображение слева без возможности обтекания текста справа.
    - `inline-left` - прижимает изображение слева и заставляет текст обтекать справа.
    - `right` - помещает изображение справа без возможности обтекания текста слева.
    - `inline-right` - прижимает изображение справа и заставляет тест обтекать слева.
    - `center` - помещает изображение по центру без возможности обтекания текста слева и справа.
- `путь/до/превью` это url до уменьшенной версии изображения;
- `путь/до/изображение` это url до полной версии изображения;
- `Скрытый текст изображения` это текст который будет показываться при наведении на изображение.


## Пример использования
```md
![image (25%)](https://img.solarspace.pro/docs/docs_img/1600x2500.png|https://img.solarspace.pro/docs/docs_img/800x1250.png "Some text")

![image (25%|inline-right)](https://img.solarspace.pro/docs/docs_img/1600x2500.png "Some text")
Lorem ipsum dolor sit amet, consectetur adipisicing elit. Neque, nostrum veritatis! Architecto beatae delectus eum exercitationem illum laboriosam nemo quas.
Lorem ipsum dolor sit amet, consectetur adipisicing elit. Neque, nostrum veritatis! Architecto beatae delectus eum exercitationem illum laboriosam nemo quas.


![image (25%|right)](https://img.solarspace.pro/docs/docs_img/1600x2500.png "Some text")
Lorem ipsum dolor sit amet, consectetur adipisicing elit. Neque, nostrum veritatis! Architecto beatae delectus eum exercitationem illum laboriosam nemo quas.
Lorem ipsum dolor sit amet, consectetur adipisicing elit. Neque, nostrum veritatis! Architecto beatae delectus eum exercitationem illum laboriosam nemo quas.


Lorem ipsum dolor sit amet, consectetur adipisicing elit. Neque, nostrum veritatis! Architecto beatae delectus eum exercitationem illum laboriosam nemo quas.
![image (25%|inline-left)](https://img.solarspace.pro/docs/docs_img/1600x2500.png "Some text")
Lorem ipsum dolor sit amet, consectetur adipisicing elit. Neque, nostrum veritatis! Architecto beatae delectus eum exercitationem illum laboriosam nemo quas.


Lorem ipsum dolor sit amet, consectetur adipisicing elit. Neque, nostrum veritatis! Architecto beatae delectus eum exercitationem illum laboriosam nemo quas.
![image (25%|left)](https://img.solarspace.pro/docs/docs_img/1600x2500.png "Some text")
Lorem ipsum dolor sit amet, consectetur adipisicing elit. Neque, nostrum veritatis! Architecto beatae delectus eum exercitationem illum laboriosam nemo quas.


Lorem ipsum dolor sit amet, consectetur adipisicing elit. Neque, nostrum veritatis! Architecto beatae delectus eum exercitationem illum laboriosam nemo quas.
![image (50%|center)](https://img.solarspace.pro/docs/docs_img/1600x2500.png "Some text")
Lorem ipsum dolor sit amet, consectetur adipisicing elit. Neque, nostrum veritatis! Architecto beatae delectus eum exercitationem illum laboriosam nemo quas.


Lorem ipsum dolor sit amet, consectetur adipisicing elit. Neque, nostrum veritatis! Architecto beatae delectus eum exercitationem illum laboriosam nemo quas.
![image](https://img.solarspace.pro/docs/docs_img/1600x2500.png "Some text")
Lorem ipsum dolor sit amet, consectetur adipisicing elit. Neque, nostrum veritatis! Architecto beatae delectus eum exercitationem illum laboriosam nemo quas.
```


## Результат

![image (25%)](https://img.solarspace.pro/docs/docs_img/800x1250.png "Some text")

![image (25%|inline-right)](https://img.solarspace.pro/docs/docs_img/1600x2500.png "Some text")
Lorem ipsum dolor sit amet, consectetur adipisicing elit. Neque, nostrum veritatis! Architecto beatae delectus eum exercitationem illum laboriosam nemo quas.
Lorem ipsum dolor sit amet, consectetur adipisicing elit. Neque, nostrum veritatis! Architecto beatae delectus eum exercitationem illum laboriosam nemo quas.


![image (25%|right)](https://img.solarspace.pro/docs/docs_img/1600x2500.png "Some text")
Lorem ipsum dolor sit amet, consectetur adipisicing elit. Neque, nostrum veritatis! Architecto beatae delectus eum exercitationem illum laboriosam nemo quas.
Lorem ipsum dolor sit amet, consectetur adipisicing elit. Neque, nostrum veritatis! Architecto beatae delectus eum exercitationem illum laboriosam nemo quas.


Lorem ipsum dolor sit amet, consectetur adipisicing elit. Neque, nostrum veritatis! Architecto beatae delectus eum exercitationem illum laboriosam nemo quas.
![image (25%|inline-left)](https://img.solarspace.pro/docs/docs_img/1600x2500.png "Some text")
Lorem ipsum dolor sit amet, consectetur adipisicing elit. Neque, nostrum veritatis! Architecto beatae delectus eum exercitationem illum laboriosam nemo quas.


Lorem ipsum dolor sit amet, consectetur adipisicing elit. Neque, nostrum veritatis! Architecto beatae delectus eum exercitationem illum laboriosam nemo quas.
![image (25%|left)](https://img.solarspace.pro/docs/docs_img/1600x2500.png "Some text")
Lorem ipsum dolor sit amet, consectetur adipisicing elit. Neque, nostrum veritatis! Architecto beatae delectus eum exercitationem illum laboriosam nemo quas.


Lorem ipsum dolor sit amet, consectetur adipisicing elit. Neque, nostrum veritatis! Architecto beatae delectus eum exercitationem illum laboriosam nemo quas.
![image (50%|center)](https://img.solarspace.pro/docs/docs_img/1600x2500.png "Some text")
Lorem ipsum dolor sit amet, consectetur adipisicing elit. Neque, nostrum veritatis! Architecto beatae delectus eum exercitationem illum laboriosam nemo quas.


Lorem ipsum dolor sit amet, consectetur adipisicing elit. Neque, nostrum veritatis! Architecto beatae delectus eum exercitationem illum laboriosam nemo quas.
![image](https://img.solarspace.pro/docs/docs_img/1600x2500.png "Some text")
Lorem ipsum dolor sit amet, consectetur adipisicing elit. Neque, nostrum veritatis! Architecto beatae delectus eum exercitationem illum laboriosam nemo quas.
