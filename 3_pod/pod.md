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

   apiVersion: v1
   kind: Pod
   metadata:
     name: <pod-name>
     labels:
       app: <app-name>
   spec:
     containers:
     - name: <container-name>
       image: <image-name>
       ports:
       - containerPort: 80

