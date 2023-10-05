helm repo add argo-cd https://argoproj.github.io/argo-helm
helm dep update charts/argocd/
helm install -f values.yaml --create-namespace -n argocd argocd .
helm upgrade --install argocd --values values.yaml --create-namespace -n argocd .
helm uninstall argocd --namespace argocd
kubectl delete namespace argocd


Install Helmcharts Declarative
- https://argo-cd.readthedocs.io/en/stable/user-guide/helm/
- https://github.com/argoproj/argo-cd/blob/master/docs/operator-manual/argocd-repositories.yaml