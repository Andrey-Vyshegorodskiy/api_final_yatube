# api_final
api final

Описание: API к проекту Yatube.

Yatube - это сайт, для публикации личных дневников. Можно создать свою страницу, если на нее зайти можно посмотреть все записи автора. Пользователи смогут заходить на чужие страницы, подписываться на авторов и комментировать их записи.

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


для развертывания - склонируйте приложение api_final

Cоздать и активировать виртуальное окружение:


python3 -m venv env



source env/bin/activate



python3 -m pip install --upgrade pip


Установить зависимости из файла requirements.txt:


pip install -r requirements.txt


Выполнить миграции:


python3 manage.py migrate


Запустить проект:


python3 manage.py runserver
