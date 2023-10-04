# Диплом


### Запуск локально
___
Шаг 1. Установите зависимости:
```
pip install -r requirements.txt
```
Шаг 2. Зайдите в настройки БД и настройте их под себя
```
# mycloud/settings.py

EMAIL_HOST = 'smtp.qq.com'
EMAIL_PORT = '587'
EMAIL_HOST_USER = '******'
EMAIL_HOST_PASSWORD = '******'
EMAIL_USE_TLS = True
DEFAULT_FROM_EMAIL = EMAIL_HOST_USER


DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'cloud',
        'HOST': '127.0.0.1',
        'PORT': '3306',
        'USER': '***',
        'PASSWORD': '******',
    }
}
```
Шаг 3. Сделайте перенос БД
```
python manage.py migrate
```

Шаг 4. Создайте суперпользователя
```
python manage.py createsuperuser
```
Шаг 5. Запустите локальный сервер
```
python manage.py runserver