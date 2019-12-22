# Kubernetes demo voting application

In this tutorial, we will demo a Voting application on Google Kubernetes Engine.

TODO
[x] 1. Setup a Google Container Engine Environtment
[x] 2. Create Kubernetes PODS
[x] 3. Create Services - ClusterIP - Internal
[x] 4. Create Services - LoadBalancer - External

## Basic knowledge

#### Pod

Pod is internal.

#### Service

Service is external.

To create a service from pod must use selector attribue with labels: name, app which is defined in pod.

**postgres-service.yml**

Kind: Service
Service name: db OR database

```shell
name: db # remember that the services should be named based on what the other application is looking for

```