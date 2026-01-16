# MLflow Model Lifecycle – Churn Prediction (MLOps Lab)

## Overview
This lab demonstrates a complete MLflow-based MLOps workflow for managing the lifecycle of a churn prediction model.

---

## Step 1 – Environment Initialization and MLflow Installation
We initialized the Python environment and installed MLflow and the required dependencies.

![Step 1 Screenshot](img_lab7/1_1.png)

---

## Step 2 – Creation of the MLflow Storage Space
We explicitly created the directories used by MLflow to store experiments, artifacts, and models.

![Step 2 Screenshot](img_lab7/2_1.png)

---

## Step 3 – MLflow Client Configuration
We configured the MLflow tracking URI so that all runs are logged to the same tracking server.

![Step 3 Screenshot](img_lab7/3_1.png)

---

## Step 4 – Starting the MLflow Tracking Server
We started the MLflow tracking server and accessed the MLflow UI locally.

![Step 4 Screenshot 1](img_lab7/4_1.png)
![Step 4 Screenshot 2](img_lab7/4_2.png)
![Step 4 Screenshot 3](img_lab7/4_3.png)

---

## Step 5 – Instrumentation of `train.py`
We instrumented the training script to log parameters, metrics, and the trained model to MLflow.

![Step 5 Screenshot 1](img_lab7/5_1.png)
![Step 5 Screenshot 2](img_lab7/5_2.png)
![Step 5 Screenshot 3](img_lab7/5_3.png)

---

## Step 6 – Observation of the MLflow Model Registry
We observed the registered `churn_model` and its first version in the MLflow Model Registry.

![Step 6 Screenshot](img_lab7/6_1.png)

---

## Step 7 – Model Promotion
We promoted a selected model version to the production stage using the MLflow Model Registry.

![Step 7 Screenshot 1](img_lab7/7_1.png)
![Step 7 Screenshot 2](img_lab7/7_2.png)

---

## Step 8 – Model Rollback
We rolled back the production stage to a previous stable model version using the MLflow Model Registry.

![Step 8 Screenshot 1](img_lab7/8_1.png)
![Step 8 Screenshot 2](img_lab7/8_2.png)

---

## Step 9 – API Loading the Active Model
We configured the API to load the currently active production model directly from the MLflow Model Registry.

![Step 9 Screenshot 1](img_lab7/9_1.png)
![Step 9 Screenshot 2](img_lab7/9_2.png)
![Step 9 Screenshot 3](img_lab7/9_3.png)

---
