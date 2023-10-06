# Whoami
helm repo add cowboysysop https://cowboysysop.github.io/charts/
helm repo update
helm install -f values.yaml --create-namespace -n whoami whoami .
helm upgrade --install whoami --values values.yaml --create-namespace -n whoami .
helm uninstall whoami --namespace whoami
kubectl delete namespace whoami

helm show values cowboysysop/whoami > values.yaml
Src:
