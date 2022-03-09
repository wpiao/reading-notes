# Read: 29 - Django Custom User - 03/08/2022

- AbstractUser vs AbstractBaseUser
  We can subclass both of them to extend existing functionality however `AbstractBaseUser` requires much, much more work. `AbstractUser` is a subclass of `AbstractBaseUser` that provides more default configuration.
- 4 steps to create a custom user model

  1. Update `settings.py`
     ```python
     # config/settings.py
     INSTALLED_APPS = [
         'django.contrib.admin',
         'django.contrib.auth',
         'django.contrib.contenttypes',
         'django.contrib.sessions',
         'django.contrib.messages',
         'django.contrib.staticfiles',
         'accounts', # new
     ]
     AUTH_USER_MODEL = 'accounts.CustomUser' # new
     ```
  2. Create a new`CustomUser`model

     ```python
     # accounts/models.py
     from django.contrib.auth.models import AbstractUser
     from django.db import models

     class CustomUser(AbstractUser):
         pass
         # add additional fields in here

         def __str__(self):
             return self.username
     ```

  3. Create new`UserCreation`and`UserChangeForm`

     ```python
     # accounts/forms.py
     from django import forms
     from django.contrib.auth.forms import UserCreationForm, UserChangeForm
     from .models import CustomUser

     class CustomUserCreationForm(UserCreationForm):
         class Meta:
             model = CustomUser
             fields = ('username', 'email')

     class CustomUserChangeForm(UserChangeForm):
         class Meta:
             model = CustomUser
             fields = ('username', 'email')
     ```

  4. Update the admin

     ```python
     # accounts/admin.py
     from django.contrib import admin
     from django.contrib.auth.admin import UserAdmin
     from .forms import CustomUserCreationForm, CustomUserChangeForm
     from .models import CustomUser

     class CustomUserAdmin(UserAdmin):
        add_form = CustomUserCreationForm
        form = CustomUserChangeForm
        model = CustomUser
        list_display = ['email', 'username',]
     admin.site.register(CustomUser, CustomUserAdmin)
     ```
