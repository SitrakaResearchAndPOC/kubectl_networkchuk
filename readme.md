
* Downloading kubectl 
```
curl -LO https://storage.googleapis.com/kubernetes-release/release/v1.21.5/bin/linux/amd64/kubectl
```
```
ls
```
```
chmod +x kubctl
```
```
cp ./kubectl /usr/local/bin/kubectl
```
```
export KUBECONFIG=file.yaml
```
```
kubectl get nodes
```
```
kubectl run networkchuckcoffee --image=thenetworkchuck/nccoffee:pourover --port=80 
```
```
kubectl get pods
```
```

kubectl describe pods


Deployement :  i want three pods
-3
-nccoffee
-port 80


yaml ---> manifest deployment


kubectl delete pods networkchuckcoffee

kubectl apply -f manifest.yaml

kubectl get pods

kubectl delete pods networkchuckcoffee


kubectl get deployements

get the name of deployment

edit manifest : 
kubectl edit deployment <name of deployement>

who to expose web site :
------------------------

service is exposed to the manifest service

kubectl get services

Go to nodebalancers on Linode

kubectl describe services coffee-service


