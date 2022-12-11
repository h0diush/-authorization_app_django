---

# Проект авторизация пользователя

- ### В данном проекте используется приложение для регистрации, авторизации и аутентификации пользователей на сайте. Так же подтверждение электронной почты пользователя.

- ### Написаны юнит-тесты. Для их запуска введите в консоли ```python3 manage.py test```

- ### Используется свободная объектно-реляционная СУБД PostgresQL


## Для запуска проекта:

- #### Клонируйте репозиторий в рабочую папку ```git clone https://github.com/h0diush/authorization_app_django.git```
  - #### Создайте виртуальное окружение ```python3 -m venv venv```. Активируйте его ```. venv/bin/activate```.  И установите зависимости ```pip3 install -r req.txt``` 
- #### Создайте в корне файл ```.env``` и заполните следующими данными:
```
SECRET_KEY=django-insecure-7$0i!h%rdxiut%5mhkacu@8c&n2j2$im9g13)shz7)+*sftrd3
ALLOWED_HOSTS=localhost 127.0.0.1 0.0.0.0 [::1]
DEBUG=True

DB_ENGINE=django.db.backends.postgresql
DB_NAME=...
POSTGRES_USER=...
POSTGRES_PASSWORD=...
DB_HOST=...
DB_PORT=...

EMAIL_BACKEND=django.core.mail.backends.smtp.EmailBackend
EMAIL_HOST=...
EMAIL_PORT=...
EMAIL_USE_TLS=...
EMAIL_HOST_USER=...
EMAIL_HOST_PASSWORD=...
```
- #### Выполните миграции ```python3 manage.py makemigrations``` & ```python3 manage.py migrate```
- #### Заполните БД тестовыми данными ```python3 manage.py loaddata data/data.json```
- #### Соберите статические файлы ```python3 manage.py collectstatic```
### Для входа в админку используйте следующие данные:
- #### email: ```admin@api.com```
- #### password: ```admin```

## Для запуска проекта с помощью докера
- #### установите ```debug = False```
- ### **Перед запуском убедитесь что Docker установлен на ваше устройство**
- #### После чего введите в консоли ```docker-compose up -d --build```
- ### И пользуйтесь, на здоровье
