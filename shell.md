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


## Update package.json
Update repository field
```
REPO='myrepo'
VENDOR='myvendor'
TARGET_PACKAGE_JSON='package.json'

jq \
--arg type 'git' \
--arg url ${REPO} \
--arg directory ${VENDOR} \
'. + {"repository": {"type": $type, "url": $url, "directory": $directory}}' \
${TARGET_PACKAGE_JSON} \
| sponge ${TARGET_PACKAGE_JSON}
 ```
