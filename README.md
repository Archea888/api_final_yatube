# Описание

Проект Yatube это социальная сеть, в проекте реализованна API.
Аутентификация по JWT-токену. Применнненые методы GET, POST, PUT, PATCH, DELETE.
У неаутентифицированных пользователей доступ к API только на чтение, аутентифицированным пользователям разрешено изменение и удаление своего контента.

# Технологии

Python, Django, DRF, Simple JWT.

# Развернуть проект

## 1) Склонировать репозиторий

git clone https://github.com/Archea888/api_final_yatube

cd api_final_yatube/

## 2) Создать и активировать виртуальное окружение для проекта

python -m venv venv

source venv/scripts/activate
## 3) Установить зависимости
python pip install -r requirements.txt

## 4) Сделать миграции
python manage.py makemigrations
python manage.py migrate

## 5) Запустить сервер
python manage.py runserver

# Примеры 
 
Для доступа к проекту необходимо получить токен:  
Нужно выполнить POST-запрос localhost:8000/api/v1/token/ в ответе на запрос приходит token (JWT-токен). 
 
Дальше, передав токен можно будет обращаться к методам, например:  
 
/api/v1/posts/ (GET, POST, PUT, PATCH, DELETE) 