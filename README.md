# Wine-Quality-Prediction-with-MLflow

### The project is currently in development phase. 

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
