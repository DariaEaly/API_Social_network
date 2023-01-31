# ![Logo](yatube_api\static\favicon-32x32.png) api_yatube_project

## Описание

Проект Yatube, теперь и с API!
Теперь в нем появилась возможность с помощью запросов к API получать посты и группы, авторизовываться и публиковать новые посты, подписываться на любимых авторов.

## Технологии

**Python:** 3.7

**Django:** 2.2.19  


## Запуск проекта в dev-режиме

- Установите и активируйте виртуальное окружение
    ```
    python -m venv venv
    source venv/Scripts/activate
    ```
- Установите зависимости из файла requirements.txt
    ```
    pip install -r requirements.txt
    ```
- В папке с файлом manage.py выполните миграции:
    ```
    python manage.py migrate
    ```
- Запустите сервер:
    ```
    python manage.py runserver
    ```
    

## Автор

- [Дарья](https://github.com/DariaEaly)
