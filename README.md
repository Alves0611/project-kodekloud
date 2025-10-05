# 🚀 Solar System - Advanced CI/CD Pipeline

[![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=github-actions&logoColor=white)](https://github.com/features/actions)
[![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)](https://www.docker.com/)
[![Kubernetes](https://img.shields.io/badge/kubernetes-%23326ce5.svg?style=for-the-badge&logo=kubernetes&logoColor=white)](https://kubernetes.io/)
[![AWS](https://img.shields.io/badge/AWS-%23FF9900.svg?style=for-the-badge&logo=amazon-aws&logoColor=white)](https://aws.amazon.com/)
[![Node.js](https://img.shields.io/badge/node.js-6DA55F?style=for-the-badge&logo=node.js&logoColor=white)](https://nodejs.org/)

> **A project demonstrating advanced DevOps practices with complete CI/CD pipeline, containerization, Kubernetes deployment, and automated monitoring.**

## 📋 Overview

This project presents an application built with **Node.js** and **Express**, implementing a robust CI/CD pipeline that demonstrates modern DevOps best practices. The pipeline includes security analysis, automated testing, code coverage, containerization, multi-environment deployment, and integrated notifications.

## 🏗️ Pipeline Architecture

![Pipeline CI/CD](images/pipeline.drawio.svg)


## 🛠️ Technologies Used

### **DevOps & CI/CD**
- **GitHub Actions** - Automation and CI/CD
- **Docker** - Containerization
- **Kubernetes** - Container orchestration
- **AWS EKS** - Managed Kubernetes
- **AWS S3** - Artifact storage

### **Testing & Quality**
- **Mocha** - Testing framework
- **Chai** - Assertion library
- **NYC** - Code coverage
- **CodeQL** - Security analysis

### **Monitoring**
- **Slack** - Notifications

### **Container Registry**
- **Docker Hub** - Public registry
- **GitHub Container Registry** - Private registry

## 🚀 Pipeline Features

### **1. Security Analysis (CodeQL)**
- ✅ Static JavaScript code analysis
- ✅ Automatic vulnerability detection
- ✅ GitHub Security Advisory integration

### **2. Automated Testing**
- ✅ **Matrix Testing**: Node.js 18 and 20
- ✅ **Unit Tests**: Mocha with Chai
- ✅ **Coverage**: 90% minimum coverage
- ✅ **Database Testing**: MongoDB container for tests

### **3. Smart Containerization**
- ✅ **Multi-stage Build**: Image optimization
- ✅ **Security Scanning**: Vulnerability analysis
- ✅ **Health Checks**: Functionality validation
- ✅ **Multi-registry**: Docker Hub + GitHub Container Registry

### **4. Multi-environment Deployment**
- ✅ **Development**: Automatic deploy for features
- ✅ **Production**: Controlled deploy for main
- ✅ **Kubernetes**: Deploy to AWS EKS
- ✅ **Secrets Management**: Secure credential management

### **5. Monitoring and Notifications**
- ✅ **Slack Integration**: Real-time notifications
- ✅ **Artifact Storage**: S3 reports
- ✅ **Status Tracking**: Deployment monitoring

## 📁 Project Structure

```
github-actions/
├── .github/
│   ├── workflows/
│   │   ├── solar-system.yml          # Main pipeline
│   │   ├── codeql-analysis.yml       # Security analysis
│   │   └── reusable-deployment.yml   # Reusable deploy
│   └── custom-actions/
│       └── npm-action/               # Custom action
├── kubernetes/
│   ├── development/                  # Dev manifests
│   └── production/                   # Prod manifests
├── images/                           # Assets and diagrams
├── app.js                           # Main application
├── Dockerfile                       # Containerization
└── package.json                     # Dependencies
```

## 🔧 Setup and Deploy

### **Prerequisites**
- GitHub Repository
- AWS Account (EKS, S3)
- Docker Hub Account
- Slack Workspace

### **Required Secrets**
```bash
# MongoDB
MONGO_USERNAME, MONGO_PASSWORD, MONGO_URI

# Docker
DOCKER_USERNAME, DOCKER_PASSWORD

# AWS
AWS_ACCESS_KEY_ID, AWS_SECRET_ACCESS_KEY
EKS_CLUSTER_NAME

# Notifications
SLACK_WEBHOOK_URL
```

### **Automatic Deploy**
```bash
# Development (feature branches)
git push origin feature/new-feature

# Production (main branch)
git push origin main
```

## 📊 Metrics and Quality

| Metric | Value | Status |
|---------|-------|--------|
| **Code Coverage** | 90%+ | ✅ |
| **Security Scan** | CodeQL | ✅ |
| **Node.js Versions** | 18, 20 | ✅ |
| **Deploy Time** | < 5min | ✅ |
| **Uptime** | 99.9% | ✅ |

## 🎯 Implemented Features

### **Pipeline Features**
- 🔒 **Security First**: Security analysis on every commit
- 🧪 **Comprehensive Testing**: Unit tests with coverage
- 🐳 **Container Strategy**: Multi-registry deployment
- ☸️ **Kubernetes Native**: Native K8s deploy
- 📱 **Real-time Monitoring**: Slack notifications
- 🔄 **Environment Parity**: Dev/Prod consistency

### **DevOps Best Practices**
- ✅ **Infrastructure as Code**: Kubernetes manifests
- ✅ **Secrets Management**: Kubernetes secrets
- ✅ **Artifact Management**: S3 storage
- ✅ **Rollback Strategy**: Blue-green deployment ready
- ✅ **Monitoring**: Health checks and status tracking


## 📈 Roadmap

- [ ] **Multi-region Deployment**
- [ ] **Advanced Monitoring** (Prometheus/Grafana)
- [ ] **Auto-scaling** based on metrics
- [ ] **Canary Deployments**
- [ ] **Automated Integration Tests**
- [ ] **Performance Testing**
