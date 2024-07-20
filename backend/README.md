# IJML DRF Backend

# Main routes

- http://localhost:8000
- http://localhost:8000/admin

### Main commands && steps

```shell
pdm init
```

```shell
pdm add django
```

```shell
pdm run django-admin startproject config .
```

```shell
pdm run python manage.py runserver
```

```shell
pdm run python manage.py migrate
```

```shell
pdm run python manage.py makemigrations
```

```shell
pdm run python manage.py createsuperuser
```

```shell
pdm run python manage.py startapp users
```

```python
INSTALLED_APPS = [
    "users",
]
```