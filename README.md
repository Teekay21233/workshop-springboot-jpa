# 🏷️ Course Application

A **RESTful API** built with **Spring Boot** for managing users, orders, products, and categories.  
The project follows clean architecture principles with well-defined layers: **entities, repositories, services, controllers**, and **centralized exception handling**.

## 🚀 Technologies Used

- **Java 17+**
- **Spring Boot 3**
- **Spring Web**
- **Spring Data JPA**
- **H2 Database** (for testing)
- **Maven**

## 📌 Features

- **Users**
  - Create (`POST /users`)
  - List (`GET /users`)
  - Find by ID (`GET /users/{id}`)
  - Update (`PUT /users/{id}`)
  - Delete (`DELETE /users/{id}`)  
    - Returns **404** if the user does not exist  
    - Returns **400** if there is a database integrity violation (e.g., user has linked orders)

- **Orders, Categories, and Products**
  - CRUD operations with proper entity relationships

- **Global Exception Handling**
  - `ResourceNotFoundException` → HTTP 404
  - `DatabaseException` → HTTP 400
  - Error response format:
    ```json
    {
      "timestamp": "2025-09-25T13:15:30.123Z",
      "status": 404,
      "error": "Resource not found",
      "message": "Resource not found. Id 999",
      "path": "/users/999"
    }
    ```

## 🛠️ Prerequisites

- [Java 17+](https://adoptium.net/)
- [Maven](https://maven.apache.org/)


