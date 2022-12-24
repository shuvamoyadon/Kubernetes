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
       3. Responsible for noticing and responding when nodes go down.
       4. MAnaging Job Controller.
   
   B. Cloud Control Manager(c-c-m): 
       1. It provides interface between Kubernetes and various Cloud Platform
       2. It is used when cloud based resources are in use with Kubernetes.
   
   C. ETCD : 
       1. Consistent and highly-available key value data store
       2. Provides High Availibility storage for data
       
   D. Scheduler:
       1. Looks for unassigned node.
       2. it handles scheduling for avialble nodes in the cluster to run container.
       
   E. Node Components:
       Node components run on every node, maintaining running pods and providing the Kubernetes runtime environment. It has the follwing components below
         1. kubelet : An agent that runs on each node in the cluster. It communicates with control plane and make sure that containers are running on node.
         2. kube-proxy : It maintains network rules on nodes. These rules allow network communication to our Pods from network sessions.
         3. Container-Runtime: The container runtime is the software that is responsible for running containers.Some popular Container runtime is Docker.



       
