# Retro:33 - Django authentication and production server - 03/24/2022

```python
# dependencies
# - gunicorn
# - whitenoise
# - djangorestframework-simplejwt

# settings.py
MIDDLEWARE = [
    # ...
    'whitenoise.middleware.WhiteNoiseMiddleware',
]

INSTALLED_APPS = [
    # ...
    'whitenoise.runserver_nostatic',
]
REST_FRAMEWORK = {
    'DEFAULT_PERMISSION_CLASSES' : [
        'rest_framework.permissions.IsAuthenticated',
    ],
    'DEFAULT_AUTHENTICATION_CLASSES': [
        'rest_framework_simplejwt.authentication.JWTAuthentication',
        'rest_framework.authentication.SessionAuthentication',
        'rest_framework.authentication.BasicAuthentication',
    ]
}

STATIC_ROOT = BASE_DIR / 'staticfiles'

# urls.py in project folder
from rest_framework_simplejwt import views as jwt_views

urlpatterns = [
    # ...
    path('api/token/', jwt_views.TokenObtainPairView.as_view(), name='token_obtain_pair'),
    path('api/token/refresh', jwt_views.TokenRefreshView.as_view(), name='token_refresh'),
]
```
