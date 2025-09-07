# 🍷 Wine Quality Prediction – End-to-End ML Project with MLflow

---

## 📖 Overview

This project implements an **end-to-end machine learning solution** to predict wine quality using **ElasticNet regression**. 

The aim is to assist winemakers in assessing and improving wine quality through data-driven insights.  

- Built a scalable ML pipeline with **MLflow** for experiment tracking, model management, and versioning.
  
- Developed a **Flask web application** for real-time predictions.
  
- Established **CI/CD pipelines** using GitHub Actions for automated deployments.
  
- Successfully deployed on **AWS (EC2, ECR)** and **Azure (Container Registry & Web App)**.  

---

## ❓ Problem Statement

Winemakers often face challenges in assessing wine quality objectively. Traditional methods rely heavily on manual tasting,  
which can be inconsistent and subjective.  

The goal of this project is to: 

- Build a predictive system to **classify wine quality** based on physicochemical properties.
  
- Provide a **web-based tool** for winemakers to upload data and receive instant predictions.
  
- Enable **continuous integration and deployment (CI/CD)** for scalable, production-ready ML workflows.  

---

## 🔹 Steps Followed

### 1. Workflows
- Updated `config.yaml`
  
- Updated `schema.yaml`
  
- Updated `params.yaml`
  
- Defined entities
  
- Updated the **configuration manager** in `src/config`
    
- Built **components** and **pipeline**
  
- Updated `main.py`
  
- Updated `app.py`  

---

### 2. AWS CI/CD Deployment with GitHub Actions

**a. IAM Setup**  

- Created IAM user with access to:
  
  - **EC2** → virtual machine
    
  - **ECR** → container registry  

**b. Policies**  

- `AmazonEC2ContainerRegistryFullAccess`
  
- `AmazonEC2FullAccess`  

**c. ECR Repository**  

- Example URI:  


**d. EC2 Setup & Docker Installation**  

sudo apt-get update -y

sudo apt-get upgrade

curl -fsSL https://get.docker.com -o get-docker.sh

sudo sh get-docker.sh

sudo usermod -aG docker ubuntu

newgrp docker

e. Configure EC2 as Self-Hosted Runner

Go to GitHub: Settings > Actions > Runners > New self-hosted runner

Choose OS and run commands.

f. Setup GitHub Secrets

AWS_ACCESS_KEY_ID=<your-key>

AWS_SECRET_ACCESS_KEY=<your-secret>

AWS_REGION=us-east-1

AWS_ECR_LOGIN_URI=566373416292.dkr.ecr.ap-south-1.amazonaws.com

ECR_REPOSITORY_NAME=simple-app

3. Azure Deployment

docker build -t mlproj.azurecr.io/mlproj:latest .

docker login mlproj.azurecr.io

docker push mlproj.azurecr.io/mlproj:latest

## ✅ Outcome

Achieved high accuracy in predicting wine quality

Provided real-time web app predictions

Enabled scalable CI/CD deployment pipelines on AWS and Azure

Delivered valuable insights for winemakers to refine their products

## 🖼️ Demo Screenshot
