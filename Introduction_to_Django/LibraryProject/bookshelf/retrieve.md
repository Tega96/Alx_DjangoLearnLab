## Retrieving a Book from models

`book = Book.objects.get(title="1984")` - Retrives all books from models

Expected output:

```shell
>>> Book.objects.get(title="1984")
<QuerySet [<Book: Book object (1)>, <Book: Book object (2)>]>

```
