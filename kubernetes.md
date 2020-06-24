Tail logs from cluster, exclude certain strings
```
stern --all-namespaces -l app=harbor --tail=1 --exclude=kube-probe --exclude=/api/health
```
