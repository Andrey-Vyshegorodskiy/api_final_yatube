# api_final
api final

Описание: API к проекту Yatube.

### Описание
API для Yatub представляет собой проект социальной сети в которой реализованы следующие возможности, 
публиковать записи, комментировать записи, а так же подписываться или отписываться от авторов.
### Технологии
Python 3.7, Django 3.2, DRF, JWT + Djoser
### Запуск проекта в dev-режиме
- Клонировать репозиторий и перейти в него в командной строке.
- Установите и активируйте виртуальное окружение c учетом версии Python 3.7 (выбираем python не ниже 3.7):
```bash
py -3.7 -m venv venv
venv/Scripts/activate
python -m pip install --upgrade pip
```
- Затем нужно установить все зависимости из файла requirements.txt
```bash
pip install -r requirements.txt
```
- Выполняем миграции:
```bash
python manage.py migrate
```
Создаем суперпользователя:
```bash
python manage.py createsuperuser
```
Запускаем проект:
```bash
python manage.py runserver
```
Функции API api_final
1. Получение публикаций GET http://127.0.0.1:8000/api/v1/posts/
2. Создание публикации POST http://127.0.0.1:8000/api/v1/posts/
3. Удаление публикаций DEL  http://127.0.0.1:8000/api/v1/posts/{id}/
4. Возможно обновление и частичное обновление публикаций (PUT и PATCH)

5. Получение комментариев GET http://127.0.0.1:8000/api/v1/posts/{post_id}/comments/
6. Добавление комментария POST http://127.0.0.1:8000/api/v1/posts/{post_id}/comments/
7. Добавление комментария POST http://127.0.0.1:8000/api/v1/posts/{post_id}/comments/{id}/
8. Удаление комментария DEL http://127.0.0.1:8000/api/v1/posts/{post_id}/comments/{id}/
9. Возможно обновление и частичное обновление публикаций (PUT и PATCH)

10. Получение списка сообществ GET http://127.0.0.1:8000/api/v1/groups/
11. Информация о сообществе GET http://127.0.0.1:8000/api/v1/groups/{id}/

12. Подписки на авторов (с поиском) GET http://127.0.0.1:8000/api/v1/follow/
13. Создание подписки на автора (по username) POST http://127.0.0.1:8000/api/v1/follow/

14. Получить JWT-токен POST http://127.0.0.1:8000/api/v1/jwt/create/
15. Обновить JWT-токен POST http://127.0.0.1:8000/api/v1/jwt/refresh/
16. Проверить JWT-токен POST http://127.0.0.1:8000/api/v1/jwt/verify/

Автор: [Андрей Вышегородский](https://github.com/Andrey-Vyshegorodskiy) :+1:
