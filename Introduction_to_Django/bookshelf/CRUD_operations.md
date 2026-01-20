## Creating a Book instance

`new_book = Book(title="1984", author="George Orwell", publication_year='1948')`C

### Documentation on expected outcome

```shell
new_book = Book(title='Science of Getting rich', author='Wallace D Wattle', publication_year=1936)
>>> new_book.save()
>>> new_book
<Book: Book object (1)>

```

## Retrieving a Book from models

`book = Book.objects.all()` - Retrives all books from models

Expected output:

```shell
>>> Book.objects.all()
<QuerySet [<Book: Book object (1)>, <Book: Book object (2)>]>

```

## Updating books

Command: `updated_book = Book.objects.filter(title="1989")`
`updated_book.update(title='Ninteen Eighty-Four`

Documentation

```shell
>>> update_book = Book.objects.filter(title="1984")
>>> update_book
<QuerySet [<Book: 1984 by George Orwell in 1949>]>
>>> update_book.update(title='Ninety Eighty-Four')
1
>>> update_book
<QuerySet []>
>>> Book.object.all()
Traceback (most recent call last):
  File "<console>", line 1, in <module>
AttributeError: type object 'Book' has no attribute 'object'. Did you mean: 'objects'?
>>> Book.objects.all()
<QuerySet [<Book: Science of Getting rich by Wallace D Wattle in 1936>, <Book: Science of being greate by Walace D Wattle in 1947>, <Book: Mechanism of sitting down to read by ken Carter in 2011>, <Book: Science of getting rich by Wallace D Wattle in 1995>, <Book: Ninety Eighty-Four by George Orwell in 1949>]>
>>>


```

## Delete books

Command: `Book.objects.filter(author='George Orwell').delete()`

Documentation:

```shell
>>> deleted_book = Book.objects.filter(author='George Orwell')
>>> deleted_book
<QuerySet [<Book: Ninety Eighty-Four by George Orwell in 1949>]>
>>> deleted_book.delete()
(1, {'bookshelf.Book': 1})
>>> deleted_book
<QuerySet []>

```
