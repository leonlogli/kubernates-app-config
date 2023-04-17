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

Expose declaratively the deployment as a Kubernetes service:

```bash
kubectl apply -f="service.yaml"
```

Get the external IP address of the service:

```bash
kubectl get services

# the kubernates-app-config service will have pending external ip because we use minikube in local
# to get an external ip for the kubernates-app-config service and open the generated url in the browser
minikube service kubernates-app-config
```

Delete services and deployment

```bash
kubectl delete -f="service.yaml,deployment.yaml"
```

Merge services and deployment into one file

```bash
kubectl apply -f="kubernates.yaml"
```
