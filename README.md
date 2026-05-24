# Nilachakra Platform

Central orchestration repository for the Nilachakra Microservices Ecosystem.

This repository aggregates all backend services and frontend applications into a unified development workspace using Git Submodules.

---

# Architecture Overview

```text
                    +----------------------+
                    |   Angular Frontend   |
                    |   nilachakra-ui      |
                    +----------+-----------+
                               |
                               v
                    +----------------------+
                    | API Gateway Service  |
                    |  nilachakra-gateway |
                    +----------+-----------+
                               |
        -------------------------------------------------
        |                       |                       |
        v                       v                       v

+----------------+   +----------------------+   +----------------------+
| Auth Service   |   | Brain Service        |   | Repository Service   |
| Authentication |   | AI / Business Logic  |   | Data Management      |
+----------------+   +----------------------+   +----------------------+
```

---

# Repositories

## Backend Services

| Service                   | Description                              |
| ------------------------- | ---------------------------------------- |
| `nilachakra-auth-service` | Authentication and authorization service |
| `nilachakra-brain`        | Core AI and business logic service       |
| `nilachakra-gateway`      | API Gateway and request routing          |
| `nilachakra-repository`   | Repository and persistence service       |

---

## Frontend

| Application     | Description                  |
| --------------- | ---------------------------- |
| `nilachakra-ui` | Angular frontend application |

---

# Technology Stack

## Backend

* Java
* Spring Boot
* Spring Cloud
* Microservices Architecture
* REST APIs

---

## Frontend

* Angular
* TypeScript
* RxJS

---

# Repository Structure

```text
nilachakra-platform/
│
├── services/
│   ├── nilachakra-auth-service/
│   ├── nilachakra-brain/
│   ├── nilachakra-gateway/
│   └── nilachakra-repository/
│
├── frontend/
│   └── nilachakra-ui/
│
├── .gitmodules
└── README.md
```

---

# Clone Project

```bash
git clone --recurse-submodules https://github.com/pravudatta10/nilachakra-platform.git
```

If already cloned:

```bash
git submodule update --init --recursive
```

---

# Development Workflow

## Working on a Service

Example:

```bash
cd services/nilachakra-brain
```

Commit normally:

```bash
git add .
git commit -m "feature implementation"
git push
```

---

## Update Platform Reference

After updating a submodule:

```bash
cd ../../

git add services/nilachakra-brain

git commit -m "Updated brain service reference"

git push
```

---

# Recommended Local Ports

| Service            | Port |
| ------------------ | ---- |
| Gateway            | 8080 |
| Auth Service       | 8081 |
| Brain Service      | 8082 |
| Repository Service | 8083 |
| Angular UI         | 4200 |

---

# Future Enhancements

* Kubernetes Deployment
* Helm Charts
* Kafka Integration
* Redis Caching
* OpenTelemetry Tracing
* Prometheus & Grafana Monitoring
* CI/CD Pipelines
* AI RAG Architecture
* GitOps Deployment
* AWS Cloud Deployment

---

# Engineering Goals

* Scalable microservice architecture
* Independent deployable services
* Unified developer workspace
* AI-ready backend ecosystem
* Enterprise-grade orchestration

---

# Author

Pravudatta
Full Stack & Microservices Engineer
