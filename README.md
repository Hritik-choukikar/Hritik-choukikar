# 🚀 Streaming Platform – Microservices Project

![GitHub Org](https://img.shields.io/badge/GitHub-my--org-blue?logo=github)
![CI/CD](https://img.shields.io/github/actions/workflow/status/my-org/infra/ci.yml?label=CI%2FCD)
![Kubernetes](https://img.shields.io/badge/Kubernetes-ready-blue?logo=kubernetes)
![Docker](https://img.shields.io/badge/Docker-images-green?logo=docker)

Welcome to the **Streaming Platform** project!  
This organization hosts multiple microservices that together form a scalable, modular system for authentication, posting, and frontend delivery, all orchestrated via Kubernetes.

---

## 🔗 Repositories

- [Auth Service](https://github.com/stream-service/Authentication)  
  Handles user authentication, login, and token management.

- [Posting Service](https://github.com/stream-service/posting)  
  Manages content posting, feeds, and interactions.

- [Notification Service](https://github.com/stream-service/Notification)  
  Manages Notification

- [Frontend](https://github.com/my-org/frontend)  
  Provides the user interface, connecting to backend services via API Gateway.

 

---

## 🏗️ Architecture

```mermaid
graph TD
    User[Frontend UI] -->|HTTPS| API_Gateway
    API_Gateway --> Auth_Service
    API_Gateway --> Posting_Service
    API_Gateway --> Compression_service
    API_Gateway --> Notification_Service
    API_Gateway --> Streaming_Service
    API_Gateway --> Follow_Service
    Auth_Service --> DB[(Auth DB)]
    Follow_Service --> DB2[(Follow DB)]
    Posting_Service --> DB3[(Posts DB)]
    Compression_service --> DB4[(Compression DB)]
    Streaming_Service --> DB5[(Strteaming DB)]
    Searching_service--> DB6[(Posts DB)]
    Notification_Service --> DB7[(Strteaming DB)]
    
```
 
 ## ⚙️ Tech Stack
    - **Frontend**: HTML,CSS,JS
    - **Backend Services**: Python
    - **Database**: MySQL  
    - **Containerization**: Docker
    - **Orchestration**: Kubernetes (Ingress + LoadBalancer)
    - **CI/CD**: GitHub Actions

 
 

 
 

 

