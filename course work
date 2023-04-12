#GROUP MEMBERS
#Malesi Joel David
#Karungi Faith
#Aspolo



class Book:
    def __init__(self, title, author, isbn, available=True):
        self.title = title
        self.author = author
        self.isbn = isbn
        self.available = available

    def __str__(self):
        return f"{self.title} by {self.author}"

    def get_info(self):
        return f"{self.title} by {self.author}. ISBN: {self.isbn}. Available: {self.available}"

    def check_out(self):
        if self.available:
            self.available = False
            print(f"{self.title} has been checked out.")
        else:
            print(f"Sorry, {self.title} is not available at the moment.")

    def return_book(self):
        if not self.available:
            self.available = True
            print(f"Thank you for returning {self.title}.")
        else:
            print(f"{self.title} has already been returned.")


class Fiction(Book):
    def __init__(self, title, author, isbn, genre, available=True):
        super().__init__(title, author, isbn, available)
        self.genre = genre

    def get_info(self):
        return f"{super().get_info()} Genre: {self.genre}."


class NonFiction(Book):
    def __init__(self, title, author, isbn, subject, available=True):
        super().__init__(title, author, isbn, available)
        self.subject = subject

    def get_info(self):
        return f"{super().get_info()} Subject: {self.subject}."


class Library:
    def __init__(self):
        self.books = []

    def add_book(self, book):
        self.books.append(book)

    def remove_book(self, book):
        self.books.remove(book)

    def search_by_title(self, title):
        matching_books = [book for book in self.books if book.title == title]
        return matching_books

    def search_by_author(self, author):
        matching_books = [book for book in self.books if book.author == author]
        return matching_books

    def search_by_isbn(self, isbn):
        matching_books = [book for book in self.books if book.isbn == isbn]
        return matching_books

    def show_inventory(self):
        for book in self.books:
            print(book.get_info())


# Example usage
book1 = Fiction("The Catcher in the Rye", "J.D. Salinger", "0316769487", "Coming-of-age")
book2 = NonFiction("The Selfish Gene", "Richard Dawkins", "0192860925", "Evolutionary biology")
book3 = Fiction("To Kill a Mockingbird", "Harper Lee", "0446310786", "Southern Gothic")

lib = Library()
lib.add_book(book1)
lib.add_book(book2)
lib.add_book(book3)

# search for a book by title
matching_books = lib.search_by_title("To Kill a Mockingbird")
print([book.get_info() for book in matching_books])

# check out a book
book1.check_out()

# show the library inventory
lib.show_inventory()
