## What is POD?
   1. It is the smallest and basic building block of Kubernetes service.
   2. Pod consists of one or more containers.
   3. Pod has resources and unique IP address.
   4. containers in a pod can communicate with each other using localhost 
   5. It does not need network address translation (NAT) or expose their ports to the outside world.
   6. Pods are ephemeral, which means that they are not meant to be long-lived. 
   7. When a pod is deleted, all of its containers are terminated and their state is lost.
   8. Pods are usually managed by higher-level resources such as Deployments, which ensure that a specified number of replicas of a pod are running at any given time.

## YAML to create POD
      In the YAML file for pod resource , these are the main required key to use. 
      apiVersion
      kind
      metadata
      spec
      
      TEMPLATE yaml file:
      
      apiVersion: v1.                   #The apiVersion and kind fields specify that this is a pod resource that it uses.
      kind: Pod
      metadata:                         # The metadata field contains information about the pod, such as its name and labels.
        name: <pod-name>
        labels:
          app: <app-name>
      spec:                             #The spec field specifies the details of the pod, including the containers details
        containers:
        - name: <container-name>
          image: <image-name>
          ports:
          - containerPort: 80
          
     The pod has a single container with the specified name and image. It exposes port 80 of the container to the outside world. You can add more containers to the pod by adding additional elements to the containers list. 
     
## How to apply the pod in kubernetes
  
    Use the kubectl apply command to create the pod:

    kubectl apply -f <pod-config-file.yaml>

## How to see the pod whether its created or not in the cluster
    
    Command: we can add namespace at the end if we have any namespace
    kubectl get pods
    
    
## How to delete pod from the cluster 
   
   kubectl delete pod <pod-name>



