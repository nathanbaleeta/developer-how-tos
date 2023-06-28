#### Create deployment using docker image in specified namespace
```
kubectl create deployment nginx-depl -n <my-namespace>
kubectl create deployment webapp-depl -n cloud-erp
```
#### Get details of specific deployment in given namespace
```
kubectl describe deployment <my-delpoyment> -n <my-namepsace>
kubectl describe deployment webapp-depl -n cloud-erp
```
