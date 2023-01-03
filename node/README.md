# Example Node.js hello world containerized application

This repository contains the official Node.js "hello world" containerized application files, as [described in this link on their website](https://nodejs.org/de/docs/guides/nodejs-docker-webapp/).

It is a useful example to look for vulnerabilities using [Sysdig Secure image scanning](https://www.sysdig.com).

To make the image secure, change the reference base image from `node:12` to `bitnami/node`.

From [repo](https://github.com/johnfitzpatrick/hello-world-node-vulnerable).


How to build the image and push to a registry:

```
cd node
export REGISTRY
export IMAGE=$AWS_ACCOUNT.dkr.ecr.$REGION.amazonaws.com/$ECR_NAME
docker build . -t $IMAGE
docker push $IMAGE 
```