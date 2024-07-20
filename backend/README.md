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

```shell
pdm add djangorestframework
```

```python
INSTALLED_APPS = [
...
    "rest_framework",
    "users",
]
```


```shell
touch users/serializers.py
```


```python
from rest_framework.serializers import ModelSerializer

from .models import *

class UsersSerializer(ModelSerializer):
    class Meta:
        model = Categoria
        fields = "__all__"
```


- `views.py`:

```python
from rest_framework.viewsets import ModelViewSet

from .models import *
from .serializers import UsersSerializer

class UsersViewSet(ModelViewSet):
    queryset = Users.objects.all()
    serializer_class = UsersSerializer
```


As rotas são responsáveis por mapear as URLs para as views.

-  `urls.py`;

```python
from django.contrib import admin
from django.urls import include, path

from rest_framework.routers import DefaultRouter

from .views import *

router = DefaultRouter()
router.register(r"users", UsersViewSet)

urlpatterns = [
    path("admin/", admin.site.urls),
    path("", include(router.urls)),
]
```