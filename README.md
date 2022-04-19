# yamdb_final

## **Описание**
Проект YaMDb собирает отзывы пользователей на различные произведения.

**Технологи:**
* Python
* Django REST Framework
* Docker

(https://github.com/Anastasia-prog-create/yamdb_final/actions/workflows/yamdb_workflow.yml/badge.svg?event=push)

### Как запустить проект:

Клонируйте репозиторий и перейдите в него в командной строке:
```sh
git clone https://github.com/Anastasia-prog-create/infra_sp2.git
cd infra_sp2
```
В директории infra/ cоздайте и заполните файл .env необходимыми переменными.
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
Запустите терминал и перейдите в директорию, в которой находится docker-compose.yaml:
```sh
сd infra
```
Запустите docker-compose командой:
```sh
docker-compose up -d
```
В контейнере web по очереди выполните команды:
```sh
docker-compose exec web python manage.py migrate
docker-compose exec web python manage.py createsuperuser
docker-compose exec web python manage.py collectstatic --no-input 
```
Убедитесь, что проект работает по ссылке: http://127.0.0.1:8000/admin/
