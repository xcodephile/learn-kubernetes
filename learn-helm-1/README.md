# angular-nodejs-minikube
This is an example project Angular with NodeJS backend running on Minikube

## Source
https://medium.com/bb-tutorials-and-thoughts/how-to-get-started-with-helm-b3babb30611f

## Run

```
docker build -t frontend-example-1 .
docker tag frontend-example-1 xcodephile/frontend-example-1
docker login
docker push xcodephile/frontend-example-1:latest
# https://hub.docker.com/repository/docker/xcodephile/frontend-example-1
```

```
helm create frontend-example-1
# dir ./frontend-example-1 created
helm package frontend-example-1
helm install frontend-example-1-v1 frontend-example-1-0.1.0.tgz
http://localhost:32755/
helm uninstall frontend-example-1-v1
```
