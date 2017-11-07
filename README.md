# YAO Bank
(Yet Another Online Bank)

Demo Application for Kubernetes suitable for showing authorization policy.

Consists of 3 microservices:

1. **database** - a single-cluster etcd database.  Stores the state for the demo.
1. **summary** - HTTP service that returns JSON account summaries.
1. **customer** - Front-end web service that displays account summaries to users.

![service graph](./docs/service-graph.svg)

## How to run

Set up the deployments, service accounts, and services.

```
kubectl apply -f 10-yaobank.yaml
```

*If using Istio*, then run the following to set up the Istio Ingress to the application.

```
kubectl apply -f 20-ingress.yaml
```
