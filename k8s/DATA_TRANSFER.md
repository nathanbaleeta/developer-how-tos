#### Copy files from kubernetes pod to local system
```
kubectl exec -n <namespace> <pod> -- cat <src-file> > <dest-file> 
```
