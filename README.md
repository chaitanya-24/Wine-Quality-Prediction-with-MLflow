# WineQuality.ai: ML-Powered Quality Assurance System

## Project Overview

The project aims to predict the quality of wine based on several physicochemical properties, such as acidity, pH, and sugar content, using a machine learning model. It uses the UCI Wine Quality Dataset and follows an end-to-end machine learning pipeline. The pipeline involves data ingestion, validation, transformation, model training, evaluation, and deployment using GitHub Actions and Flask.

**MLflow** is employed to track experiments and handle the model registry, while the deployment process is automated using **GitHub Actions** with a **Flask** API interface for prediction.

### Key Features
- **End-to-End ML Pipeline**: From data ingestion to model deployment.
- **MLflow Integration**: Experiment tracking, logging metrics, and registering models.
- **CI/CD Pipeline**: Using GitHub Actions for continuous integration and deployment.
- **API Interface**: Built using Flask for real-time predictions.
- **Dockerized Deployment**: Deploy models via Docker on AWS EC2 instances.

---

## Project Components

1. **Data Ingestion**
   - Fetching the dataset from the UCI Wine Quality repository
   - Features include:
     - Fixed Acidity
     - Volatile Acidity
     - Citric Acid
     - Residual Sugar
     - Chlorides
     - Free Sulfur Dioxide
     - Total Sulfur Dioxide
     - Density
     - pH
     - Sulphates
     - Alcohol

2. **Data Validation**
   - Checking for missing/null values
   - Validating data types and feature ranges

3. **Data Transformation**
   - Scaling features
   - Splitting the dataset into training and testing sets
   - Label creation for wine quality

4. **Model Training**
   - Train the model using ElasticNet Regression
   - Track experiments with MLflow, logging metrics like accuracy, precision, and F1-score

5. **Model Evaluation**
   - Evaluation metrics such as:
     - MAE
     - MSE
     - R2 Score

6. **Train Pipeline**
   - Orchestrates the entire process:
     - Triggers data ingestion, validation, transformation
     - Logs metrics and registers models in the MLflow registry

7. **Prediction Pipeline**
   - Accepts new inputs (wine features)
   - Provides real-time predictions

8. **Deployment**
   - The selected model is dockerized and deployed on an AWS EC2 instance
   - The deployment process is automated using GitHub Actions
   - The Flask API interface is built to accept requests and return predictions

9. **CI/CD Pipeline**
   - GitHub Actions handles:
     - Continuous integration: running tests on commits
     - Continuous deployment: builds Docker image and deploys it on AWS EC2

---

## Workflows
- Update `config.yaml`
- Update `schema.yaml`
- Update `params.yaml`
- Update the entity
- Update the configuration manager in the src config
- Update the components
- Update the pipeline
- Update `main.py`
- Update `app.py`


## How to Run?
### STEPS:
1. Clone the repository:
   ```bash
   git clone https://github.com/chaitanya-24/Wine-Quality-Prediction-with-MLflow
   ```

2. Create a conda environment:
   ```lua
   conda create -n venv python=3.8 -y
   conda activate venv
   ```

3. Install the requirements:
   ```
   pip install -r requirements.txt
   ```

4. Run the training pipeline:
   ```
   python main.py
   ```
5. Run the Project:
   ```
   python app.py
   ```

### MLflow
You can start MLflow locally with:
```
mlflow ui
```

For DAGsHub integration:
1. Run this to set environment variables:
   ```arduino
   export MLFLOW_TRACKING_URI=[Link]
   export MLFLOW_TRACKING_USERNAME=[Username]
   export MLFLOW_TRACKING_PASSWORD=[Password]
   ```

## AWS CI/CD Deployment with GitHub Actions
### Steps:
1. Login to AWS console and create an IAM user for deployment with access to:
   - EC2 for virtual machines
   - ECR (Elastic Container Registry) to store Docker images

2. Create ECR Repository to store Docker images

3. Create EC2 Machine (Ubuntu):
   - Install Docker on EC2:
     ```vbnet
     sudo apt-get upgrade -y
     sudo apt-get upgrade
     curl -fsSL https://get.docker.com -o get-docker.sh
     sudo sh get-docker.sh
     sudo usermod -aG docker ubuntu
     newgrp docker
     ```

4. Configure EC2 as Self-Hosted Runner:
   - Navigate to: GitHub > Actions > New self-hosted runner
   - Choose OS and run the given commands

5. Set up GitHub Secrets for AWS:
   ```makefile
   AWS_ACCESS_KEY_ID=[Your_Access_Key]
   AWS_SECRET_ACCESS_KEY=[Your_Secret_Key]
   AWS_REGION=us-east-1
   AWS_ECR_LOGIN_URI=[ECR_Login_URI]
   ECR_REPOSITORY_NAME=simple-app
   ```

6. GitHub Actions Deployment:
   - Build Docker image of the source code
   - Push the image to ECR
   - Launch EC2
   - Pull the image from ECR to EC2
   - Run Docker image on EC2

## Getting Started
### Prerequisites
1. Clone the repository:
   ```bash
   git clone https://github.com/chaitanya-24/wine-quality-prediction.git
   ```

2. Install the required dependencies:
   ```
   pip install -r requirements.txt
   ```

3. Set up AWS EC2 instance and GitHub Actions for deployment

## Tools and Technologies
- MLflow: For tracking experiments and managing model lifecycle
- Flask: For building APIs to serve the model
- GitHub Actions: For continuous integration and deployment
- Docker: For containerizing the model for deployment
- AWS EC2: For deployment of the model
- UCI Wine Quality Dataset: Used for model training

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## About MLflow
- Production Grade: MLflow is a scalable tool that ensures reproducibility in model training
- Experiment Tracking: Easily track all experiments, metrics, parameters, and outcomes
- Model Registry: Manage multiple versions of models

## Author
### Chaitanya Sawant:
* **[Gmail](mailto:chaitanya.aiwork@gmail.com)**
* **[Twitter](https://twitter.com/chaitanya_42)**
#

![w1](https://github.com/chaitanya-24/Wine-Quality-Prediction-with-MLflow/assets/62403348/525a232d-d539-4110-9f9f-90eb1d6de81a)
![w2](https://github.com/chaitanya-24/Wine-Quality-Prediction-with-MLflow/assets/62403348/f3de9dd0-38b3-49bd-a877-90bb0c5abe6d)
![w3](https://github.com/chaitanya-24/Wine-Quality-Prediction-with-MLflow/assets/62403348/4483db9f-c353-4a8d-b1c4-617083682b92)
