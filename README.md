# King-In-N-Out-Books

King-In-N-Out-Books is a Node.js RESTful API for managing a bookstore's inventory and user authentication. The project demonstrates TDD principles, error handling, and schema validation using Express, AJV, and Jest.

## Features

- **Book Management**: Add, update, delete, and retrieve books.
- **User Authentication**: Login with email and password.
- **Security Questions**: Verify users via security questions for account recovery.
- **Input Validation**: Uses AJV for request body validation.
- **Error Handling**: Consistent error responses for invalid input and server errors.
- **Testing**: Comprehensive test suite using Jest and Supertest.

## API Endpoints

### Books

- `GET /api/books`  
  Retrieve all books.

- `GET /api/books/:id`  
  Retrieve a book by ID.

- `POST /api/books`  
  Add a new book.  
  **Body:** `{ "id": Number, "title": String, "author": String }`

- `PUT /api/books/:id`  
  Update a book by ID.  
  **Body:** `{ "title": String, "author": String }`

- `DELETE /api/books/:id`  
  Delete a book by ID.

### Users

- `POST /api/login`  
  Authenticate a user.  
  **Body:** `{ "email": String, "password": String }`

- `POST /api/users/:email/verify-security-question`  
  Verify security questions for a user.  
  **Body:** `{ "answer1": String, "answer2": String }`

## Getting Started

### Prerequisites

- Node.js (v16+ recommended)
- npm

### Installation

```sh
npm install
```

### Running the Application

Start the server:

```sh
npm start
```

The server will run at [http://localhost:3000](http://localhost:3000).

### Development Mode

For automatic restarts on file changes:

```sh
npm run dev
```

### Running Tests

```sh
npm test
```

## Project Structure

```
.
├── bin/
│   └── www                # Server entry point
├── database/
│   ├── books.js           # Book data and collection logic
│   ├── collection.js      # In-memory collection class
│   └── users.js           # User data and collection logic
├── src/
│   └── app.js             # Express app and API routes
├── test/
│   └── app.spec.js        # Jest/Supertest API tests
├── package.json
└── README.md
```

## License

MIT

---

**Author:** Professor Krasso  
**Student:** Robert King
