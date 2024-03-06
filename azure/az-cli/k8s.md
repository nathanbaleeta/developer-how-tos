## Set up basic AKS cluster
```
az group create --name myResourceGroup --location eastus
```

```
az aks create --resource-group myResourceGroup \
    --name myAKSCluster \
    --enable-managed-identity \
    --node-vm-size standard_dc2s_v3 \
    --node-count 2 \
    --generate-ssh-keys
```

```
az aks get-credentials --resource-group myResourceGroup --name myAKSCluster
```

```
kubectl get nodes
```

```
az group delete --name myResourceGroup
```
