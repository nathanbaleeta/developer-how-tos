
#### Get details including OS image of nodes in node pool
```
kubectl get nodes -o wide
```

#### Gracefully remove node from AKS cluster
```
kubectl drain <node-name> --ignore-daemonsets --delete-emptydir-data
kubectl delete <node-name>
```
