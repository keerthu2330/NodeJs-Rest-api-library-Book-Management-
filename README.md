# NodeJs-Rest-api-library-Book-Management-
Project code
library = []

def add_book():
    book_id = input("Enter Book ID: ")
    title = input("Enter Book Title: ")
    author = input("Enter Author Name: ")
    library.append({"ID": book_id, "Title": title, "Author": author})
    print("Book added successfully!\n")

def search_book():
    book_id = input("Enter Book ID to search: ")
    for book in library:
        if book["ID"] == book_id:
            print("Book Found!")
            print(book)
            return
    print("Book not found.\n")

def display_books():
    if not library:
        print("No books available.\n")
    else:
        for book in library:
            print(book)
        print()

def delete_book():
    book_id = input("Enter Book ID to delete: ")
    for book in library:
        if book["ID"] == book_id:
            library.remove(book)
            print("Book deleted successfully!\n")
            return
    print("Book not found.\n")

while True:
    print("Library Menu")
    print("1. Add Book")
    print("2. Search Book")
    print("3. Display Books")
    print("4. Delete Book")
    print("5. Exit")

    choice = input("Enter choice: ")

    if choice == '1':
        add_book()
    elif choice == '2':
        search_book()
    elif choice == '3':
        display_books()
    elif choice == '4':
        delete_book()
    elif choice == '5':
        print("Exiting...")
        break
    else:
        print("Invalid choice. Try again.\n")
