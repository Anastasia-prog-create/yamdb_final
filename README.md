# yamdb_final

## **Описание**
Проект YaMDb собирает отзывы пользователей на различные произведения.

**Технологи:**
* Python
* Django REST Framework
* Docker

![Yamdb_final workflow](https://github.com/Anastasia-prog-create/yamdb_final/actions/workflows/yamdb_workflow.yml/badge.svg?event=push)

### О проекте:

Клонировать репозитозиторий можно командами ниже:
```sh
git clone https://github.com/Anastasia-prog-create/yamdb_final.git
cd yamdb_final
```
Для работы с проектом в директории infra/ cоздайте и заполните файл .env необходимыми переменными.
Пример наполнения файла .env:
```
SECRET_KEY = 'your_secret_key'

DB_ENGINE=django.db.backends.postgresql
DB_NAME=db_name
POSTGRES_USER=login
POSTGRES_PASSWORD=password
DB_HOST=container_name
DB_PORT=port_number
```
### URLS проекта:
Все запросы к API начинаются с /api/v1/, доступные адреса:
* http://51.250.102.104/api/v1/users/
* http://51.250.102.104/api/v1/categories/
* http://51.250.102.104/api/v1/genres/
* http://51.250.102.104/api/v1/titles/

### Ознакомится с подробной документацией к API можно здесь:
http://51.250.102.104/redoc/
