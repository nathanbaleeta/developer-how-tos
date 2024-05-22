# Organizing your components with K8s Namespaces

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

#### Delete namespace
```
kubectl delete ns <my-namespace>
```

#### Force delete namespace (Single line command)
```
kubectl delete ns <my-namespace>

kubectl patch ns <my-namespace> -p '{"metadata":{"finalizers":null}}'
```

OR
```
kubectl delete ns <my-namespace>
```
In one terminal:
```
kubectl proxy
```

In another terminal:
```
kubectl get ns delete-me -o json | \
  jq '.spec.finalizers=[]' | \
  curl -X PUT http://localhost:8001/api/v1/namespaces/delete-me/finalize -H "Content-Type: application/json" --data @-
```
