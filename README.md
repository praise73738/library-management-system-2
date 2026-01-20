# Library Management System (LMS)

## Project Overview
The **Library Management System (LMS)** is a web-based application designed to automate the process of managing books and student borrowing activities. It allows librarians to manage books and users while tracking borrowing and returning of books efficiently. This project is implemented using **HTML, CSS, JavaScript (frontend), Python + Flask (backend), and SQLite (database)**.

---

## SDLC Report

### 1. Planning
- **Problem:** Manual tracking of books and student borrowing is slow and error-prone.
- **Solution:** LMS automates book management, borrowing, and returning processes, improving efficiency and accuracy.

---

### 2. Requirements

#### Functional Requirements
1. Add/Edit/Delete users (students/librarians)
2. Add/Edit/Delete books
3. Borrow books (check availability)
4. Return books
5. View borrowing history and reports

#### Non-Functional Requirements
1. Web-based interface, responsive and user-friendly
2. Fast and reliable operations
3. Secure access to prevent unauthorized changes

---

### 3. Design

#### Database Structure
- **Students**(`StudentID`, `Name`, `Email`)
- **Books**(`BookID`, `Title`, `Author`, `Quantity`)
- **BorrowRecords**(`BorrowID`, `StudentID`, `BookID`, `BorrowDate`, `ReturnDate`)

#### UML Overview
- **Use-case:** Students borrow/return books; admin manages books/users.
- **Classes:** `Student`, `Book`, `BorrowRecord`, `LibrarySystem`.

---

### 4. Implementation
- **Frontend:** HTML/CSS/JS  
  - `index.html` → Borrow books  
  - `return.html` → Return books  
  - `users.html` → Manage users  
  - `catalog.html` → View all books  
- **Backend:** Python + Flask (`backend/app.py`)  
- **Database:** SQLite (`database/library.db`)  
- **JavaScript:** Handles form submission and communicates with backend using Fetch API.

---

### 5. Testing
- **Unit Testing:** Validated borrow and return functions.  
- **Integration Testing:** Borrowing reduces book quantity; returning increases it.  
- **UI Testing:** Forms and buttons function correctly, error messages displayed when needed.

---

### 6. Deployment
- **Frontend:** GitHub Pages (static pages)  
- **Backend:** Flask server deployed locally or on Heroku/Railway  
- **Database:** SQLite  

---

### 7. Maintenance
- Regular updates to add new features or fix bugs  
- Database backups and migration  
- UI improvements based on feedback

---

### 8. SDLC to Implementation Mapping

| SDLC Name | Implementation Name |
|-----------|-------------------|
| Student   | `StudentID`, `Name`, `Email` |
| Book      | `BookID`, `Title`, `Author`, `Quantity` |
| BorrowRecord | `BorrowID`, `StudentID`, `BookID`, `BorrowDate`, `ReturnDate` |
| LibrarySystem | `backend/app.py` + `database/library.db` |

---

### 9. How to Run Locally
1. Install Python and Flask:  
```bash
pip install flask
