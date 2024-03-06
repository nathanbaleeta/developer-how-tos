### Create a resource group

A resource group is a logical container into which Azure resources are deployed and managed
```
az group create --name myResourceGroupAG --location eastus
```

### Create network resources
Create the virtual network named ```myVNet``` and the subnet named ```myAGSubnet``` using az network vnet create. You can then add the subnet named ```myBackendSubnet``` needed by the backend servers using az network vnet subnet create. Create the public IP address named ```myAGPublicIPAddress``` using az network public-ip create.

```
az network vnet create \
 --name myVNet \
 --resource-group myResourceGroupAG \
 --location eastus \
 --address-prefix 10.0.0.0/16 \
 --subnet-name myAGSubnet \
 --subnet-prefix 10.0.1.0/24

az network vnet subnet create \
 --name myBackendSubnet \
 --resource-group myResourceGroupAG \
 --vnet-name myVNet \
 --address-prefix 10.0.2.0/24

az network public-ip create \
 --resource-group myResourceGroupAG \
 --name myAGPublicIPAddress \
 --allocation-method Static \
 --sku Standard
```
