# One liners
## Change property in YAML file
```
cat $F_PATH| yq '.versions.tag.app = $v' --arg v 1.0.1 -y |sponge $F_PATH
```

Tip: to install `yq` and `sponge`
```
brew install python-yq
brew install moreutils
```