# Deploying Application on Kubernetes by using config file

This guide explains how to deploy the sample application on a Kubernetes cluster using yaml file.

## Prerequisites

Before you get started, you need to have the following tools installed:

- Docker
- minikube or a Kubernetes cluster
- kubectl

## Building the app image

Navigate to the root directory of the cloned repository:

Build the Docker image and push it to a registry:

```bash
kubectl apply -f="deployment.yaml"
```

To Get a Kubernetes deployments and check the status, run:

```bash
kubectl get deployments
```
