## Creating a Book instance

`new_book = Book.objects.create(title="1984", author="George Orwell", publication_year='1948')`C

### Documentation on expected outcome

```shell
new_book = Book.objects.create(title='Science of Getting rich', author='Wallace D Wattle', publication_year=1936)
>>> new_book.save()
>>> new_book
<Book: Book object (1)>

```
