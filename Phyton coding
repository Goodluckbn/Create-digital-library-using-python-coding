```python
class Book:
    def __init__(self, title, author, year, genre):
        self.title = title
        self.author = author
        self.year = year

```python
class Book:
    def __init__(self, title, author, genre):
        self.title = title
        self.author = author
        self.genre = genre
        self.status = "Available"

    def display_info(self):
        print("Title:", self.title)
        print("Author:", self.author)
        print("Genre:", self.genre)
        print("Status:", self.status)

    def change_status(self, new_status):
        self.status = new_status
```

```python
class DigitalLibrary:
    def __init__(self):
        self.books = []

    def add_book(self, book):
        self.books.append(book)

    def search_book(self, title):
        found_books = []
        for book in self.books:
            if book.title.lower() == title.lower():
                found_books.append(book)
        return found_books

    def display_books(self):
        if not self.books:
            print("No books in the library.")
        else:
            for book in self.books:
                book.display_info()
                print("---------------------")

    def borrow_book(self, title):
        found_books = self.search_book(title)
        if len(found_books) == 0:
            print("Book not found.")
        elif found_books[0].status == "Available":
            found_books[0].change_status("On loan")
            print("Book borrowed successfully.")
        else:
            print("Book is already on loan.")

    def return_book(self, title):
        found_books = self.search_book(title)
        if len(found_books) == 0:
            print("Book not found.")
        elif found_books[0].status == "Available":
            print("Book is already in the library.")
        else:
            found_books[0].change_status("Available")
            print("Book returned successfully.")
```

```python
# Create instances of Book
book1 = Book("Book 1", "Author 1", "Genre 1")
book2 = Book("Book 2", "Author 2", "Genre 2")

# Create an instance of DigitalLibrary
library = DigitalLibrary()

# Add books to the library
library.add_book(book1)
library.add_book(book2)

# Display all books in the library
library.display_books()

# Search for a book
found_books = library.search_book("Book 1")
if found_books:
    found_books[0].display_info()

# Borrow a book
library.borrow_book("Book 1")

# Return a book
library.return_book("Book 1")
```
