#### Forward traffic from K8s cluster service to host port
```
kubectl port-forward service/<service-name> host-port:cluster-port -n <my-namespace>
kubectl port-forward service/customer-erp-service 8090:8090 -n customer-erp-staging
```
