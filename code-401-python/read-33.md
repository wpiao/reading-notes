# Read:33 - Authentication & Production Server - 03/22/2022

## Jason Web Token

Json Web Token (JWT) is an open standard that defines a compact and self-contained way for securely transimitting information between parties as a JSON object. This information can be verified and trusted because it is digitally signed.  
**Use cases**:

- Authorization
- Information Exchange

**JWT Structure**:

- Header:
  ```json
  {
    "typ": "JWT",
    "alg": "HS256"
  }
  ```
- Payload
  ```json
  {
    "token_type": "access",
    "exp": 1543828431,
    "jti": "7f5997b7150d46579dc2b49167097e7b",
    "user_id": 1
  }
  ```
- Signature
- Format: `header.payload.signature`: `xxxxx.yyyyy.zzzz`

## JWT setup for Django REST Framework

Dependency: `djangorestframework-simplejwt`

```python
# install dependency: pip install djangorestframework-simplejwt

# settings.py
REST_FRAMEWORK = {
    'DEFAULT_AUTHENTICATION_CLASSES': [
        'rest_framework_simplejwt.authentication.JWTAuthentication',
    ],
}

# urls.py in the project
from django.urls import path
from rest_framework_simplejwt import views as jwt_views

urlpatterns = [
    # Your URLs...
    path('api/token/', jwt_views.TokenObtainPairView.as_view(), name='token_obtain_pair'),
    path('api/token/refresh/', jwt_views.TokenRefreshView.as_view(), name='token_refresh'),
]

# views.py
from rest_framework.views import APIView
from rest_framework.response import Response
from rest_framework.permissions import IsAuthenticated


class HelloView(APIView):
    permission_classes = (IsAuthenticated,)

    def get(self, request):
        content = {'message': 'Hello, World!'}
        return Response(content)

# urls.py
from django.urls import path
from myapi.core import views

urlpatterns = [
    path('hello/', views.HelloView.as_view(), name='hello'),
]
```

## Django production server

Django app does not actually run as you would think a server would - waiting for requests and reacting to them. Your project provides a uwsgi.py file, which contains a function to be called by the application server. This function gets a Python object representing the incoming request.

This function calls your code, and produces a response object which is passed to the WSGI server. There the response is translated into a HTTP response and is passed back to the web server, which finally delivers it to the user.

If you want to run Django in production, be sure to use a production-ready web server like Nginx, and let your app be handled by a WSGI application server like Gunicorn.

## References

- [JWT introduction](https://jwt.io/introduction/)
- [How to Use JWT Authentication with Django REST Framework](https://simpleisbetterthancomplex.com/tutorial/2018/12/19/how-to-use-jwt-authentication-with-django-rest-framework.html)
- [Gunicorn](https://vsupalov.com/django-runserver-in-production/)
