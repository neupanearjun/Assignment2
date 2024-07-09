Deploying a Python Application on Kubernetes

Overview

In this project, I gained hands-on experience with containerization and orchestration using Docker and Kubernetes. The goal was to deploy a Python web application that displays the current time in Toronto, Canada, utilizing Kubernetes. The application was containerized using Docker, and I exposed it using NodePort on port 3030.

Objectives

Create a Dockerfile for the Python application.
Build and push a Docker image to a Docker repository.
Deploy the application on Kubernetes using a Deployment and expose it using a Service of type NodePort.
Document the process and push all necessary files to my GitHub repository.

Steps Completed

1. Fork and Clone the Repository

I forked the repository containing the Python application from source.
Next, I cloned my forked repository locally to begin working on it.

2. Create a Dockerfile
I wrote a Dockerfile to containerize the Python application, ensuring all dependencies were installed and that the application started correctly.

3. Build and Push Docker Image
I built the Docker image using the Dockerfile.
After successful build and testing, I tagged my Docker image and pushed it to a public Docker repository.

docker build -t arjunneupane/toronto-time-app:v01 .
docker push arjunneupane/toronto-time-app:v01

4. Write Kubernetes Manifests
I created a Kubernetes Deployment YAML file (deployment.yaml) to specify how Kubernetes should deploy my Docker image.
Additionally, I defined a Kubernetes Service YAML file (service.yaml) using NodePort to expose my application on port 3030.

5. Deploy to Kubernetes
I applied my Kubernetes manifests (deployment.yaml and service.yaml) to deploy my application.

I ensured that my Kubernetes cluster was accessible and verified that the application was running correctly.

6. Test the Application
I accessed the application via the NodePort (http://localhost:30300/) to ensure it displayed the correct current time in Toronto/Canada.

Challenges Faced
- Creating YAML files.
