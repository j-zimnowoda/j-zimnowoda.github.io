# Logging
Tail logs from cluster, exclude certain strings
```
stern --all-namespaces -l app=harbor --tail=1 --exclude=kube-probe --exclude=/api/health
```

# Ingress
## To inspect all ingress hosts and paths
ka get ing -o json | jq -r '.items[]| .metadata.name, .spec.rules[]'
