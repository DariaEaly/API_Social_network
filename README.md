# ![Logo](yatube_api\static\favicon-32x32.png) api_yatube_project

## Описание

Проект Yatube, теперь и с API!
Теперь в нем появилась возможность с помощью запросов к API получать посты и группы, авторизовываться и публиковать новые посты, подписываться на любимых авторов.

## Технологии

**Python:** 3.7

**Django:** 2.2.19  

## Запуск проекта в dev-режиме

- Установите и активируйте виртуальное окружение

    ```bash
    python -m venv venv
    source venv/Scripts/activate
    ```

- Установите зависимости из файла requirements.txt

    ```bash
    pip install -r requirements.txt
    ```

- В папке с файлом manage.py выполните миграции:

    ```bash
    python manage.py migrate
    ```

- Запустите сервер:

    ```bash
    python manage.py runserver
    ```

## Примеры запросов к API

- Создайте пользователя

    ```bash
    curl -X POST -H "Content-Type: application/json" -d '{"username": "MyUsername",
    "password": "MySecretPsW:)"}' "http://127.0.0.1:8000/api/v1/auth/users/"
    ```

- Получите токен

    ```bash
    curl -X POST -H "Content-Type: application/json" -d '{"username": "username",
    "password": "MySecretPsW:)"}' "http://127.0.0.1:8000/api/v1/jwt/create"
    ```

- Напишите пост

    ```bash
    curl -X POST -H "Content-Type: application/json" -H "Authorization: Bearer {Your access Token}" -d '{"text": "My first post"}' "http://127.0.0.1:8000/api/v1/posts/"
    ```

- Получите пост:

    ```bash
    curl -X GET "http://127.0.0.1:8000/api/v1/posts/1"
    ```

- Удалите пост

    ```bash
    curl -X DELETE -H "Authorization: Bearer {Your access Token}" "http://127.0.0.1:8000/api/v1/posts/1"
    ```

## Автор

- [Дарья](https://github.com/DariaEaly)
