## What is namespace?
1. Namespace is a virtual sub-cluster
2. It is used to organize and separate our kubernetes objects. 
3. All Kubernetes ojects stay inside the namespace.
4. While creating the objects,we have to provide the namespace.
5. If we do not provide the namespace while creating objects, then default namespace will be used.

## How to list Namespace ?
   command: kubectl get namespaces 
   
## How to specify Namespace?
   We can provide namespace flag like this - 
   command: kubectl get pods -n our_name_spacename
   command: kubectl get pods --namespace our_name_spacename
   
   
 
  


