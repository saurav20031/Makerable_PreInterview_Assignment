#Makerable_PreInterview_Assignment

## Ruby on Rails CI/CD Pipeline with Docker, Kubernetes, ArgoCD, and Tekton

This project demonstrates a complete CI/CD pipeline for a Ruby on Rails application using Docker, Kubernetes, ArgoCD, and Tekton. The pipeline includes building a Docker image, deploying to Kubernetes, managing deployments with ArgoCD, and setting up Tekton pipelines for automation.

## Table of Contents

- [Project Overview](#project-overview)
- [Prerequisites](#prerequisites)
- [Steps Completed](#steps-completed)


## Project Overview

This project demonstrates the following steps in a CI/CD pipeline:

1. **Step 1: Docker**
   - Built a Dockerfile for deploying a simple Ruby on Rails application with PostgreSQL DB enabled. Application and DB run on different containers.

2. **Step 2: Kubernetes**
   - Built a YAML file to deploy the Ruby on Rails application and PostgreSQL DB on Kubernetes.
   - Used a Kubernetes StatefulSet for the standalone PostgreSQL pod.
   - Used an Ingress Controller for routing external traffic to the application.

3. **Step 3: ArgoCD**
   - Deployed ArgoCD to manage the deployment of the application using GitOps.
   - Created a private GitHub repository to manage the YAML files for GitOps.
   - Configured ArgoCD with application.yaml, ArgoCD config maps, and Kubernetes manifest files.

4. **Step 4: Tekton**
   - Set up Tekton pipelines and the Tekton dashboard.
   - Created a Task to download source code, build Docker images, and push them to Docker Hub.
   - Created a TaskRun to trigger the Task with specified parameters.

## Prerequisites

Before running this project, ensure you have the following installed:

- Docker
- Kubernetes 
- ArgoCD
- Tekton Pipelines

## Steps Completed

- Step 1: Build a Dockerfile for deploying a simple Ruby on Rails application with PostgreSQL DB  enabled. Application and DB should run on different containers.

- Step 2: Build a YAML file for the same application you’ve used in your first step to deploy it on Kubernetes. You can use any local cluster provider such as Minikube or K3d. The deployment of the standalone PostgreSQL pod must use Kubernetes StatefulSet. Additionally, the candidate may use any ingress controller they are comfortable with or a service mesh.

- Step 3: Deploy ArgoCD to manage the deployment of the previously mentioned application using GitOps. The candidate must create a private GitHub repository to manage the YAML files and for GitOps purposes. All ArgoCD config files must be present in the GitHub repository. The expected files include application.yaml to define the application to deploy, ArgoCD config maps (argocd-cm and argocd-rbac-cm), a config file for/(to add) the private GitHub repository and kubernetes manifest files.

- Step 4: Set up Tekton pipelines and the Tekton dashboard. The pipeline should download the source code from the public fork of the sample project (Which you’ve containerized in the first step), build the image, and push it to Docker Hub. The candidate is expected to manually run the pipeline from the Tekton dashboard.



