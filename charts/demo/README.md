helm upgrade --install demo --values values.yaml --create-namespace -n demo .
kubectl apply -f demo.yaml