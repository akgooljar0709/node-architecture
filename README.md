# Node-architecture
Modular Clean Architecture (with Dependency Injection &amp; Layered Abstractions)

# 🔹 "Node.js Clean Architecture with Provider-Consumer Pattern"
📦 Architecture Characteristics:
Layer / Concept	Description
Domain Layer	Contains core business logic (DTOs, interfaces)
Application Layer	Use cases — orchestrates business rules via services
Infrastructure Layer	API implementations, external resources (APIs, DBs)
Interface Layer	HTTP controllers (express handlers)
Provider Layer	Registers dependencies (DI container)
Router Layer	Central routing logic
Shared Layer	Utilities, constants (e.g., logger, HTTP status, path constants)
Mock Layer	Mock data for development or testing
server.ts	App entry point with minimal setup
