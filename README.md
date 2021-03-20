# DjangorestAPI

Exemplo de API feita em [Django Rest Framework](https://www.django-rest-framework.org/).

## Como rodar o projeto?

* Clone esse repositório.
* Crie um virtualenv com Python 3.
* Ative o virtualenv.
* Instale as dependências.
* Rode as migrações.

```
git clone https://github.com/bahiamartins/DjangorestAPI.git
cd DjangorestAPI
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
python manage.py migrate
python manage.py createsuperuser --username="admin" --email=""
```

No Admin crie seu Token. Ou pelo terminal:

```python
python manage.py shell_plus
```

```python
from django.contrib.auth.models import User
from rest_framework.authtoken.models import Token

user = User.objects.first()
Token.objects.create(user=user)
```

## Swagger

http://localhost:8000/swagger/

## Postman

POST: http://localhost:8000/api/users/

`Body > raw > JSON`

```
{
  "email": "user@example.com",
  "first_name": "string",
  "last_name": "string",
  "password": "string"
}
```


## Links

* https://www.django-rest-framework.org/api-guide/viewsets/
* http://www.cdrf.co/3.9/rest_framework.generics/CreateAPIView.html#perform_create
* https://drf-yasg.readthedocs.io/en/stable
