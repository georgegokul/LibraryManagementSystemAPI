# Library Management API

This project is a simple Library Management API built using Java with Javalin as the web framework and H2 as an in-memory database. The API allows basic CRUD operations for managing authors and books in a library.

## Table of Contents

- [Features](#features)
- [Technologies Used](#technologies-used)
- [Setup and Running the Project](#setup-and-running-the-project)
- [API Endpoints](#api-endpoints)
- [Contributing](#contributing)
- [License](#license)

## Features

- CRUD operations for Books by authors.
- In-memory H2 database for testing
- Clean separation between layers (Controller, Service, DAO)
- Pre-populated sample data for authors and books

## Technologies Used

- **Java**: Core programming language
- **JDBC**: Database operations
- **Javalin**: Lightweight web framework for Java
- **H2 Database**: In-memory database for quick testing and development
- **Maven**: Build automation and dependency management

## Setup and Running the Project

### Prerequisites

Make sure you have the following installed:

- [Java 8+](https://www.oracle.com/java/technologies/javase-jdk8-downloads.html)
- [Maven](https://maven.apache.org/install.html)

### Steps to Run

1. Clone the repository:

    ```bash
    git clone https://github.com/your-username/library-management-api.git
    cd library-management-api
    ```

2. Build the project using Maven:

    ```bash
    mvn clean install
    ```

3. Run the application:

    ```bash
    mvn exec:java -Dexec.mainClass="Application.Application"
    ```

4. The API will be accessible at `http://localhost:8080`.

## API Endpoints

The following endpoints are available to interact with the library system:

### Authors

- **GET /authors**: Get all authors.
- **POST /authors**: Add a new author (JSON body: `{ "name": "Author Name" }`).

### Books

- **GET /books**: Get all books.
- **POST /books**: Add a new book (JSON body: `{ "isbn": 123, "author_id": 1, "title": "Book Title", "copies_available": 5 }`).
- **GET /books/available**: Get all books with `copies_available > 0`.

## Project Structure

- `Application.Model`: Contains the model classes `Author` and `Book`.
- `Application.Service`: Contains the service classes that handle business logic.
- `Application.DAO`: Contains the data access classes for interacting with the database.
- `Application.Controller`: Contains the controller classes that define the API routes.
- `Application.Util`: Contains utility classes like `ConnectionUtil` for managing database connections.

## Contributing

Contributions are welcome! Feel free to submit a pull request or open an issue.

1. Fork the repo.
2. Create a new branch (`git checkout -b feature-branch`).
3. Commit your changes (`git commit -m 'Add new feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Open a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
