# Microservices Enterprise Application Deployments

This repository contains the deployments configuration scripts for each of the microservices in the Microservices Enterprise Application
project: [Microservices Enterprise Application](https://github.com/colinbut/microservices-enterprise-application)

That microservices project microservices would each run in Kubernetes.

Kubernetes is a container orchestration framework/tool which provides management of containers.

To run this, one needs access to a Kubernetes cluster.

For locally, you can use Minikube. Assuming minikube is installed and also `kubectl` the kubernetes client tool..

#### Start Cluster
To start up the Kubernetes cluster.

```bash
minikube start
```

#### Deploy to Cluster

Apply deployment configuration scripts

```bash
kubectl apply -f [kubernetes-deployment-file]
```

for e.g. To deploy each of the microservices:

```bash
kubectl apply -f account-service/account-service-deployment.yml
kubectl apply -f audit-service/audit-service-deployment.yml
kubectl apply -f email-service/email-service-deployment.yml
kubectl apply -f exclusion-service/exclusion-service-deployment.yml
kubectl apply -f marketing-service/marketing-service-deployment.yml
kubectl apply -f notification-service/notification-service-deployment.yml
kubectl apply -f registration-email-service/registration-email-service-deployment.yml
kubectl apply -f registration-service/registration-service-deployment.yml
kubectl apply -f reporting-service/reporting-service-deployment.yml
kubectl apply -f subscription-service/subscription-service-deployment.yml
kubectl apply -f user-service/user-service-deployment.yml
```

#### Useful Kubectl Commands

```bash
kubectl get pods
```

```bash
kubectl get services
```

```bash
kubectl get deployments
```

```bash
kubectl get nodes
```

```bash
kubectl get replicaSets
```

```bash
kubectl logs [POD_NAME]
```

```bash
kubectl cluster-info
```

```bash
kubectl describe pod [POD_NAME]
```