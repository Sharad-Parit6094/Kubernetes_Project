# Application Deployment using Minikube

The project aims to deploy a web application along with a MongoDB database in a Kubernetes environment using Minikube. It involves setting up MongoDB, creating Kubernetes resources (such as ConfigMaps, Secrets, Deployments, and Services), configuring access, and enabling interaction with the deployed application.

## Project Steps

### 1.Configuration and Secrets Setup:
i. Creation of a ConfigMap (mongo-config.yaml) to store MongoDB configuration data, allowing easy modification and separation of configuration from Pod specifications.
ii. Generating a Secret (mongo-secret.yaml) to securely store sensitive information like usernames and passwords for MongoDB
### 2.Deployment of MongoDB:
i. Definition of a MongoDB Deployment and Service (mongo.yaml) in Kubernetes to ensure the availability and accessibility of the MongoDB instance
### 3.Deployment of Web Application:
i. Setup of a Deployment and Service (webapp.yaml) for the web application within Kubernetes.
### 4.Integration of Secrets and Configurations:
i. Integration of the mongo-secret with the MongoDB Deployment, enabling the secure passing of sensitive credentials to the MongoDB instance.
ii. Integration of the mongo-config ConfigMap in the WebApp Deployment, allowing the web application to access necessary configuration data.
### 5.External Access Configuration:
i. Configuring external access to the deployed WebApp Service, potentially using NodePort or LoadBalancer configurations to enable access from outside the Kubernetes cluster.
### 6.Minikube Deployment:
i. Execution of the deployment within Minikube by applying the Kubernetes resources to the local cluster using kubectl apply.

``minikube start
kubectl apply -f mongo-config.yaml
kubectl apply -f mongo-secret.yaml
kubectl apply -f mongo.yaml
kubectl apply -f webapp.yaml``

### 7.Accessing the Web Application:
i. Providing instructions on how to access the deployed web application in a browser by utilizing port-forwarding or the externally exposed endpoint.


![alt text](https://github.com/Sharad-Parit6094/Kubernetes_Project/blob/main/Kubernetes_Project_image.png).

