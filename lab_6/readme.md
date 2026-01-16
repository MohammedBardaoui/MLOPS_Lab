# Kubernetes Deployment of Churn API – MLOps Lab

## Overview
This lab demonstrates how to deploy a churn prediction API on Kubernetes using Docker, ConfigMaps, Secrets, probes, persistent volumes, and network policies.

---

## Step 1 – Prepare the Kubernetes Environment
We prepared the local Kubernetes environment (Minikube) and verified cluster access.


![Step 1 Screenshot](img_lab6/1_2.png)


---

## Step 2 – Prepare the Docker Image for the Churn API
We ensured the API source code and Dockerfile were ready for containerization.

![Step 2 Screenshot](img_lab6/2_1.png)

---

## Step 3 – Create the Kubernetes Manifests Directory
We created the `k8s/` directory to store all Kubernetes manifest files.

![Step 3 Screenshot](img_lab6/3_1.png)

---

## Step 4 – Build the Docker Image (Versioned Tag)
We built the Docker image for the API with a versioned tag.

![Step 4 Screenshot](img_lab6/4_1.png)

---

## Step 5 – Load the Docker Image into Minikube
We explicitly loaded the Docker image into Minikube so it can be used by Kubernetes.

![Step 5 Screenshot](img_lab6/5_1.png)

---

## Step 6 – Kubernetes Deployment for the Churn API
We created and applied the Deployment manifest to run the API in Kubernetes.

![Step 6 Screenshot](img_lab6/6_1.png)

---

## Step 7 – Expose the API via a NodePort Service
We exposed the API externally using a Kubernetes NodePort Service.

![Step 7 Screenshot 1](img_lab6/7_1.png)
![Step 7 Screenshot 2](img_lab6/7_2.png)
![Step 7 Screenshot 3](img_lab6/7_3.png)

---

## Step 8 – Inject Configuration via ConfigMap
We injected configuration values into the API using a Kubernetes ConfigMap.

![Step 8 Screenshot 1](img_lab6/8_1.png)
![Step 8 Screenshot 2](img_lab6/8_2.png)

---

## Step 9 – Manage Secrets (MONITORING_TOKEN)
We securely injected sensitive data using a Kubernetes Secret.

![Step 9 Screenshot 1](img_lab6/9_1.png)
![Step 9 Screenshot 2](img_lab6/9_2.png)
![Step 9 Screenshot 3](img_lab6/9_3.png)

---

## Step 10 – Health Endpoints for the API
We implemented health endpoints (`/health`, `/ready`, `/startup`) in the API.

![Step 10 Screenshot 1](img_lab6/10_1.png)
![Step 10 Screenshot 2](img_lab6/10_2.png)

---

## Step 11 – Add Kubernetes Probes
We configured liveness, readiness, and startup probes in the Deployment.

![Step 11 Screenshot 1](img_lab6/11_1.png)
![Step 11 Screenshot 2](img_lab6/11_2.png)

---

## Step 12 – Persistent Volume for Registry and Logs
We mounted a PersistentVolumeClaim to store models, registry data, and logs.

![Step 12 Screenshot 1](img_lab6/12_1.png)
![Step 12 Screenshot 2](img_lab6/12_2.png)
![Step 12 Screenshot 3](img_lab6/12_3.png)

---

## Step 13 – NetworkPolicy
We applied a NetworkPolicy to control network access to the API pods.

![Step 13 Screenshot](img_lab6/13_1.png)

---

## Step 14 – Final Verification
We verified pods, services, logs, API availability, and overall system health.

![Step 14 Screenshot 1](img_lab6/14_1.png)
![Step 14 Screenshot 2](img_lab6/14_2.png)
![Step 14 Screenshot 3](img_lab6/14_3.png)
![Step 14 Screenshot 4](img_lab6/14_4.png)

---
