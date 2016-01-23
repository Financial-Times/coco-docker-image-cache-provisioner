#Docker image to provision a docker image registry

###

```
# Build the image
docker build -t coco/registry-provisioner .

# Set all the required variables
export TOKEN_URL=https://discovery.etcd.io/xxxxxx
export VAULT_PASS=xxxxxxxx
export SERVICES_DEFINITION_ROOT_URI=https://raw.githubusercontent.com/Financial-Times/coco-docker-image-cache-services/master/
export AWS_SECRET_ACCESS_KEY=xxxxxxx
export AWS_ACCESS_KEY_ID=xxxxxxxx

# Run the image
docker run --env "TOKEN_URL=$TOKEN_URL" --env "VAULT_PASS=$VAULT_PASS" --env "SERVICES_DEFINITION_ROOT_URI=$SERVICES_DEFINITION_ROOT_URI" --env "AWS_SECRET_ACCESS_KEY=$AWS_SECRET_ACCESS_KEY" --env "AWS_ACCESS_KEY_ID=$AWS_ACCESS_KEY_ID" coco/registry-provisioner
```

