
#### To expose port 8047 for your deployment
```
kubectl expose deployment drill-depl --type=ClusterIP --port=8047 --target-port=8047 --name=drill-svc -n drill-dev
```
