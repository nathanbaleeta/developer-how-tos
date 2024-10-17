#### Label specific node
```
kubectl label nodes <node-name> clustertype=daskhub
```
#### Show labels on specific resource
```
kubectl get pods --show-labels
kubectl get no --show-labels
```
#### Retrieve nodes with specific label
```
kubectl get no -l clustertype=daskhub
kubectl get no -l local-storage-available=true
```
