#### Label specific node
```
kubectl label nodes <node-name> clustertype=daskhub
```

#### Retrieve nodes with specific label
kubectl get nodes -l clustertype=daskhub
