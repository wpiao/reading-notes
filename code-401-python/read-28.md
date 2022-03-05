# Read:28 - Django Forms - 03/05/2022

- [Django Forms Tutorial](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Forms)

- HTML Form

  ```html
  <form action="/team_name_url/" method="post">
    <label for="team_name">Enter name: </label>
    <input
      id="team_name"
      type="text"
      name="name_field"
      value="Default name for team."
    />
    <input type="submit" value="OK" />
  </form>
  ```

- Django Form

  ```python
  from django import forms

  class RenewBookForm(forms.Form):
      renewal_date = forms.DateField(help_text="Enter a date between now and 4 weeks (default 3).")
  ```

- Django From Validation

  ```python
  import datetime

  from django import forms

  from django.core.exceptions import ValidationError
  from django.utils.translation import gettext_lazy as _

  class RenewBookForm(forms.Form):
      renewal_date = forms.DateField(help_text="Enter a date between now and 4 weeks (default 3).")

      def clean_renewal_date(self):
          data = self.cleaned_data['renewal_date']

          # Check if a date is not in the past.
          if data < datetime.date.today():
              raise ValidationError(_('Invalid date - renewal in past'))

          # Check if a date is in the allowed range (+4 weeks from today).
          if data > datetime.date.today() + datetime.timedelta(weeks=4):
              raise ValidationError(_('Invalid date - renewal more than 4 weeks ahead'))

          # Remember to always return the cleaned data.
          return data
  ```

- URL Configration
  ```python
  urlpatterns += [
      path('book/<uuid:pk>/renew/', views.renew_book_librarian, name='renew-book-librarian'),
  ]
  ```
