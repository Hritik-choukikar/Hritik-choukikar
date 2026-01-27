# 🚀 Streaming Platform – Microservices Project

![GitHub Org](https://img.shields.io/badge/GitHub-my--org-blue?logo=github)
![CI/CD](https://img.shields.io/github/actions/workflow/status/my-org/infra/ci.yml?label=CI%2FCD)
![Kubernetes](https://img.shields.io/badge/Kubernetes-ready-blue?logo=kubernetes)
![Docker](https://img.shields.io/badge/Docker-images-green?logo=docker)

Welcome to the **Streaming Platform** project!  
This organization hosts multiple microservices that together form a scalable, modular system for authentication, posting, and frontend delivery, all orchestrated via Kubernetes.

---
## 🔗 Repositories

<div style="display: flex; justify-content: space-between;">

<div>

- [Auth Service](https://github.com/stream-service/Authentication)  
  Handles user authentication, login, and token management.

- [Posting Service](https://github.com/stream-service/posting)  
  Manages content posting, feeds, and interactions.

- [Notification Service](https://github.com/stream-service/Notification)  
  Manages Notification

- [Compression Service](https://github.com/stream-service/compression)  
  Compress videos to multiple formats

</div>

<div>

- [Search](https://github.com/stream-service/searching)  
  A Service to search users

- [Streaming Service](https://github.com/stream-service/streaming)  
  A Service for streaming videos

- [Frontend](https://github.com/my-org/frontend)  
  Provides the user interface, connecting to backend services via API Gateway.

</div>

</div>


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
    API_Gateway --> Searching_service
    Auth_Service --> DB[(Auth DB)]
    Follow_Service --> DB2[(Follow DB)]
    Posting_Service --> DB3[(Posts DB)]
    Compression_service --> DB4[(Compression DB)]
    Streaming_Service --> DB5[(Strteaming DB)]
    Searching_service--> DB6[(Posts DB)]
    Notification_Service --> DB7[(Strteaming DB)]
    
```
 
 ## ⚙️ Tech Stack
- **Frontend**: HTML, CSS, JS
- **Backend Services**: Python
- **Database**: MySQL  
- **Containerization**: Docker
- **Orchestration**: Kubernetes (Ingress + LoadBalancer)
- **CI/CD**: GitHub Actions


 
 

 
 

 

