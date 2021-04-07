
#Definition

A pod is the basic execution unit of a K8s application the smallest and simplest unit in the K8s object model that you create or deploy 


Running a Pod

kubectl run my-nginx --image=nginx:alpine
kubectl get pods
kubectl get all

kubectl describe pod my-nginx
kubectl get pod my-nginx -o yaml


Expoose a pod port

kubectl port-forward [podname] [external host/cluster port]:[internal pod port]
kubectl port-forward podnginx [8080]:[80]


Delete a pod

kubectl delete pod [pod name]
kubectl delete pod podnginx


Creating or Apply Changes to a Pod Using YAML

#Performe a "trial" create and also validade the YAML
kubectl create -f ./files/nginx.pod.yaml --dry-run --validate=true

#Create a Pod from YAML
#Will error if Pod already exists
kubectl create -f ./files/nginx.pod.yaml --dry-run --validate=true

#Alternate way to create or apply changes to a Pod from YAML
kubectl apply -f ./files/nginx.pod.yaml 

#Use --save-config when you ant to use 
#Kubectl apply in the future
kubectl apply -f ./files/nginx.pod.yaml 

#Delete POD Using YAML file that created it
kubectl delete -f ./files/nginx.pod.yaml 

Access in the container inside Pod

kubectl exec my-nginx -it sh


Pod Health

