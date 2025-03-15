# Проект API Yatube
***
## Описание
CRUD для Yatube.

API доступен только аутентифицированным пользователям. Аутентификация реализована по токену TokenAuthentication. Аутентифицированный пользователь авторизован на изменение и удаление своего контента, в остальных случаях доступ предоставляется только для чтения.
***
## Функционал
- Получение токенов доступа.
- Чтение/Публикация/Редакция/Удаление записей и комментариев.
***
# Endpoints

- **api/v1/api-token-auth/** - (POST): Передаём логин и пароль, получаем токен.
- **api/v1/posts/** - (GET, POST): Получаем список всех постов или создаём новый пост.
- **api/v1/posts/{post_id}/** - (GET, PUT, PATCH, DELETE): Получаем, редактируем или удаляем пост по id.
- **api/v1/groups/** - (GET): Получаем список всех групп.
- **api/v1/groups/{group_id}/** - (GET): Получаем информацию о группе по id.
- **api/v1/posts/{post_id}/comments/** - (GET, POST): Получаем список всех комментариев поста с id=post_id или создаём новый, указав id поста, который хотим прокомментировать.
- **api/v1/posts/{post_id}/comments/{comment_id}/** - (GET, PUT, PATCH, DELETE): Получаем, редактируем или удаляем комментарий по id у поста с id=post_id.
***
## Запуск проекта в dev-режиме
* Установите и активируйте виртуальное окружение
```sh
cd api_yatube
python3 -m venv venv
source venv/bin/activate
```
* Установите зависимости из файла requirements.txt
```sh
pip install -r requirements.txt
```
* Выполнить миграции:
```sh
python3 manage.py migrate
```
* Запустить проект:
```sh
python3 manage.py runserver
```
***

