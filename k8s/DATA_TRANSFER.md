#### Copy files from kubernetes remote pod to local system
```
kubectl exec -n <namespace> <pod> -- cat <src-file> > <dest-file>

kubectl exec -n my-namespace customer-erp-postgresql-0 -- cat /tmp/database_dump.tgz > /tmp/database_dump.tgz
```
