# Wine-Quality-Prediction-with-MLflow

- The project uses the UCI Wine Quality Dataset, which includes features like ‘fixed acidity’, 
‘pH’, and ‘residual sugar’ to train and predict the quality of wine.
- The project uses MLflow which is used for experiment tracking, model management, and 
deployment
- Deployment is done using AWS EC2 with an app runner.

## Workflows

1. Update config.yaml
2. Update schema.yaml
3. Update params.yaml
4. Update the entity
5. Update the configuration manager in src config
6. Update the components
7. Update the pipeline 
8. Update the main.py
9. Update the app.py
<<<<<<< HEAD


# How to run?
### STEPS:

Clone the repository

```bash
https://github.com/chaitanya-24/Wine-Quality-Prediction-with-MLflow
```
### STEP 01- Create a conda environment after opening the repository

```bash
conda create -n venv python=3.8 -y
```

```bash
conda activate venv
```


### STEP 02- install the requirements
```bash
pip install -r requirements.txt
```


```bash
# Finally run the following command
python app.py
```

Now,
```bash
open up you local host and port
```



## MLflow

[Documentation](https://mlflow.org/docs/latest/index.html)


##### cmd
- mlflow ui

### dagshub
[dagshub](https://dagshub.com/)

MLFLOW_TRACKING_URI=https://dagshub.com/chaitanya-24/Wine-Quality-Prediction-with-MLflow.mlflow \
MLFLOW_TRACKING_USERNAME=chaitanya-24 \
MLFLOW_TRACKING_PASSWORD=be00d7047851daf8623880cf2d283725cc59f763 \
python script.py

Run this to export as env variables:

```bash

export MLFLOW_TRACKING_URI=https://dagshub.com/chaitanya-24/Wine-Quality-Prediction-with-MLflow.mlflow

export MLFLOW_TRACKING_USERNAME=chaitanya-24

export MLFLOW_TRACKING_PASSWORD=be00d7047851daf8623880cf2d283725cc59f763

```


# AWS-CICD-Deployment-with-Github-Actions

## 1. Login to AWS console.

## 2. Create IAM user for deployment

	#with specific access

	1. EC2 access : It is virtual machine

	2. ECR: Elastic Container registry to save your docker image in aws


	#Description: About the deployment

	1. Build docker image of the source code

	2. Push your docker image to ECR

	3. Launch Your EC2 

	4. Pull Your image from ECR in EC2

	5. Lauch your docker image in EC2

	#Policy:

	1. AmazonEC2ContainerRegistryFullAccess

	2. AmazonEC2FullAccess

	
## 3. Create ECR repo to store/save docker image
    <!-- - Save the URI: 802898747809.dkr.ecr.ap-south-1.amazonaws.com/mlproj -->
    - Save the URI: 802898747809.dkr.ecr.us-east-1.amazonaws.com/mlproj

	
## 4. Create EC2 machine (Ubuntu) 
 
## 5. Open EC2 and Install docker in EC2 Machine:
	
	
	#optinal

		

	sudo apt-get upgrade -y

	sudo apt-get upgrade
	
	#required

	curl -fsSL https://get.docker.com -o get-docker.sh

	sudo sh get-docker.sh

	sudo usermod -aG docker ubuntu

	 
	
# 6. Configure EC2 as self-hosted runner:
    setting>actions>runner>new self hosted runner> choose os> then run command one by one


# 7. Setup github secrets:

    AWS_ACCESS_KEY_ID=

    AWS_SECRET_ACCESS_KEY=

    AWS_REGION = us-east-1

    AWS_ECR_LOGIN_URI = demo>>  566373416292.dkr.ecr.ap-south-1.amazonaws.com

    ECR_REPOSITORY_NAME = simple-app

## About MLflow 
MLflow

 - Its Production Grade
 - Trace all of your expriements
 - Logging & tagging your model


![w1](https://github.com/chaitanya-24/Wine-Quality-Prediction-with-MLflow/assets/62403348/525a232d-d539-4110-9f9f-90eb1d6de81a)
![w2](https://github.com/chaitanya-24/Wine-Quality-Prediction-with-MLflow/assets/62403348/f3de9dd0-38b3-49bd-a877-90bb0c5abe6d)
![w3](https://github.com/chaitanya-24/Wine-Quality-Prediction-with-MLflow/assets/62403348/4483db9f-c353-4a8d-b1c4-617083682b92)
