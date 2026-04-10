# 🌱 Automated Greenhouse Management System

## 📌 Overview

The **Automated Greenhouse Management System** is a microservices-based application designed to monitor and control greenhouse conditions efficiently. It uses **Spring Boot, Spring Cloud, and Microservices Architecture** to ensure scalability, flexibility, and maintainability.

The system manages:

- 🌡 Temperature & Humidity  
- 💧 Irrigation  
- 🌿 Plant Monitoring  
- 📊 Data Analysis  

---
## 🏗️ Architecture

This project follows a **Microservices Architecture** with the following components:

- **Eureka Server** – Service discovery  
- **Config Server** – Centralized configuration management  
- **API Gateway** – Routing and filtering  
- **Domain Services** – Core business logic (Greenhouse services)  

---

## ⚙️ Technologies Used

- Java 17+  
- Spring Boot  
- Spring Cloud (Eureka, Config, Gateway)  
- Maven  
- REST APIs  

---

## 📂 Project Structure

│
├── eureka-server/

├── config-server/

├── api-gateway/

├── greenhouse-service/

├── irrigation-service/

├── monitoring-service/

└── README.md


## 🛠️ Technology Stack

| Component               | Technology                               |
|-------------------------|------------------------------------------|
| **Framework**           | Spring Boot 3.2.2, Spring Cloud 2023.0.0 |
| **Service Registry**    | Netflix Eureka                           |
| **API Gateway**         | Spring Cloud Gateway + JWT               |
| **Config Server**       | Spring Cloud Config (Native/Git)         |
| **Inter‑Service Comm.** | OpenFeign                                |
| **Database**            | MySQL 8.0 (Automation), H2 (others)      |
| **External IoT API**    | REST (http://104.211.95.241:8080/api)    |
| **Build Tool**          | Maven                                    |
| **Language**            | Java 17                                  |

## 📦 Prerequisites

Before you begin, ensure you have the following installed:

- **Java 17** (JDK 17 or later)
- **Maven** (3.8+)
- **MySQL** (8.0+) – for Automation Service logs
- **Git** (optional, for cloning)
- **Postman** (for testing APIs)

### Verify installations:
```bash
java -version      # Should show 17.x.x
mvn -version       # Should show 3.8+
mysql --version    # Should show 8.0.x
```
## ▶️ Step-by-Step Startup Guide

⚠️ **IMPORTANT:** Start services in the correct order  

---

### 1️⃣ Start Config Server (Port 8888)

```bash
cd config-server
mvn clean spring-boot:run
```
### 2️⃣ Start Eureka Server (Port 8761)

```bash
cd ../eureka-server
mvn clean spring-boot:run
```
### 3️⃣ Start API Gateway (Port 8080)

```bash
cd ../api-gateway
mvn clean spring-boot:run
```

### 4️⃣ Start Domain Services

### 🌿Zone Service (Port 8081)
```bash
cd ../zone-service
mvn clean spring-boot:run
```

### 💧Sensor Telemetry Service (Port 8082)
```bash
cd ../sensor-telemetry-service
mvn clean spring-boot:run
```

### 📊Automation Service (Port 8083)
```bash
cd ../automation-service
mvn clean spring-boot:run
```

### 📊 Features
---
- Real-time greenhouse monitoring
- Automated irrigation control
- Centralized configuration
- Service discovery using Eureka
- Scalable microservices design

👩‍💻 Author
---

Yehara Nethsilu
