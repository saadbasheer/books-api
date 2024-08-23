# Books API with CRUD Operations

A simple RESTful API for managing a collection of books, built with Express and Node.js. This project demonstrates basic CRUD operations and JSON handling using Express.

## Features

- **Create:** Add new books to the collection.
- **Read:** Retrieve all books or a specific book by ID.
- **Update:** Modify the details of an existing book.
- **Delete:** Remove a book from the collection.

## Installation

1. **Clone the repository:**

```bash
   git clone https://github.com/saadbasheer/books-api.git

   cd books-api
```

2. **Install dependencies:**

```bash
npm install

3. **Start the server:**

```bash
npm start
```

The server will run on http://localhost:3000.

## Endpoints
POST /books: Add a new book

Request body:
```json
{
  "title": "Book Title",
  "author": "Author Name"
}
```

- GET /books: Retrieve all books
- GET /books/:id: Retrieve a specific book by ID
- PUT /books/:id: Update a book's details by ID

Request body:
```json
{
  "title": "Updated Title",
  "author": "Updated Author"
}
```
DELETE /books/:id: Delete a book by ID

## Example Usage
Add a new book:
```bash
curl -X POST http://localhost:3000/books -H "Content-Type: application/json" -d '{"title": "1984", "author": "George Orwell"}'
```
Retrieve all books:
```bash
curl http://localhost:3000/books
```
Update a book:
```bash
curl -X PUT http://localhost:3000/books/1 -H "Content-Type: application/json" -d '{"title": "Brave New World", "author": "Aldous Huxley"}'
```
Delete a book:

```bash
curl -X DELETE http://localhost:3000/books/1
```