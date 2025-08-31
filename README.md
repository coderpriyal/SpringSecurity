# Library Management System (Spring Boot + Spring Security)

A simple Library Management System built using Spring Boot and Spring Security demonstrating basic authentication and role-based authorization with in-memory user management.
The application includes public pages, role-specific access to book management, reservations, and admin reports. Custom login and access denied pages are implemented with Thymeleaf templates and basic styling.

## How to Run
- Import as Maven project
- Run `LibraryApplication.java`
- Access: http://localhost:8080

## Credentials

| Username  | Password    | Role      |
|-----------|-------------|-----------|
| admin     | admin123    | ADMIN     |
| lib123    | lib123      | LIBRARIAN |
| student   | student123  | STUDENT   |
| guest     | guest123    | GUEST     |

## Endpoints Overview

### Public
- `/` - Home
- `/about` - About
- `/login` - Login
- `/books/public` - Public book list

### Student
- `/books`
- `/books/{id}`
- `/books/{id}/reserve`

### Librarian
- All student endpoints +
- `/books` [POST]
- `/books/{id}` [PUT]
- `/reservations`
- `/reservations/{id}/approve`

### Admin
- All librarian endpoints +
- `/books/{id}` [DELETE]
- `/users`
- `/admin/reports`

## Screenshots
_(Include login screen, home page, access denied, etc.)_

## Test Results
_(Include terminal or Postman screenshots confirming role-based access)_
