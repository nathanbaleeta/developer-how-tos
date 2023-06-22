# Kubernetes commands for managing namespaces in an existing cluster

#### Create a new namespace named my-namespace
```
kubectl create namespace <my-namespace>
```

#### Display all resources running in specified namespace
```
kubectl get all -n <my-namespace>
```
