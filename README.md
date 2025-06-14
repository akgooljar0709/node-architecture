# 🧱 Node-Architecture

### Modular Clean Architecture (with Dependency Injection & Layered Abstractions)

---

## 🔹 Node.js Clean Architecture with Provider-Consumer Pattern

A scalable and maintainable architecture built using modular layers, separation of concerns, and dependency injection principles.

---

## 📦 Architecture Characteristics

| **Layer / Concept**      | **Description**                                                                 |
|--------------------------|---------------------------------------------------------------------------------|
| **Domain Layer**         | Contains core business logic such as **DTOs**, **interfaces**, and **entities**. |
| **Application Layer**    | Defines **use cases** and orchestrates business rules via **services**.         |
| **Infrastructure Layer** | Implements APIs and handles external resources like **databases**, **APIs**, etc. |
| **Interface Layer**      | HTTP controllers (e.g., **Express handlers**) for user-facing endpoints.         |
| **Provider Layer**       | Registers all **dependencies** using a **DI container** or factory functions.   |
| **Router Layer**         | Defines and organizes **routing logic** for the application.                    |
| **Shared Layer**         | Common utilities such as **loggers**, **HTTP status codes**, **path constants**. |
| **Mock Layer**           | Holds **mock data** and test fixtures for development or automated testing.     |
| **server.ts**            | Entry point of the app. Minimal setup to initialize the app and inject dependencies. |

---

## ✅ Benefits

- Follows **SOLID** principles
- Encourages **testability**, **reusability**, and **decoupling**
- Supports **clean dependency flow** (inward)
- Easy to scale and maintain

---

## 🗂️ Example Folder Structure

src/
├── application/
│ └── use-cases/
├── domain/
│ ├── dtos/
│ └── interfaces/
├── infrastructure/
│ ├── api/
│ └── db/
├── interface/
│ └── controllers/
├── provider/
│ └── container.ts
├── router/
│ └── index.ts
├── shared/
│ ├── constants/
│ └── utils/
├── mock/
│ └── mock-data.ts
└── server.ts



---

## 💡 Notes

- Prefer **dependency injection** over direct instantiation for better testability.
- Define **constants** (HTTP status, paths) in the `shared/constants` folder.
- Use the `provider` layer to bind all your abstractions to their implementations.

---

## 🚀 Getting Started

```bash
# Install dependencies
npm install

# Start development server
npm run dev

# Build for production
npm run build

# Run production server
npm start
