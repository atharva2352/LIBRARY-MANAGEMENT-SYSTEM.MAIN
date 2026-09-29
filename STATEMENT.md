# Project Statement — Library Management System

## 1. Project Title

**Library Management System**

## 2. Problem Statement

Managing books manually can make it difficult to keep track of which books are available and which books have been borrowed. A simple computer-based system can make these basic library operations easier to perform.

This project provides a menu-driven Python application for managing a small collection of library books. The system allows the user to add books, view available books, borrow books, return books, and exit the application.

## 3. Objective

The main objective of this project is to create a simple and easy-to-use Library Management System using basic Python programming concepts.

The project is designed to:

1. Maintain a list of available books.
2. Allow the user to add new books.
3. Display books currently available in the library.
4. Allow a user to borrow an available book.
5. Allow a borrowed book to be returned.
6. Provide appropriate messages for unavailable books and invalid options.

## 4. Scope of the Project

The current project is a basic console-based system intended for learning and academic demonstration.

It focuses on the core operations of a small library:

- Adding books
- Viewing available books
- Borrowing books
- Returning books
- Exiting the system

It does not currently include user accounts, databases, book authors, due dates, fines, or permanent storage.

## 5. Functional Requirements

### FR1 — Add Book

The system should allow the user to enter a book name and add it to the available-books list.

### FR2 — Display Available Books

The system should display the books currently present in the library.

### FR3 — Borrow Book

The system should accept a book name and check whether that book is available.

If available:

- Remove the book from the available list.
- Add it to the borrowed list.
- Display a confirmation message.

If unavailable:

- Display an appropriate unavailable message.

### FR4 — Return Book

The system should accept a book name and check whether it is in the borrowed list.

If the book was borrowed:

- Remove it from the borrowed list.
- Add it back to the available list.
- Display a confirmation message.

If it was not borrowed:

- Display an appropriate message.

### FR5 — Exit

The system should terminate when the user selects option 5.

## 6. Non-Functional Requirements

- The program should be simple to use.
- The program should provide clear menu options.
- The program should run in a Python 3 environment.
- The program should give understandable messages for successful and unsuccessful operations.
- The program should continue displaying the menu until the user chooses to exit.

## 7. Input

The program accepts:

- Menu option from 1 to 5
- Book name when adding a book
- Book name when borrowing a book
- Book name when returning a book

Book names are converted to uppercase before being stored or searched.

## 8. Output

The program displays:

- Library menu
- Available books
- Confirmation when a book is added
- Confirmation when a book is borrowed
- Confirmation when a book is returned
- Messages for unavailable or incorrectly returned books
- Invalid-option message
- Exit/thank-you message

## 9. Data Structures Used

The program uses two Python lists:

```python
books = [...]
taken = []
```

### `books`

Stores the books currently available in the library.

### `taken`

Stores the books that have been borrowed.

When a book is borrowed, it moves from `books` to `taken`.

When a book is returned, it moves from `taken` back to `books`.

## 10. Main Functions

### `addBook()`

Takes a book name from the user, converts it to uppercase, and adds it to the `books` list.

### `showBook()`

Displays the currently available books with numbering.

### `borrowBook()`

Checks whether the requested book exists in `books`. If it exists, the book is moved to `taken`.

### `returnBook()`

Checks whether the requested book exists in `taken`. If it exists, the book is moved back to `books`.

## 11. Program Flow

```text
START
  |
  v
Display Library Menu
  |
  v
Take User Choice
  |
  +---- 1 ----> Add Book
  |
  +---- 2 ----> Show Available Books
  |
  +---- 3 ----> Borrow Book
  |
  +---- 4 ----> Return Book
  |
  +---- 5 ----> Exit
  |
  v
Return to Menu
```

The menu repeats using a `while True` loop until the user selects option 5.

## 12. Algorithm

1. Initialize the list of sample books.
2. Initialize an empty list for borrowed books.
3. Display the library menu.
4. Ask the user to select an option.
5. Execute the corresponding function:
   - Add a book.
   - Show available books.
   - Borrow a book.
   - Return a book.
   - Exit the program.
6. If the selected option is invalid, display an error message.
7. Continue the menu until the user selects Quit.

## 13. Current Limitations

The current implementation stores all information in Python lists in memory. Therefore, any changes made during execution are lost after the program closes.

Other current limitations include:

- No permanent database/file storage
- No login or member management
- No book IDs
- No author/publisher information
- No due-date management
- No fine calculation
- No duplicate-book validation

## 14. Future Enhancements

Possible improvements include:

1. Add SQLite/MySQL database support.
2. Add student/member registration.
3. Add login and authentication.
4. Store book ID, title, author, and publisher.
5. Add issue date and return date.
6. Add automatic fine calculation.
7. Add book search functionality.
8. Add duplicate-book validation.
9. Create a GUI version.
10. Add permanent data storage.

## 15. Conclusion

The Library Management System is a beginner-friendly Python project that demonstrates how functions, lists, loops, conditions, and user input can be combined to create a useful menu-driven application.

The project provides the basic operations required to manage the availability and borrowing status of books and can be expanded into a larger library management application with database and user-management features.
