
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
```
* Deployement 
i want three pods </br>
-3 </br>
-nccoffee </br>
-port 80 </br>
yaml ---> manifest deployment
```
wget https://raw.githubusercontent.com/SitrakaResearchAndPOC/kubectl_networkchuk/main/networkchuckcoffee_deployment.yaml
```
```
kubectl delete pods networkchuckcoffee
```
```
kubectl apply -f networkchuckcoffee_deployment.yaml
```
```
kubectl get pods
```
```
kubectl delete pods networkchuckcoffee
```
```
kubectl get deployements
```
```
get the name of deployment
```
edit manifest : </br>
change replica </br>
```
kubectl edit deployment <name of deployement>
```
* Services
Expose web site </br>
service is exposed to the manifest service (yaml)
```
wget https://raw.githubusercontent.com/SitrakaResearchAndPOC/kubectl_networkchuk/main/networkchuckcoffee_service.yaml
```
```
kubectl apply -f networkchuckcoffee_service.yaml
```
```
kubectl get services
```
Go to nodebalancers on Linode and verify </br>
```
kubectl describe services coffee-service
```
