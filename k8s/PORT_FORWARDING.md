#### Forward traffic from K8S service to localhost port
```
kubectl port-forward service/<service-name> localhost-port:cluster-port -n <my-namespace>
```
