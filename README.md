# 🚀 Streaming Platform – Microservices Project

![GitHub Org](https://img.shields.io/badge/GitHub-my--org-blue?logo=github)
![CI/CD](https://img.shields.io/github/actions/workflow/status/my-org/infra/ci.yml?label=CI%2FCD)
![Kubernetes](https://img.shields.io/badge/Kubernetes-ready-blue?logo=kubernetes)
![Docker](https://img.shields.io/badge/Docker-images-green?logo=docker)

Welcome to the **Streaming Platform** project!  
This organization hosts multiple microservices that together form a scalable, modular system for authentication, posting, and frontend delivery, all orchestrated via Kubernetes.

---

## 🔗 Repositories

- [Auth Service](https://github.com/my-org/auth-service)  
  Handles user authentication, login, and token management.

- [Posting Service](https://github.com/stream-service/posting)  
  Manages content posting, feeds, and interactions.

- [Frontend](https://github.com/my-org/frontend)  
  Provides the user interface, connecting to backend services via API Gateway.

- [Infra](https://github.com/my-org/infra)  
  Contains Kubernetes manifests, CI/CD pipelines, and deployment configurations.

---

## 🏗️ Architecture

```mermaid
graph TD
    User[Frontend UI] -->|HTTPS| API_Gateway
    API_Gateway --> Auth_Service
    API_Gateway --> Posting_Service
    Auth_Service --> DB[(Auth DB)]
    Posting_Service --> DB2[(Posts DB)]
 
 

 
 

 
 

![Activity Graph](https://github-readme-activity-graph.vercel.app/graph?username=Hritik-choukikar&theme=react-dark)

