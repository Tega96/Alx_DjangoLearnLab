## Delete books

Command: `Book.objects.filter(author='George Orwell').delete()`

Documentation:

```shell
from bookshelf.models import Book

>>> deleted_book = Book.objects.filter(author='George Orwell')
>>> deleted_book
<QuerySet [<Book: Ninety Eighty-Four by George Orwell in 1949>]>
>>> deleted_book.delete()
(1, {'bookshelf.Book': 1})
>>> deleted_book
<QuerySet []>

```
