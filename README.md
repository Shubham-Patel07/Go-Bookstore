# Go-Bookstore API

## Overview
Go-Bookstore API is a robust and efficient API designed for managing a library's book inventory. It supports operations to fetch, view, and update the list and status of books, facilitating seamless integration for library management systems.

## Features
- Fetch a list of all books available in the library
- View details of a specific book
- Update the status of a book (e.g., available, checked out, reserved)
- Add new books to the inventory
- Remove books from the inventory

## Technologies Used
- **Programming Language:** Go (Golang)
- **Database:** MySQL
- **API Architecture:** RESTful
- **Dependencies:**
  - [github.com/go-sql-driver/mysql v1.5.0](https://github.com/go-sql-driver/mysql)
  - [github.com/gorilla/mux v1.8.1](https://github.com/gorilla/mux)
  - [github.com/jinzhu/gorm v1.9.16](https://github.com/go-gorm/gorm)
  - [github.com/jinzhu/inflection v1.0.0](https://github.com/jinzhu/inflection)

## Getting Started

### Prerequisites
- Go 1.16+ installed
- MySQL installed and running

### Installation
1. **Clone the repository:**
    ```bash
    git clone https://github.com/yourusername/go-bookstore.git
    ```
2. **Navigate to the project directory:**
    ```bash
    cd go-bookstore
    ```
3. **Install dependencies:**
    ```bash
    go mod tidy
    ```

### Database Setup
1. **Create a MySQL database:**
    ```sql
    CREATE DATABASE bookstore;
    ```
2. **Run the provided SQL script to set up the tables:**
    ```bash
    mysql -u yourusername -p bookstore < schema.sql
    ```

### Configuration
Create a `.env` file in the project root with the following environment variables:
```env
DB_HOST=localhost
DB_PORT=3306
DB_USER=yourusername
DB_PASSWORD=yourpassword
DB_NAME=bookstore
```
## API Endpoints

### Create a new book
```
POST /book/
``` 
Adds a new book to inventory

### Lists all books
```
GET /book/
``` 
Retrieves a list of all books in the library.

### View Book Details
```
GET /book/{bookId}
``` 
Retrieves details of a specific book by its ID.

### Update Book Status
```
PUT /book/{bookId}
``` 
Updates the status of a book.

### Delete a Book
```
DELETE /book/{bookId}
``` 
Removes a book from the inventory.