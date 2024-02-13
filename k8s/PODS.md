## Connect to pod bash shell
```
kubectl exec -n <namespace> -it <name_of_pod> -- /bin/bash
```

Clean up evicted pods in specific namespace
```
kubectl -n <namespace> delete pods --field-selector=status.phase=Failed
```
