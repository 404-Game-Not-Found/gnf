# Web Application Design Document: Game Showcase

## 1. Introduction

### 1.1 Purpose

The purpose of this document is to outline the design and architecture of the Game Showcase web application. This application is designed to display games that have been developed and allow users to read articles about the games.

### 1.2 Scope

The Game Showcase web application consists of four main components:

1. Angular-based Frontend for public viewing
2. Rust-based Backend for reading data
3. React-based Frontend for management of the Public site
4. Go-based Backend for writing data

## 2. Application Components

### 2.1 Angular-based Frontend for Public Viewing

#### Features:

- Displays a list of games with details.
- Provides search and filter functionality for users.
- Allows users to view game details and articles related to the game.

#### Technologies:

- Angular
- HTML/CSS
- JavaScript/TypeScript
- RESTful API for data retrieval

### 2.2 Rust-based Backend for Reading Data

#### Features:

- Handles requests from the Angular-based frontend.
- Retrieves game data and articles from the SQLite database.
- Provides data in a structured JSON format.

#### Technologies:

- Rust
- SQLite database for data storage
- RESTful API for data retrieval

### 2.3 React-based Frontend for Article Management

#### Features:

- Allows administrators to create, edit, and delete articles about games.
- Supports rich text editing for article content.
- Provides user authentication for article management.

#### Technologies:

- React
- HTML/CSS
- JavaScript/TypeScript
- RESTful API for article management
- User authentication (JWT or OAuth)

### 2.4 Go-based Backend for Writing Data

#### Features:

- Accepts requests from the React-based frontend for article management.
- Manages and stores articles in the SQLite database.
- Supports user authentication and authorization for article management.

#### Technologies:

- Go
- SQLite database for data storage
- RESTful API for article management
- User authentication (JWT or OAuth)

## 3. Architecture

The Game Showcase application will follow a client-server architecture. The frontends (Angular and React) will act as clients, making requests to their respective backends (Rust and Go) for data retrieval and management.

### 3.1 Frontend-Backend Communication

- Angular-based Frontend communicates with the Rust-based Backend to retrieve game data and articles for public viewing.
- React-based Frontend communicates with the Go-based Backend to create, edit, and delete articles.

### 3.2 Data Storage

- Game and article data is stored in an SQLite database.
- The Rust-based Backend handles data retrieval.
- The Go-based Backend handles data writing.

### 3.3 User Authentication

- User authentication is required for article management.
- JWT or OAuth can be used for user authentication in both the React and Go components.

## 4. Security

Security is of utmost importance in the Game Showcase application:

- Implement proper input validation to prevent SQL injection and other security vulnerabilities.
- Use HTTPS to secure data transmission between clients and servers.
- Implement user authentication and authorization for article management.

## 5. Deployment

- Deployment should be done in a production-ready environment.
- Containerization (e.g., Docker) and orchestration (e.g., Kubernetes) can be considered for scalability and ease of management.

## 6. Future Enhancements

- Implement user reviews and ratings for games.
- Add user comments and discussion sections for articles.
- Consider integrating with a CDN for media files, such as game screenshots and images.

## 7. Conclusion

The Game Showcase web application is designed to showcase games and provide a platform for managing articles about those games. With a clear separation of frontends and backends, it ensures scalability and modularity, while also focusing on security and user authentication.

This design document serves as a guide for development, ensuring a systematic and organized approach to building the application.