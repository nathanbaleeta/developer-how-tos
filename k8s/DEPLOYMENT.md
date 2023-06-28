#### Create deployment using docker image in specified namespace
```
kubectl create deployment nginx-depl -n <my-namespace>
kubectl create deployment nginx-depl -n cloud-erp
```
#### Get details of specific deployment in given namespace
```
kubectl describe namespace <my-namespace>
kubectl describe namespace cloud-erp
```
