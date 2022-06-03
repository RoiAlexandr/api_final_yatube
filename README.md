Описание
API для взаимодействия с YaTube (https://github.com/RoiAlexandr/hw05_final.git ) проект.

Автор
Рой Александр

### Как запустить проект:

Клонировать репозиторий и перейти в него в командной строке:

```
git clone https://github.com/RoiAlexandr/api_final_yatube.git
```

```
cd api_final_yatube

```

Cоздать и активировать виртуальное окружение:

```
python3 -m venv env
```

```
source env/bin/activate
```

```
python3 -m pip install --upgrade pip
```

Установить зависимости из файла requirements.txt:

```
pip install -r requirements.txt
```

Выполнить миграции:

```
python3 manage.py migrate
```

Запустить проект:

```
python3 manage.py runserver
```



Примеры запросов API

Получение публикаций
```
GET /api/v1/posts/
```
Образец ответа
```

{
    "id": 0,
    "author": "string",
    "text": "string",
    "pub_date": "2019-08-24T14:15:22Z",
    "image": "string",
    "group": 0
}
```
Создание публикации
```
POST /api/v1/posts/
```
Образец запроса
```
}
    "text": "string",
    "image": "string",
    "group": 0
}
```
Образец ответа
```
{
    "id": 0,
    "author": "string",
    "text": "string",
    "pub_date": "2019-08-24T14:15:22Z",
    "image": "string",
    "group": 0
}
```
Обновление публикации
```
PUT /api/v1/posts/{id}/
```
Образец запроса
```
{
    "text": "stringstring",
    "image": "string",
    "group": 0
}
```
Образец ответа
```
{
    "id": 0,
    "author": "stringstring",
    "text": "string",
    "pub_date": "2019-08-24T14:15:22Z",
    "image": "string",
    "group": 0
}
```

Образец запроса
```
{
    "text": "anotherstring"
}
```
Образец ответа
```
{
    "id": 0,
    "author": "stringstring",
    "text": "anotherstring",
    "pub_date": "2019-08-24T14:15:22Z",
    "image": "string",
    "group": 0
}
```
Удаление публикации
```
DELETE /api/v1/posts/{id}/
```
Получение комментариев
```
GET /api/v1/posts/{post_id}/comments/
```
Образец ответа
```
[
    {
        "id": 0,
        "author": "string",
        "text": "string",
        "created": "2019-08-24T14:15:22Z",
        "post": 0
    }
]
```
Добавление комментария
```
POST /api/v1/posts/{post_id}/comments/
```
Образец запроса
```
{
    "text": "string"
}
```
Образец ответа
```
{
    "id": 0,
    "author": "string",
    "text": "string",
    "created": "2019-08-24T14:15:22Z",
    "post": 0
}
```
Получить JWT-токен
```
POST /api/v1/jwt/create/
```
Образец запроса
```
{
    "username": "string",
    "password": "string"
}
```
Образец ответа
```
{
    "refresh": "string",
    "access": "string"
```
