Project Description: System Monitoring Application Deployment
Objective:
The primary goal of this project was to develop and deploy a scalable system monitoring application using modern DevOps and cloud technologies. The application was designed to monitor various system metrics and provide insights into system performance and health.

Technologies Used:

Python & Flask: For developing the core application.
Docker: For containerizing the application.
Amazon ECR (Elastic Container Registry): For storing Docker images.
Amazon EKS (Elastic Kubernetes Service): For deploying and managing the application in a Kubernetes cluster.
Detailed Process:
Application Development:

Python & Flask: I started by developing a system monitoring application using Python and Flask. The application was designed to collect and display system metrics such as CPU usage, memory usage, and disk space.
Local Testing: The application was tested locally on port 5000 to ensure it functioned as expected.
Containerization:

Dockerfile Creation: I created a Dockerfile to define the environment and dependencies required to run the Flask application. This included installing Python, Flask, and any other necessary libraries.
Docker Image: Using the Dockerfile, I built a Docker image of the application. This image encapsulated the application code, runtime, libraries, and environment variables.
Docker Container: The Docker image was then used to create and run a Docker container locally, verifying that the containerized application worked as expected.
Pushing to Amazon ECR:

ECR Repository: I created an ECR repository in AWS to store the Docker image.
Image Push: The Docker image was pushed to the ECR repository, making it accessible for deployment in the AWS ecosystem.
Deployment Using Amazon EKS:

EKS Cluster Setup: An EKS cluster was created to orchestrate the deployment of the application. This included setting up the control plane and worker nodes.
Kubernetes Manifests: I wrote Kubernetes manifests (YAML files) to define the desired state of the application, including deployments and services. These manifests specified how many replicas of the application should run and how they should be exposed to the outside world.
Deployment: The application was deployed to the EKS cluster using the Kubernetes manifests. This involved creating Kubernetes deployments and services to manage the application containers.
Port Forwarding and Exposure: To make the application accessible, port forwarding was configured, and the service was exposed, allowing external access to the application.
Version Control:

GitHub Repository: All the project files, including the application code, Dockerfile, and Kubernetes manifests, were saved in a GitHub repository for version control and collaboration.
Benefits and Impact:
Scalability: The use of Kubernetes on EKS allowed the application to scale seamlessly based on demand.
Efficiency: Docker containerization ensured that the application could be easily deployed and managed across different environments.
Reliability: The deployment on AWS EKS provided a robust and reliable infrastructure, reducing the risk of downtime and ensuring high availability.
