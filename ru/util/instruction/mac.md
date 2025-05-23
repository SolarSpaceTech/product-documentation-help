---
id: 48
seoTitle: MacOS - Инструкция - Утилита
displayName: Для MacOS
order: 10
published: true
historyName: Инструкция к утилите для MacOS
historyDescription: Описание установки и обновления
---

# Инструкция по работе с утилитой на MacOS

Данная инструкция поможет вам установить и использовать утилиту на macOS.

1. Подготовка утилиты
    - **Получите утилиту**: Убедитесь, что у вас есть самораспаковывающийся скрипт pd для macOS. Он должен находиться 
   в той же директории, что и документация.
2. Организация директорий
   - **Расположение утилиты**: Убедитесь, что утилита `pd` находится на одном уровне с директорией документации.
   - **Переименуйте директорию документации**: Директория с документацией должна называться `content`.
   Если она называется иначе, переименуйте её в `content`.
   - **Примечание**: Хотя вы можете изменить путь к директории документации с помощью переменной `PD_CONTENT_DIR`
   в скрипте `pd`, рекомендуется просто переименовать директорию в `content`, так как при обновлениях установленное
   значение будет сбрасываться.

3. Настройка прав доступа
   - **Сделайте скрипт исполняемым**: По умолчанию утилита не является исполняемой. Откройте терминал и перейдите
   в директорию, где находится файл `pd`.
    ```bash
    chmod +x ./pd
    ```

4. Первый запуск утилиты
   - **Разархивация файлов**: При первом запуске утилиты будут созданы директории `bin` и `plugins`.
    ```bash
    sudo ./pd
    ```
    Убедитесь, что вы запускаете утилиту из той же директории, где находится скрипт `pd`.



## Последующие запуски

- **Оптимизация запуска**: При повторных запусках утилита не будет разархивировать директорию `bin` снова,
что ускоряет процесс запуска.
- **Обновление плагинов**: Директория `plugins` будет разархивироваться при каждом запуске. Это позволяет
обновлять существующие плагины и добавлять новые без необходимости переустановки всей утилиты.


## Обновление и добавление плагинов

- **Обновление утилиты**: Замените `pd` файл, удалите директории `bin` и `plugins`
- **Обновление плагинов**: Поместите новую версию плагина в директорию `plugins`.
- **Добавление новых плагинов**: Добавьте новый плагин в директорию `plugins`.


## Дополнительные примечания:

- **Права доступа**: Всегда запускайте утилиту с правами суперпользователя (sudo), чтобы избежать проблем с доступом
к файлам и директориям.
