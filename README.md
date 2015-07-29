#Docker image to provision a docker image registry

###

```
# Build the image
docker build -t coco/coreos-registry-setup .

# Set all the required variables
TOKEN_URL=https://discovery.etcd.io/xxxxxx
VAULT_PASS=xxxxxxxx
DEPLOYER_SERVICE_FILE_LOCATION=https://raw.githubusercontent.com/Financial-Times/coco-docker-image-cache-services/master/service-files/deployer.service
AWS_SECRET_ACCESS_KEY=xxxxxxx
AWS_ACCESS_KEY_ID=xxxxxxxx

# Run the image
docker run --env "TOKEN_URL=$TOKEN_URL" --env "VAULT_PASS=$VAULT_PASS" --env "DEPLOYER_SERVICE_FILE_LOCATION=$DEPLOYER_SERVICE_FILE_LOCATION" --env "AWS_SECRET_ACCESS_KEY=$AWS_SECRET_ACCESS_KEY" --env "AWS_ACCESS_KEY_ID=$AWS_ACCESS_KEY_ID" coco/coreos-registry-setup
```

