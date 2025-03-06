# Deploy-NGINX-Using-Kubernetes

# Nginx Deployment Using Minikube and Kubernetes

This project demonstrates how to deploy a Nginx web server using Minikube, kubectl, and Helm on Kubernetes.

## Prerequisites

- **Minikube**: A local Kubernetes cluster.
- **kubectl**: Kubernetes CLI tool.
- **Helm**: Kubernetes package manager.
- **Docker**: To build images locally if necessary.
- **Git**: For version control.

## Setup Instructions

Follow these steps to deploy the Nginx web server on Minikube.

### 1. Start Minikube

If you haven't started Minikube yet, do so with the following command:

```bash
minikube start
2. Apply Kubernetes Configurations
Apply the necessary Kubernetes configuration files to set up the Nginx web server.

bash
Copy
Edit
kubectl apply -f configmap.yml
kubectl apply -f deployment.yml
kubectl apply -f ingress.yml
kubectl apply -f nginx-pod.yml
kubectl apply -f pv.yml
kubectl apply -f pvc.yml
kubectl apply -f service.yml
3. Check the Deployment
To verify that everything has been deployed correctly, run the following commands:

bash
Copy
Edit
kubectl get pods
kubectl get svc
kubectl get ingress
4. Access the Nginx Web Server
If you're using a NodePort or LoadBalancer service type, you can access the Nginx web server via the Minikube IP and port:

bash
Copy
Edit
minikube service nginx-service
5. Optional: Use Helm for Deployment
If you want to deploy using Helm, create a Helm chart for the Nginx deployment and install it using the following:

bash
Copy
Edit
helm install nginx-web-server ./nginx-chart
