# bank-infrastructure
Bank - Infrastructure and deployment

This repository contains the deployment configuration.

# Requirements
This is set up using minikube.
Note about installing: latest helm (v2.14.3) is not compatible with Kubernetes 1.16.0.

As workaround, start minikube with an older version.

`minikube start --kubernetes-version=1.15.4`

https://github.com/helm/helm/issues/6374

# Use
Minikube has no access to the local docker image registry.

To build the images within minikube use the following:

`eval $(minikube docker-env)`

`docker build -t fake-bank-backend:latest .`

`eval $(minikube docker-env -u)`
