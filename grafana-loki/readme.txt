First create NS and deploy the grafana-loki monitoring and logging tool in your kubernets cluster.
--------------------------------------------------------------------------------------------------

kubectl create ns grafana-loki
 
kubectl apply -f dep -n grafana-loki

kubectl apply -f yamlshost -n grafana-loki
