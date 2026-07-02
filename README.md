# DevOps Assignment - Spring Boot REST API Deployment on AWS

## Project Overview

This project demonstrates the deployment of a Spring Boot REST API on AWS using Docker, Amazon EC2, Amazon ECR, GitHub Actions, Amazon S3, and Amazon CloudWatch.

The objective is to automate deployment, monitor the application, secure AWS resources, and evaluate application performance through load testing.

---

## Features

- Spring Boot REST API
- Dockerized application
- CI/CD using GitHub Actions
- Docker images stored in Amazon ECR
- Deployment to Amazon EC2
- Application monitoring using Amazon CloudWatch
- Database backup to Amazon S3
- Load testing using k6 (or JMeter)
- IAM least privilege configuration

---

## Architecture

> Insert your architecture diagram here.

Example:

GitHub
↓
GitHub Actions
↓
Amazon ECR
↓
Amazon EC2 (Docker)
↓
Spring Boot API
↓
MySQL

CloudWatch ← Logs & Metrics

S3 ← Database Backups

---

## Technologies Used

| Technology | Purpose |
|------------|---------|
| Java 21 | Backend |
| Spring Boot | REST API |
| Maven | Build Tool |
| Docker | Containerization |
| GitHub Actions | CI/CD |
| Amazon EC2 | Hosting |
| Amazon ECR | Docker Registry |
| Amazon S3 | Backup Storage |
| Amazon CloudWatch | Monitoring |
| MySQL | Database |
| k6/JMeter | Load Testing |

---

## Project Structure

```
project/
├── src/
├── Dockerfile
├── docker-compose.yml
├── pom.xml
├── .github/
│   └── workflows/
├── README.md
```

---

## Prerequisites

- AWS Account
- Docker
- Java 21
- Maven
- Git
- AWS CLI

---

## Local Setup

Clone the repository

```bash
git clone <repository-url>
```

Move into the project

```bash
cd project-name
```

Build the application

```bash
mvn clean package
```

Run locally

```bash
java -jar target/app.jar
```

---

## Docker

Build Image

```bash
docker build -t springboot-app .
```

Run Container

```bash
docker run -p 8080:8080 springboot-app
```

---

## CI/CD Pipeline

The GitHub Actions workflow performs the following steps:

1. Checkout source code
2. Build Maven project
3. Run tests
4. Build Docker image
5. Push image to Amazon ECR
6. Deploy latest image to Amazon EC2

---

## AWS Infrastructure

Services used:

- Amazon EC2
- Amazon ECR
- Amazon S3
- Amazon CloudWatch
- IAM
- Security Groups

---

## Monitoring

CloudWatch monitors:

- CPU Utilization
- Memory Usage
- Disk Usage
- Network Traffic
- Application Logs

CloudWatch Dashboard and Alarm screenshots are included in the report.

---

## Security

Implemented security measures:

- IAM least privilege
- GitHub Secrets for credentials
- Restricted Security Group rules
- No hardcoded AWS credentials
- Docker image pulled using IAM Role

---

## Load Testing

Tool Used:

- k6 (or JMeter)

Metrics collected:

- Average Response Time
- Throughput
- CPU Usage
- Memory Usage
- Error Rate

Results are available in the project report.

---

## Challenges Faced

- Configuring IAM permissions
- Deploying Docker image from ECR
- Setting up CloudWatch Agent
- Managing GitHub Secrets securely

---

## Future Improvements

- Amazon RDS
- Application Load Balancer
- Auto Scaling
- HTTPS with Let's Encrypt
- Kubernetes (Amazon EKS)

---

## Author

Hemanth Chitikela
