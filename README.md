# Expense Tracker

A Golang project for tracking user expenses, designed with **Clean Architecture** principles for scalability and maintainability.

---

## 🚀 Features

- **User Management**: Register, login, and manage users.
- **Expense Tracking**: Add, edit, delete, and view expenses.
- **Category & Date Filtering**: Organize expenses by categories or filter by date.
- **Secure Authentication**: Password hashing and JWT-based authentication.

---

## 🛠️ Project Structure

The project follows the **Clean Architecture** pattern:

```plaintext
expense-tracker/
├── cmd/                 # Application entry point
│   └── main.go          # Main application logic
├── config/              # Configuration management
│   └── config.go
├── internal/            # Internal application logic
│   ├── entity/          # Business models
│   │   └── expense.go
│   ├── usecase/         # Core business use cases
│   │   └── expense_usecase.go
│   ├── repository/      # Data storage and retrieval
│   │   └── expense_repository.go
│   ├── delivery/        # Delivery mechanisms (HTTP, gRPC, etc.)
│   │   ├── http/
│   │   │   └── expense_handler.go
│   │   └── middleware/
│   │       └── auth_middleware.go
│   └── utils/           # Utility functions
│       ├── jwt.go
│       ├── hash.go
│       └── response.go
├── migrations/          # Database migration files
├── docs/                # Documentation
│   └── README.md
└── go.mod               # Dependency management
```

---

## 🛆 Installation

### Prerequisites

Make sure you have the following installed on your system:

- [Golang](https://go.dev/dl/) (v1.20 or higher)
- PostgreSQL (or another preferred database)

### Steps

1. Clone this repository:

   ```bash
   git clone https://github.com/<your-username>/expense-tracker.git
   cd expense-tracker
   ```

2. Install dependencies:

   ```bash
   go mod tidy
   ```

3. Create a `.env` file with the following content:

   ```env
   DB_HOST=localhost
   DB_PORT=5432
   DB_USER=your_db_user
   DB_PASSWORD=your_db_password
   DB_NAME=expense_tracker
   JWT_SECRET=your_jwt_secret
   ```

4. Apply database migrations:

   ```bash
   go run cmd/migrate.go
   ```

5. Run the application:
   ```bash
   go run cmd/main.go
   ```

---

## 🔐 API Documentation

Comming soon

## 🛠️ Contributing

Contributions are welcome! Please fork this repository and create a pull request for any changes or features you'd like to add.

---

## 🖍️ License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## 🤝 Acknowledgements

Special thanks to the Golang community for their support and resources that make learning and development easier!
