# Monitoreando pods y clusters con prometheus y framana.

```
#Metrics server
helm repo add bitnami https://charts.bitnami.com/bitnami
helm install metrics-server -n kube-system bitnami/metrics-server

# Prometheus
kubectl create ns monitoring
helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
helm repo update
helm install -n monitoring prometheus prometheus-community/prometheus

# grafana
helm repo add grafana https://grafana.github.io/helm-charts
helm repo update
helm install -n monitoring grafana grafana/grafana

importar dashboard 10000 y 15661
https://grafana.com/grafana/dashboards/15661
```


![image](https://github.com/CliberCastillo/prometheus-grafana-kubernetes/assets/48666090/c289fe16-1d00-4acf-8aa9-5a5053757963)
