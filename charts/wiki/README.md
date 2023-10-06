# Wikijs
helm repo add requarks https://charts.js.wiki
helm repo update
helm deb update
helm upgrade --install wiki --values values.yaml --create-namespace -n wiki .
helm uninstall wiki --namespace wiki
kubectl delete namespace wiki

helm show values requarks/wiki > values.yaml
Src:
