Genereate typescript client as an npm library
```
docker run --rm \
  -v ${PWD}:/local \
  openapitools/openapi-generator-cli generate \
  -i /local/swagger.json \
  -g typescript-node \
  -o /local/out/ \
  --additional-properties supportsES6=true,npmName=ts-harbor-client
```
