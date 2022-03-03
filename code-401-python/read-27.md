# Read: 27 - Django Models - 02/28/2022

## Using Models

- [Django Model Tutorial](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Models)

- modles example codes

  ```python
  from django.db import models

  class MyModelName(modles.Model):

    # Fields
    my_field_name = models.CharField(max_length=20, help_text='Enter field documentation')

    # Metadata
    class Meta:
      ordering = ['-my_field_name']

    # methods
    def get_absolute_url(self):
      return reverse('model-detail-view', args=[str(self.id)])

    def __str__(self):
      return self.my_field_name
  ```

- Commom Field Arguments

  - help_text
  - verbose_name
  - default
  - null
  - blank
  - choices
  - primary_key

- Comon Field Types
  - CharField
  - TextField
  - IntegerField
  - DataField and DataTimeField
  - EmailField
  - FileField and ImageField
  - AutoField
  - ForeignKey
  - ManyToManyField

## Django Admin

- [Django Admin Tutorial](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Admin_site)

- Registering models

  ```python
  from django.contrib import admin
  from .models import Author, Genre, Book, BookInstance
  admin.site.register(book)
  admin.site.register(Author)
  admin.site.register(Genre)
  admin.site.register(BookInstance)
  ```

- Creating a superuser
  `python3 manage.py createsuperuser`
  `python3 manage.py runserver`
