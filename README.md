# [Backstage](https://backstage.io)

This is your newly scaffolded Backstage App, Good Luck!

To start the app, run:

```sh
yarn install
yarn start
```

# Custom Image
This is based on the Udemy Course [From DevOps to Platform Engineering: Master Backstage & IDPs](https://www.udemy.com/course/from-devops-to-platform-engineering-master-backstage-idps/?utm_campaign=email&utm_medium=email&utm_source=sendgrid.com)

## Creating an updated Docker Image
From the directory with app-config.yaml and Dockerfile run:

```bash
docker buildx create --use --name multiarch-builder || docker buildx use multiarch-builder

docker buildx build \
  --platform linux/amd64,linux/arm64 \
  -t jaysuzi5/backstage:v4 \
  --push .
```
Adjust the version accordingly

## Deploying to Kubernetes
See home-lab project specifically the infrastructure/backsage/README.md file for more information.