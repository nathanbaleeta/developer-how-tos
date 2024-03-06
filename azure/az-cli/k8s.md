## Set up basic AKS cluster

#### Create resource group 
```
az group create --name myResourceGroup --location eastus
```

#### Create basic cluster with managed identity enabled
```
az aks create --resource-group myResourceGroup \
    --name myAKSCluster \
    --enable-managed-identity \
    --node-vm-size standard_dc2s_v3 \
    --node-count 2 \
    --generate-ssh-keys
```
#### Connect kubectl and make sure commands can be run against the cluster
```
az aks get-credentials --resource-group myResourceGroup --name myAKSCluster
```

#### Verfiy cluster nodes are running
```
kubectl get nodes
```

#### Tear down resource group including all resources created under it
```
az group delete --name myResourceGroup
```
