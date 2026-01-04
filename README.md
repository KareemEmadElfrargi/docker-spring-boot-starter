# 🐳 Spring Boot + PostgreSQL Docker Starter

A production-ready template for running a **Spring Boot** application with a **PostgreSQL** database using **Docker Compose**.
This setup ensures a consistent development environment without requiring local Java or PostgreSQL installations.

##  Tech Stack
* **Java 21** (Temurin Alpine Image)
* **Spring Boot 3** (Web & Data JPA)
* **PostgreSQL 15** (Alpine Image)
* **Docker & Docker Compose**

---

##  Getting Started

### Prerequisites
* [Docker Desktop](https://www.docker.com/products/docker-desktop/) must be installed and running.

### Step 1: Build the Application
Before running Docker, you must build the JAR file.
We use the **Maven Wrapper** so you don't need Maven installed globally.

**For Windows (PowerShell / CMD):**
```powershell
.\mvnw.cmd clean package -DskipTests
```
**For Mac / Linux:**
```
.\mvnw.cmd clean package -DskipTests
```

* Note: If you modify the Java code, you must re-run this command to update the JAR file.

### Step 2: Run with Docker
Start the application and database containers:
```powershell
docker compose up --build
```
The `--build` flag ensures Docker recreates the image with the latest JAR file.

## Verification
Once the logs show `Started Task1Application`, verify the setup:
1. API Check: Open your browser to `http://localhost:8080/hello` (Expected Output: Docker is working! 🐳)

![Project Output Screenshot](https://github.com/KareemEmadElfrargi/docker-spring-boot-starter/blob/main/Screenshot%20Output.png)

3. Database: The app will automatically connect to the PostgreSQL container using the credentials defined in `docker-compose.yml`

## Project Structure

1. `Dockerfile`: Instructions to containerize the Spring Boot application.
2. `docker-compose.yml`: Orchestrates the App and Database services.
3. `src/main/resources/application.properties`: Configuration (overridden by Docker environment variables).

---

##  Summary & Resources
I have prepared a detailed summary and guide for this project. You can access the full documentation and resources on Google Drive:

| **[Download Summary & Resources](Comming Soon)**


