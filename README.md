# API для социальной сети Yatube123456

## Описание

API для соцсети блогеров Yatube.Проект реализован на REST API DJANGO.
  
#### Доступный функционал

- Для аутентификации используются JWT-токены.
- У неаутентифицированных пользователей доступ к API только на уровне чтения.
- Для эндпойнта /follow/ установлено дополнительное ограничение.Доступ к нему только у аутентифицированных пользователей.
- Аутентифицированным пользователям разрешено изменение и удаление своего контента, в остальных   случаях доступ предоставляется только для чтения.
- Подписки на пользователей.
- Просмотр, создание, изменение и удаление записей.
- Просмотр и создание групп.
- Возможность добавления, редактирования, удаления своих комментариев и просмотр чужих.
- Фильтрация по полям.

#### Документация к API доступна по адресу [http://127.0.0.1:8000/redoc/](http://127.0.0.1:8000/redoc/) после запуска сервера с проектом

#### Технологии

- Python 3.7
- Django 2.2.16
- Django Rest Framework 3.12.4
- Djoser 
- Simple JWT
- SQLite3

#### Запуск проекта в dev-режиме

- Склонируйте репозиторий:  
``` git clone <название репозитория> ```    
- Установите и активируйте виртуальное окружение:  
``` python -m venv venv ```  
``` source venv/Scripts/activate ``` 
- Установите зависимости из файла requirements.txt:   
``` pip install -r requirements.txt ```
- Перейдите в папку api_yatube/yatube_api.
- Примените миграции:   
``` python manage.py migrate ```
- Выполните команду:   
``` python manage.py runserver ```

#### Примеры некоторых запросов API

Получить список всех постов:  
``` GET /api/v1/posts/ ```  
Добавление нового поста:  
``` POST /api/v1/posts/ ```   
Получить список всех групп:  
``` GET /api/v1/groups/ ```  
Добавление нового комментария:  
``` POST /api/v1/posts/{post_id}/comments/ ```  
Удаление комментария по id:  
``` DELETE /api/v1/posts/{post_id}/comments/{id}/ ```  
Получение списока подписок:  
``` GET /api/v1/follow/ ```  
Подписка пользователя на пользователя переданного в запросе:  
``` POST /api/v1/follow/ ```    

#### Полный список запросов API находятся в документации

#### Автор

Гут Владимир
