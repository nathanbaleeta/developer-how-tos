## Set up basic AKS cluster

#### List K8s available as of today
```
az aks get-versions --location westeurope -o table
```

#### Create resource group 
```
az group create --name myResourceGroup --location eastus
```

#### Create basic [cluster](https://learn.microsoft.com/en-us/cli/azure/aks?view=azure-cli-latest#az-aks-create) with managed identity enabled
```
az aks create --resource-group myResourceGroup \
    --name myAKSCluster \
    --enable-managed-identity \
    --node-vm-size standard_dc2s_v3 \
    --node-count 2 \
    --generate-ssh-keys
```
#### Configure [kubectl](https://learn.microsoft.com/en-us/azure/aks/learn/quick-kubernetes-deploy-cli) to connect to your Kubernetes cluster
```
az aks get-credentials --resource-group myResourceGroup --name myAKSCluster
```

#### Verfiy cluster nodes are running
```
kubectl get nodes
```

#### Show the [dashboard](https://learn.microsoft.com/en-us/cli/azure/aks?view=azure-cli-latest#az-aks-browse(aks-preview)) for a K8s cluster in a web browser
```
az aks browse --name myAKSCluster --resource-group MyResourceGroup
```

#### Validate the [ACR](https://learn.microsoft.com/en-us/cli/azure/aks?view=azure-cli-latest#az-aks-check-acr) is accessible from the AKS cluster

```
az aks check-acr --name myAKSCluster --resource-group MyResourceGroup --acr myacr.azurecr.io
```

#### [Manually scale the node count](https://learn.microsoft.com/en-us/azure/aks/scale-cluster?tabs=azure-cli)
Get the name of your node pool using the ```az aks show``` command:
```
az aks show --resource-group myResourceGroup --name myAKSCluster --query agentPoolProfiles
```

Scale the cluster nodes using the ```az aks scale``` command
```
az aks scale --resource-group myResourceGroup --name myAKSCluster --node-count 1 --nodepool-name <your node pool name>
```

#### Tear down resource group including all resources created under it
```
az group delete --name myResourceGroup
```

#### Start an AKS cluster
```
az aks start --name myAKSCluster --resource-group myResourceGroup
```
