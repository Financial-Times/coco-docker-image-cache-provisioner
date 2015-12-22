#Docker image to provision a docker image registry

###

```
# Build the image
docker build -t coco/registry-provisioner .

# Set all the required variables
TOKEN_URL=https://discovery.etcd.io/xxxxxx
VAULT_PASS=xxxxxxxx
SERVICE_DEFINITION_LOCATION=https://raw.githubusercontent.com/Financial-Times/coco-docker-image-cache-services/master/services.yaml
AWS_SECRET_ACCESS_KEY=xxxxxxx
AWS_ACCESS_KEY_ID=xxxxxxxx

# Run the image
docker run --env "TOKEN_URL=$TOKEN_URL" --env "VAULT_PASS=$VAULT_PASS" --env "SERVICE_DEFINITION_LOCATION=$SERVICE_DEFINITION_LOCATION" --env "AWS_SECRET_ACCESS_KEY=$AWS_SECRET_ACCESS_KEY" --env "AWS_ACCESS_KEY_ID=$AWS_ACCESS_KEY_ID" coco/registry-provisioner
```

