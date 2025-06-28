# Library Management System 📚

A console-based library management system built with C# and .NET 8.0 that allows you to manage books, members, borrowing, and returns in a simple and intuitive way.

## Features ✨

- 📖 Book management (add, view, search)
- 👥 Member management (add, view)
- 📋 Borrowing and returning books
- 🔍 Search functionality for books
- ⏰ Overdue book tracking
- 📊 Member book history
- 🚫 Borrowing limits (max 3 books per member)
- 📅 14-day loan periods

## Project Structure 📁

```
aruja/
├── aruja.sln                 # Solution file
├── aruja/
│   ├── aruja.csproj         # Project configuration
│   ├── Program.cs           # Main application code
│   ├── bin/                 # Compiled binaries
│   │   └── Debug/net8.0/    # Debug build output
│   └── obj/                 # Build artifacts and temporary files
```

## Classes Overview 🏗️

### 📚 `Book` Class
Represents individual books in the library system.

**Properties:**
- `Id` - Unique identifier
- `Title` - Book title
- `Author` - Book author
- `ISBN` - International Standard Book Number
- `IsAvailable` - Availability status
- `DueDate` - Return due date (when borrowed)
- `BorrowedBy` - Name of current borrower

### 👤 `Member` Class
Represents library members who can borrow books.

**Properties:**
- `Id` - Unique identifier
- `Name` - Member's full name
- `Email` - Contact email
- `BorrowedBooks` - List of currently borrowed book IDs
- `MemberSince` - Registration date

### 🏛️ `Library` Class
Main management class that handles all library operations.

**Key Methods:**
- `AddBook()` - Add new books to the collection
- `AddMember()` - Register new library members
- `BorrowBook()` - Process book borrowing
- `ReturnBook()` - Process book returns
- `SearchBooks()` - Search by title or author
- `ShowOverdueBooks()` - Display overdue items
- `ShowMemberBooks()` - Show books borrowed by a specific member

### 🖥️ `Program` Class
Contains the main entry point and user interface logic.

## How to Use 🚀

### Prerequisites
- .NET 8.0 SDK installed
- Terminal or command prompt access

### Running the Application

1. **Clone or download the project**
2. **Navigate to the project directory:**
   ```bash
   cd aruja
   ```

3. **Build the project:**
   ```bash
   dotnet build
   ```

4. **Run the application:**
   ```bash
   dotnet run
   ```

### Menu Options 📋

When you run the application, you'll see the main menu with these options:

| Option | Description |
|--------|-------------|
| **1** | View all books in the library |
| **2** | View all registered members |
| **3** | Search books by title or author |
| **4** | Borrow a book (requires book ID and member ID) |
| **5** | Return a borrowed book (requires book ID) |
| **6** | Add a new book to the library |
| **7** | Register a new member |
| **8** | View overdue books |
| **9** | View books borrowed by a specific member |
| **0** | Exit the application |

### Sample Usage Flow 📝

1. **Start the application** - The system comes pre-loaded with sample books and members
2. **View available books** (Option 1) to see what's in the library
3. **View members** (Option 2) to see registered users
4. **Borrow a book** (Option 4):
   - Enter the book ID (from the books list)
   - Enter the member ID (from the members list)
5. **Check borrowed books** (Option 9) to see what a member has borrowed
6. **Return books** (Option 5) when done reading

### Business Rules 📜

- **Loan Period:** 14 days from borrowing date
- **Borrowing Limit:** Maximum 3 books per member
- **Overdue Tracking:** System automatically tracks and displays overdue books
- **Search:** Case-insensitive search by book title or author name

### Sample Data 📊

The application comes with pre-loaded sample data:

**Books:**
- The Great Gatsby by F. Scott Fitzgerald
- To Kill a Mockingbird by Harper Lee
- 1984 by George Orwell
- Pride and Prejudice by Jane Austen
- And more classic literature...

**Members:**
- John Doe (john.doe@email.com)
- Jane Smith (jane.smith@email.com)
- Bob Johnson (bob.johnson@email.com)

## Technical Details ⚙️

- **Framework:** .NET 8.0
- **Language:** C# with nullable reference types enabled
- **Architecture:** Object-oriented design with separation of concerns
- **UI:** Console-based interface with emoji indicators
- **Data Storage:** In-memory (data resets on application restart)

## Future Enhancements 🔮

- Database integration for persistent storage
- Fine calculation for overdue books
- Book categories and genres
- Advanced search filters
- Member borrowing history
- Export
