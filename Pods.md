
#Definition

A pod is the basic execution unit of a K8s application the smallest and simplest unit in the K8s object model that you create or deploy 


Running a Pod

kubectl run podnginx --image=nginx:alpine
kubectl get pods
kubectl get all


Expoose a pod port

kubectl port-forward [podname] [external host/cluster port]:[internal pod port]
kubectl port-forward podnginx [8080]:[80]


Delete a pod

kubectl delete pod [pod name]
kubectl delete pod podnginx

kubectl delete deployment [podname]






