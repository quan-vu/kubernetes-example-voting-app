# Kubernetes demo voting application

In this tutorial, we will demo a Voting application on Google Kubernetes Engine.

TODO
[x] 1. Setup a Google Container Engine Environtment
[x] 2. Create Kubernetes PODS
[x] 3. Create Services - ClusterIP - Internal
[x] 4. Create Services - LoadBalancer - External
[x] 5. Deploy to Google Cloud Kubernetes example-voting-app cluster

## 5. Deploy to Google Cloud Kubernetes example-voting-app cluster

Todo

1. Clone https://github.com/quan-vu/kubernetes-example-voting-app.git
2. First, create the voting-app-pod to build voting app container in a pod.
3. Next, create the voting-app-service to be able to access this voting service from a browser.
4. Check the voting-app-service publish with External IP address.
5. Open the voting application on browser.

```shell
# 1. Clone https://github.com/quan-vu/kubernetes-example-voting-app.git
git clone https://github.com/quan-vu/kubernetes-example-voting-app.git
cd kubernetes-example-voting-app

# 2. First, create the voting-app-pod to build voting app container in a pod.
kubectl create -f voting-app-pod.yml

# 3. Next, create the voting-app-service to be able to access this voting service from a browser.
kubectl create -f voting-app-service.yml

# 4. Check the voting-app-service publish with External IP address.
kubectl get services

# NAME             TYPE           CLUSTER-IP    EXTERNAL-IP    PORT(S)        AGE
# kubernetes       ClusterIP      10.83.0.1     <none>         443/TCP        77m
# voting-service   LoadBalancer   10.83.1.211   34.66.203.83   80:32329/TCP   2m8s

```

Final, open external ip on your browser: http://34.66.203.83.

We will se the first piece of my or the first component of our application is up and running and the load balancer has been configured successfully.

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