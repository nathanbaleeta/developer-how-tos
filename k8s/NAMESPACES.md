# Organizing your components with Namespaces

#### Get all namespaces available in cluster
```
kubectl get namespace
```

#### Create a new namespace named my-namespace
```
kubectl create namespace <my-namespace>
kubectl create namespace cloud-erp
```

#### Display all resources running in specified namespace
```
kubectl get all -n <my-namespace>
kubectl get all -n cloud-erp
```

#### Get details about specified namespace
```
kubectl describe namespace <my-namespace>
kubectl describe namespace cloud-erp
```
