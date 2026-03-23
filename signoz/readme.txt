First create NS and deploy the signoz monitoring and logging tool in your kubernets cluster.
--------------------------------------------------------------------------------------------

kubectl create ns signoz
kubectl create ns platform
 
deploy platform services 
````````````````````````
cd platform
 
kubectl apply -f serviceaccounts -n platform
kubectl apply -f clusterroleandbinding -n platform
kubectl apply -f configmap -n platform
kubectl apply -f secret -n platform
kubectl apply -f service -n platform
kubectl apply -f dep -n platform
kubectl apply -f job -n platform
 
deploy signoz services
``````````````````````
apply the folder directly
 
kubectl apply -f signoz -n signoz