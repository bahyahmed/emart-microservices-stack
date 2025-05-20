# EMart Microservices Stack

This repository contains the full Dockerized microservices architecture for the **EMart App**, an e-commerce-style project built using multiple technologies and containerized for deployment.

## 📊 Architecture Diagram

![EMart Architecture](/assets/architecture.png)

## Architecture Overview

This project includes:

- **Angular (Client)** – Frontend single-page application.
- **Node.js (Emart API)** – Handles main business logic and connects to MongoDB.
- **Java Spring Boot (Books API)** – Manages book-related endpoints, connected to MySQL.
- **MongoDB** – Used by Node.js API to store Emart data.
- **MySQL** – Used by Java API to store book data.
- **Nginx** – Acts as an API Gateway, reverse proxies requests to the correct backend services.

All services are containerized using Docker and orchestrated with Docker Compose.

---

## Project Structure

```
emart-microservices/
├── client/             # Angular frontend
├── nodeapi/            # Node.js backend (Emart API)
├── javaapi/            # Java backend (Books API)
├── nginx/              # Nginx reverse proxy configuration
├── docker-compose.yml  # Multi-container Docker orchestration
└── README.md
```

---

## Getting Started

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/emart-microservices-stack.git
cd emart-microservices-stack
```

### 2. Build and Run the Containers
```bash
docker-compose up --build
```

### 3. Access the App
- Angular frontend: [http://localhost](http://localhost)
- Node.js API: [http://localhost/api](http://localhost/api)
- Java API: [http://localhost/webapi](http://localhost/webapi)

---

## Tech Stack

| Layer         | Technology     |
|---------------|----------------|
| Frontend      | Angular        |
| Backend 1     | Node.js + MongoDB |
| Backend 2     | Java (Spring Boot) + MySQL |
| API Gateway   | Nginx          |
| Containerization | Docker & Docker Compose |

---

## Deployment

This project is designed to be run on any server with Docker support. It's already been successfully deployed on an **AWS EC2 instance** using Docker Engine.

---

## License

This project is open-source and free to use for educational and development purposes.

