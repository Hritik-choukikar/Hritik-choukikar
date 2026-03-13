# 🚀 Scalable Streaming Platform – Microservices Architecture

![GitHub Org](https://img.shields.io/badge/GitHub-Organization-blue?logo=github&style=for-the-badge)
![CI/CD](https://img.shields.io/badge/CI%2FCD-GitHub_Actions-2088FF?logo=github-actions&style=for-the-badge)
![Kubernetes](https://img.shields.io/badge/Kubernetes-Ready-326CE5?logo=kubernetes&style=for-the-badge)
![Docker](https://img.shields.io/badge/Docker-Images-2496ED?logo=docker&style=for-the-badge)

👋 **Welcome to my flagship project!**  
Because of the massive scale and modularity of this system, **the codebase is not held in a single repository.** Instead, it is distributed across multiple independent microservices housed within a dedicated GitHub Organization.

### 👉[Click here to explore the full GitHub Organization and its Repositories!](https://github.com/orgs/Stream-Service/repositories) 👈

---

## 📖 About the Project

This project is a fully functional, highly scalable **Streaming Platform**. It handles user authentication, video uploads, compression, real-time streaming, and notifications. 

By utilizing a microservices architecture orchestrated via **Kubernetes**, each service can be scaled, updated, and deployed independently using automated **GitHub Actions CI/CD** pipelines.

---

## 🔗 The Microservices (Organization Repositories)

All source code is maintained within the Organization. Click on any service below to dive into the code:

| Service | Responsibility | Repository Link |
|---------|----------------|-----------------|
| 🔐 **Auth Service** | Handles user authentication, registration, and JWT token management. | [View Repo](https://github.com/stream-service/Authentication) |
| 📹 **Streaming Service** | Core service for streaming video content to the end user. | [View Repo](https://github.com/stream-service/streaming) |
| 🗜️ **Compression Service** | Asynchronously compresses raw video uploads into multiple optimized formats. | [View Repo](https://github.com/stream-service/compression) |
| 📝 **Posting Service** | Manages content posting, metadata, user feeds, and interactions. | [View Repo](https://github.com/stream-service/posting) |
| 🔔 **Notification Service**| Manages real-time alerts and user notifications. | [View Repo](https://github.com/stream-service/Notification) |
| 🔍 **Search Service** | Provides fast querying to search for users and video content. | [View Repo](https://github.com/stream-service/searching) |
| 💻 **Frontend** | The UI providing a seamless user experience, connecting to backends via API Gateway. | [View Repo](https://github.com/my-org/frontend) |

---

## 🏗️ System Architecture

The entire ecosystem communicates through an API Gateway, ensuring secure and routed internal traffic to the corresponding microservices and their isolated databases.

```mermaid
graph TD
    User[Frontend UI] -->|HTTPS| API_Gateway
    
    API_Gateway --> Auth_Service
    API_Gateway --> Posting_Service
    API_Gateway --> Compression_service
    API_Gateway --> Notification_Service
    API_Gateway --> Streaming_Service
    API_Gateway --> Follow_Service
    API_Gateway --> Searching_service
    
    Auth_Service --> DB[(Auth DB)]
    Follow_Service --> DB2[(Follow DB)]
    Posting_Service --> DB3[(Posts DB)]
    Compression_service --> DB4[(Compression DB)]
    Streaming_Service --> DB5[(Streaming DB)]
    Searching_service--> DB6[(Search DB)]
    Notification_Service --> DB7[(Notification DB)]
