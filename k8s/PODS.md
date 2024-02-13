## Connect to pod bash shell
```
kubectl exec -n <namespace> -it <name_of_pod> -- /bin/bash
```

## Clean up evicted pods in specific namespace
```
kubectl -n <namespace> delete pods --field-selector=status.phase=Failed
```
## Display pod environment variables in in specific namespace
```
kubectl exec -n <namespace> <name_of_pod> -- printenv
```
## Create privileged user on Superset pod
```
kubectl exec -n <namespace> -it <SUPERSET_POD> -- superset fab create-admin
```

