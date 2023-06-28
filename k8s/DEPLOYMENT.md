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
