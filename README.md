# Library Management System

A simple **console-based Library Management System** developed in Python.  
The project allows a user to add books, view available books, borrow books, return borrowed books, and exit the application.

## Features

- Add a new book to the library
- Display all currently available books
- Borrow a book by entering its name
- Return a previously borrowed book
- Handles unavailable books
- Handles invalid menu choices
- Converts book names to uppercase for consistent matching
- Uses a simple menu-driven console interface

## Technologies Used

- **Python 3**
- Python lists
- Functions
- `if/elif/else` conditions
- `while` loop
- `input()` and `print()`

## Project Structure

```text
LIBRARY-MANAGEMENT-SYSTEM/
│
├── library_management_system.py
├── README.md
├── STATEMENT.md
├── requirements.txt
├── .gitignore
│
└── screenshots/
    ├── menu_and_available_books.png
    ├── borrow_book.png
    ├── return_book.png
    └── exit.png
```

## How to Run

### 1. Install Python

Make sure Python 3 is installed on your computer.

Check the installation:

```bash
python --version
```

### 2. Clone the repository

```bash
git clone <YOUR-GITHUB-REPOSITORY-URL>
```

### 3. Open the project folder

```bash
cd LIBRARY-MANAGEMENT-SYSTEM
```

### 4. Run the program

```bash
python library_management_system.py
```

## Menu

The program provides five options:

```text
1. Add A Book
2. Show Available Books
3. Borrow A Book
4. Return A Book
5. Quit
```

### 1. Add A Book

Enter the name of a new book. The program converts the name to uppercase and adds it to the available books list.

### 2. Show Available Books

Displays all books currently available in the library.

### 3. Borrow A Book

Enter the name of a book. If the book is available:

- It is removed from the available-books list.
- It is added to the borrowed-books list.

If it is not available, the program displays an unavailable message.

### 4. Return A Book

Enter the name of a borrowed book. If it exists in the borrowed-books list:

- It is removed from the borrowed-books list.
- It is added back to the available-books list.

### 5. Quit

Closes the program and displays a thank-you message.

## Sample Books

The project starts with these sample books:

- ATOMIC HABITS
- WINGS OF FIRE
- 1984
- THE GREAT GATSBY
- THE HOBBIT
- THE POWER OF NOW
- IKIGAI
- THE ALCHEMIST
- THE PSYCHOLOGY OF MONEY
- ENCYCLOPEDIA

## Data Handling

The project uses two Python lists:

```python
books = [...]
taken = []
```

- `books` stores books that are currently available.
- `taken` stores books that have been borrowed.

The data is stored **in memory only**, so changes are lost when the program is closed.

## Screenshots

### Library Menu / Available Books

![Available Books](screenshots/menu_and_available_books.png)

### Borrowing a Book

![Borrow Book](screenshots/borrow_book.png)

### Returning a Book

![Return Book](screenshots/return_book.png)

### Exiting the Program

![Exit](screenshots/exit.png)

## Limitations

- No database or permanent file storage
- No user/login system
- No student/member records
- No due dates or fine calculation
- Book information is limited to the book name
- Duplicate book names are not prevented

## Future Improvements

The project can be extended by adding:

- Database connectivity using SQLite/MySQL
- Student/member registration
- Login and authentication
- Book IDs and author details
- Issue and return dates
- Due-date and fine calculation
- Search and filter functionality
- Persistent storage
- Graphical User Interface (GUI)
- Admin functionality

## Learning Outcomes

This project demonstrates the practical use of:

- Python functions
- Lists
- Loops
- Conditional statements
- User input
- Basic program flow
- Menu-driven programming

## License

This project is provided for educational and academic use.
