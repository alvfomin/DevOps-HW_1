# Задание №1 

## Описание

Docker-файлы для настройки Nginx и PostgreSQL. 
<br>Nginx ограничивает POST-запросы, PostgreSQL создает пользователя и базу данных при запуске.

## Структура 

- `Dockerfile.nginx`: Docker-файл для Nginx.
- `nginx.conf`: Конфигурация Nginx.
- `Dockerfile.postgres`: Docker-файл для PostgreSQL.
- `init.sql`: Скрипт инициализации базы данных.

## Установка и запуск

1. Клонируйте репозиторий:
  ```bash
   git clone https://github.com/username/repository-name.git
   cd repository-name
   ```
2. Соберите образы:
  ```bash
   docker build -t my-nginx -f Dockerfile.nginx
   docker build -t my-postgres -f Dockerfile.postgres
  ```
3. Запустите контейнеры:
  ```bash
   docker run --name my-nginx-container -p 80:80 -d my-nginx
   docker run --name my-postgres-container -e POSTGRES_PASSWORD=mysecretpassword -d my-postgres
  ```
## Проверка работы
- Nginx: Перейдите по адресу http://localhost.
- PostgreSQL: Подключитесь с помощью клиента:
- Хост: localhost
- Порт: 5432
- Пользователь: test
- Пароль: test_password
- База данных: test

## Лицензия
MIT License.
