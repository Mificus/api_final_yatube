# api_final
## Описание проекта
Проект API для социальной сети Yatube. Интерфейс, через которое могут работать 
мобильное приложение или чат-бот; через него же можно передавать 
данные в любое приложение или на фронтенд.

## Стек технологий
* Django Rest Framework  
* Python 3.10  
* Django 3.2.16  
* SQlite3
  
В проекте используютя модели:  
Post -  посты  
Group - группы  
Comment - комментарии для постов  
Follow -  управление подписками  

Документация по проекту после запуска сервера доступна по адресу:  
http://127.0.0.1:8000/redoc/  


### Как запустить проект:

Клонировать репозиторий и перейти в него в командной строке:

```
https://github.com/Mificus/api_final_yatube.git
```

```
cd api_final)yatube
```

Cоздать и активировать виртуальное окружение:

```
python3 -m venv env
```

```
source env/bin/activate
```

Установить зависимости из файла requirements.txt:

```
python3 -m pip install --upgrade pip
```

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

### Пример запроса к API

GET запрос http://127.0.0.1:8000/api/v1/posts/{id}/  
Пример ожидаемого ответа:  
{
"id": 0,
"author": "string",
"text": "string",
"pub_date": "2019-08-24T14:15:22Z",
"image": "string",
"group": 0
}

POST запрос http://127.0.0.1:8000/api/v1/posts/{post_id}/comments/  
payload  
{  
"text": "string"  
}  
Пример ожидаемого ответа:  
{
"id": 0,
"author": "string",
"text": "string",
"created": "2019-08-24T14:15:22Z",
"post": 0
}
