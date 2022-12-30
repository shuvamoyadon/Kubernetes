## Create Ngnix POD using this below yaml file 
   1. kubectl apply -f pod.yaml  ## We must have pod label if we want to expose the pod
   2. create a service for the above pod by running the command: kubectl expose pod webserver --name=mysvc --port=80 --type=NodePort
   3. check the NodePort number : kubectl describe svc mysvc
   4. Now Allow the port range used for NodePort by creating the firewall rule : gcloud compute firewall-rules create myrule --allow tcp:30000-32767
   5. Now Check the external IP of any one of the nodes in the Kubernetes Cluster: kubectl get nodes -o wide
   6. Paste the external ip along with nodeport number in web browser to see the response from the pod : http://10.12.1.100:30767
