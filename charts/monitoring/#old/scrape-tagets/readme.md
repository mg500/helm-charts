1. Edit 'prometheus-additional.yaml'
2. Update secret 'kubectl create secret generic additional-scrape-configs --from-file=prometheus-additional.yaml --dry-run=client -oyaml > additional-scrape-configs.yaml'