# Monitoring
helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
helm repo update
helm dep update
helm upgrade --install monitoring --values values.yaml --create-namespace -n monitoring .
helm uninstall monitoring --namespace monitoring
kubectl delete namespace monitoring


Src:
- https://github.com/prometheus-community/helm-charts/tree/main/charts/kube-prometheus-stack