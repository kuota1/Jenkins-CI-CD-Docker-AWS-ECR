# Jenkins CI/CD with Docker and AWS ECR

This project demonstrates a complete CI/CD pipeline using **Jenkins**, **Docker**, **SonarQube**, **Nexus**, and **AWS Elastic Container Registry (ECR)**. It is divided into two main phases:

- `jenkins-project`: Focuses on building the WAR file and performing code quality analysis.
- `jenkins-docker`: Focuses on containerizing the application and deploying it to AWS ECR.

## Project Structure

```plaintext
.
├── jenkins-project/
│   ├── Jenkinsfile
│   └── screenshots/
├── jenkins-docker/
│   ├── PAAC_CI_DockerECR.groovy
│   └── screenshots/
├── nexus-setup.sh
├── sonar-setup.sh
└── README.md
Tools Used
Jenkins – automation server for building and deploying applications

Docker – container platform to build and push images

AWS ECR – private container registry for Docker images

SonarQube – static code analysis for quality and security

Nexus Repository Manager – artifact repository

Maven – build tool for Java applications

Setup Scripts
nexus-setup.sh: Script to install and configure Nexus on a CentOS/RHEL server.

sonar-setup.sh: Script to install and configure SonarQube with PostgreSQL on Ubuntu.

Pipeline Features
Pulls code from GitHub

Builds using Maven (skipping tests during packaging)

Runs unit tests

Performs static analysis with Checkstyle and SonarQube

Publishes build artifacts to Nexus

Builds Docker images

Pushes images to AWS ECR

(Optional) Deploys images to AWS ECS

Screenshots
Each folder includes screenshots of:

EC2 and Jenkins setup

Pipeline runs and output

SonarQube and Nexus configuration

AWS ECR interaction

Final image pushed

Artifacts
WAR files are archived as build artifacts

Docker images tagged with build number and latest

Artifacts are also pushed to Nexus (in jenkins-project)

Disclaimer
This repository is for educational purposes. Some setup scripts and configurations were based on third-party sources, and no application logic is included. The captured project illustrates a general CI/CD setup with multiple integrated tools, and is not tied to any specific commercial product or proprietary source code.
    

## Author

Roberto Rodríguez - [GitHub](https://github.com/kuota1)