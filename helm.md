Add chart repo 
```
helm repo add harbor https://helm.goharbor.io
```
Pull chart with a specific version
```
helm pull harbor/harbor --version "1.5.0"| tar -vxzf harbor-1.5.0.tgz
```
