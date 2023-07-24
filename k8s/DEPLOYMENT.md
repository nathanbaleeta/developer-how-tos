#### Get all deployments in given namespace
```
kubectl get deployment -n <my-namespace>
kubectl get deployment -n cloud-erp
```

#### Create deployment using docker image in specified namespace
```
kubectl create deployment <my-deployment> -n <my-namespace>
kubectl create deployment webapp-depl -n cloud-erp
```

#### Create a deployment named my-dep that runs the busybox image with 2 replicas and expose port 5701 in given namespace
```
kubectl create deployment my-dep \
                          --image=busybox \
                          --replicas=2 \
                          --port=5701 \
                          -n cloud-erp
```

#### Get details of specific deployment in given namespace
```
kubectl describe deployment <my-delpoyment> -n <my-namepsace>
kubectl describe deployment webapp-depl -n cloud-erp
```
#### Edit specific deployment in given namespace
```
kubectl edit deployment <my-deployment> -n <my-namespace>
kubectl edit deployment webapp-depl -n cloud-erp
```

#### Delete all deployment in given namespace
```
kubectl delete --all deployments -n <my-namespace>
```
