## Django Project.

Some valuable Django commands

`pip install django` - Installs Django
`django-admin startproject LibraryProject` Create a django project called LibraryProject.
`python manage.py runserver` Starts the development server
`python manage.py startapp bookshelf` -- Creates or generate new app called bookshelf.
`python manage.py makemigration bookshelf` -- Prepares your model for database integration.
`python manage.py migrate` To apply migration to update the database with.
`python manage.py shell` To interact with the python model via shell.

## Django models and their structure

Models in django are defined as python classes that inherits from django.db.models.Model base class.

Example of Book model with three fields.

```py
from django.db import models

class Book(models.Model):
    title = models.CharField(max_length=200)
    author = models.CharField(maz_length=100)
    publised_date = models.DateField()

```

## Database Interaction with the Django ORM

Examples:
Retriving all books `books = Book.objects.all()`
Filtering books by author: `books_by_author = Book.object.filter(author='John Doe')`
Ordering books by published date: `books_ordered = Book.objects.order_by('published_date')`
Create a new book: `new_book = Book(title='New Book', author='Jane Smith', published_date='2023-01-01')`
`new_book.save()`

## Configuring the database

This involves modifying the settings.py file.

```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql', // for MySQL
        'NAME': 'nameofdatabase',
        'USER': 'mydatabaseuser',
        'PASSWORD': 'mypassword',
        'HOST': 'localhost',
        'PORT': '3306',
    }
}
// use `pip install mysqlclient` to install MySQL
```

# Admin page

`python manage.py createsuperuser` To create admin user account. (Provide a user name and password).
Register model with the admin interface by adding them to the `admin.py` file in your app.
n
