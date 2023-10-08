# argocd
helm repo add argo-cd https://argoproj.github.io/argo-helm
helm dep update ./argocd
helm install -f values.yaml --create-namespace -n argocd argocd ./argocd
helm upgrade --install argocd --values values.yaml --create-namespace -n argocd .
helm uninstall argocd --namespace argocd
kubectl delete namespace argocd

helm upgrade --install argocd ./argocd/ -n argocd





Install Helmcharts Declarative
- https://argo-cd.readthedocs.io/en/stable/user-guide/helm/
- https://github.com/argoproj/argo-cd/blob/master/docs/operator-manual/argocd-repositories.yaml
- https://argo-cd.readthedocs.io/en/stable/operator-manual/declarative-setup/
- https://suedbroecker.net/2022/08/16/how-to-use-a-declarative-setup-for-argo-cd-to-deploy-an-application-using-a-helm-repository/

Err
- https://github.com/prometheus-community/helm-charts/issues/3345#issuecomment-1574929706