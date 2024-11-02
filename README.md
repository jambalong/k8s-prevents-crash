# Kubernetes Prevents Crash

This repository contains a simple Flask web application that serves as a dummy website. It is designed to demonstrate how to deploy a Flask application using Kubernetes, ensuring high availability and preventing crashes.

## Prerequisites

Before you begin, ensure you have the following installed:

- [Minikube](https://minikube.sigs.k8s.io/docs/start/)
- [kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/)
- [Docker](https://www.docker.com/get-started)

## Getting Started

1. **Clone the repository**:

```bash
git clone https://github.com/yourusername/dummy-flask-website.git
cd dummy-flask-website
```

2. **Build the Docker image:**

Make sure to build the Docker image for your Flask application:

```bash
docker build -t username/dummy-flask-website:latest .
```

3. **Start Minikube:**

Start Minikube if it is not already running:

```bash
minikube start
```

## Deployment

1. **Deploy the Flask application:**

Create a deployment for your flask application in a YAML file (deployment.yaml)

Apply the deployment:

```bash
kubectl apply -f deployment.yaml
```

2. **Create a service:**

Create a service to expose your Flask application in a YAML file (service.yaml)

Apply the service:

```bash
kubectl apply -f service.yaml
```

## Accessing the Application

After deploying the application, access it using the following URL:

```bash
http://127.0.0.1:30007
```

If using a different NodePort or Minikube IP, adjust the URL accordingly.

## Managing Deployments and Services

To check the status of your deployments and services, use:

```bash
kubectl get deployments
kubectl get services
```
