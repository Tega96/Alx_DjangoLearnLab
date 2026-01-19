## Updating books

Command: `updated_book = Book.objects.filter(title="1989")`
`updated_book.update(title='Ninteen Eighty-Four`

Documentation

```shell
>>> update_book = Book.objects.filter(title="1984")
>>> update_book
<QuerySet [<Book: 1984 by George Orwell in 1949>]>
>>> update_book.update("book.title", 'Ninety Eighty-Four')
1
>>> Book.objects.all()
<QuerySet [<Book: Science of Getting rich by Wallace D Wattle in 1936>, <Book: Science of being greate by Walace D Wattle in 1947>, <Book: Mechanism of sitting down to read by ken Carter in 2011>, <Book: Science of getting rich by Wallace D Wattle in 1995>, <Book: Ninety Eighty-Four by George Orwell in 1949>]>
>>>
U

```
