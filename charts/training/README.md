# argocd
helm install --create-namespace -n training training .
helm get manifest training -n training