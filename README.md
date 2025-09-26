# CI/CD Pipeline: Automated Deployment to AWS ECS Fargate

## TL;DR
This project demonstrates a full CI/CD lifecycle. A Jenkins pipeline automates building a Java application, containerizing it with Docker, pushing it to AWS ECR, and triggering an automated deployment to a serverless environment on AWS ECS and Fargate.

## Workflow

• Developer pushes to GitHub

• Jenkins: build + unit tests + code style + SonarQube analysis → Quality Gate

• On pass: build multi‑stage Docker image and push to Amazon ECR

• Deploy: Amazon ECS (Fargate) pulls the latest image and runs the container behind an ALB

## Tech Stack

• CI/CD: Jenkins, Jenkins Pipeline (Groovy)

• Containerization: Docker

• Cloud & Deployment: AWS (ECS, Fargate, ECR, ALB, IAM)

• Application: Java, Maven

• Code Quality: SonarQube

• Infrastructure Scripting: AWS CLI

