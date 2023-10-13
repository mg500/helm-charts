# argocd
helm install --create-namespace -n training training .
helm get manifest training -n training
helm uninstall training -n training
helm install --debug --dry-run training .