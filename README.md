
# API для Yatube

  

Реализация API в любой подходящий для этого сервис с целью получения информации о постах, для создания самих постов и т.п.

Для получения полной информации о проекте, разверните его у себя и пройдите по ссылке http://127.0.0.1:8000/redoc/

### Запуск проекта

1. Создайте и активируйте виртуальное окружение

- python3 -m venv venv

- source venv/bin/activate

2. Установите все необходимые пакеты из _requirements.txt_

- pip install -r requirements.txt

3. Выполните миграции

- python manage.py migrate

5. Запустить проект

- python3 manage.py runserver


### Примеры запросов

 
**1. Получение списка публикаций (GET) - /api/v1/posts/**

Ответ:

```
{
  "count": 123,
  "next": "http://api.example.org/accounts/?offset=400&limit=100",
  "previous": "http://api.example.org/accounts/?offset=200&limit=100",
  "results": [
    {
      "id": 0,
      "author": "string",
      "text": "string",
      "pub_date": "2021-10-14T20:41:29.648Z",
      "image": "string",
      "group": 0
    }
  ]
}

```

**2. Получение конкретной публикации (GET) - /api/v1/posts/{id}/**

Ответ:

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

**3. Создание публикации (POST) - /api/v1/posts/**

Ответ:

```
{
  "text": "string",
  "image": "string",
  "group": 0
}

```

**4. Получение комментариев (GET) - /api/v1/posts/{post_id}/comments/**

Ответ:

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

**5. Получение комментария (GET) - /api/v1/posts/{post_id}/comments/{id}/**

Ответ:

```
{
  "id": 0,
  "author": "string",
  "text": "string",
  "created": "2019-08-24T14:15:22Z",
  "post": 0
}
```

**6. Получение подписок (GET) - /api/v1/follow/**

Ответ:

```
  {
    "user": "string",
    "following": "string"
  }
```

**7. Подписка на пользователя (POST) - /api/v1/follow/**

Ответ:

```
{
  "following": "string"
}
```
Проект выполнен студентом курса Python-разработчик плюс Малявко    Татьяной
