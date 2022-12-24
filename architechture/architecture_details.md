# What is Kubernetes?
Kubernetes is an orchestration engine for container technologies such as Docker.It is already available on many clouds like Azure and Google Cloud as a managed service.

# Use Of Kubernetes
  1. Deployment services
  2. automated deployments,
  3. updates by managing services with almost zero downtime.
  
# Architecture 

![alt text](https://user-images.githubusercontent.com/42385240/209423021-75e8a91c-3c44-4866-9bd1-7aa85588c583.jpeg)

# Architectural Component of Kubernetes

Control Plane Components : 
   A. Control Manager(c-m): 
       1. Run multiple controllers utility.
       2. All controllers execute automation related task within a cluster.
   
   B. Cloud Control Manager(c-c-m): 
       1. It provides interface between Kubernetes and various Cloud Platform
       2. It is used when cloud based resources are in use with Kubernetes.
