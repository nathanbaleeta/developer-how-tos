
#### To expose port 8047 for your deployment
```
kubectl expose deployment <name-of-deployment> --type=<type> --port=<port> --target-port=<target-port> --name=<name-of-svc> -n <my-namespace>
kubectl expose deployment drill-depl --type=ClusterIP --port=8047 --target-port=8047 --name=drill-svc -n drill-dev
```

```
kubectl expose deployment drill-depl \
    --type LoadBalancer \
    --port 8047 \
    --target-port 8047 \
    --name=drill-svc \
    -n drill-dev
```
