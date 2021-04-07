Kube Web UI 
    kubectl apply -f https://raw.githubusercontent.com/kubernetes/dashboard/v2.0.0/aio/deploy/recommended.yaml
    k describe secret -n kube-system
    kubectl proxy
    http://localhost:8001/api/v1/namespaces/kubernetes-dashboard/services/https:kubernetes-dashboard:/proxy/



kubectl

kubectl version 

kubectl cluster-info

kubectl get all

kubectl run [container-name] --image=[image-name]

kubectl port-forwad [pod] [port]

kubectl expose ...

kubectl create [resource]

kubectl apply [resource]


Aliasing kubeclt

#powershell
Set-Alias -Name k -Value kubectl
#mac/linux
alias k="kubectl"

