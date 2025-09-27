# Event Management & Registration REST API

A REST API for managing and booking events, built with **Go** and the **Gin** framework. Users can sign up, create and manage their own events, or register for events created by others.

## ✨ Features

-   **Authentication & Authorization**: Secure registration and login system with **JWT** tokens and **Bcrypt** password hashing.
-   **Authorization Logic**: A key feature is the authorization control, ensuring that users can only edit or delete the events they have created themselves.
-   **Full Event Management (CRUD)**: Authenticated users can create, view, update, and delete events.
-   **Event Registration System**: Users can register for any existing event and also cancel their registration.
-   **Public and Private APIs**: Endpoints for public viewing of events (no token required) and protected endpoints for actions that require authentication.

## 🛠️ Tech Stack

-   **Language**: Go
-   **Web Framework**: Gin
-   **Database**: SQLite
-   **Authentication**: JWT
-   **Password Security**: Bcrypt

## 📄 API Endpoints

| Method   | Path                       | Description                        | Auth Required |
| :------- | :------------------------- | :--------------------------------- | :-----------: |
| `POST`   | `/signup`                  | Register a new user                |      No       |
| `POST`   | `/login`                   | Log in and receive a token         |      No       |
| `GET`    | `/events`                  | View a list of all events          |      No       |
| `GET`    | `/events/:id`              | View a specific event              |      No       |
| `POST`   | `/events`                  | Create a new event                 |      Yes      |
| `PUT`    | `/events/:id`              | Update an event (owned by the user)|      Yes      |
| `DELETE` | `/events/:id`              | Delete an event (owned by the user)|      Yes      |
| `POST`   | `/events/:id/register`     | Register for an event              |      Yes      |
| `DELETE` | `/events/:id/register`     | Cancel a registration              |      Yes      |

## 🚀 Getting Started

1.  Clone the repository:
    ```bash
    git clone https://github.com/AryaTabani/REST-API-Go-project.git
    cd REST-API-Go-project
    ```
2.  Install dependencies:
    ```bash
    go mod tidy
    ```
3.  Run the application:
    ```bash
    go run main.go
    ```
