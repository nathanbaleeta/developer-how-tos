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
 --address-prefix 10.224.0.0/12 \
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
#### List subnets in a virtual network
```
az network vnet subnet list -g MyResourceGroup --vnet-name MyVNet
```

### Create an application gateway
Use az network application-gateway create to create the application gateway named myAppGateway. When you create an application gateway using the Azure CLI, you specify configuration information, such as capacity, sku, and HTTP settings. The application gateway is assigned to myAGSubnet and myPublicIPAddress that you previously created.
```
az network application-gateway create \
 --name myAppGateway \
 --location eastus \
 --resource-group myResourceGroupAG \
 --vnet-name myVNet \
 --subnet myAGsubnet \
 --capacity 2 \
 --sku Standard_v2 \
 --http-settings-cookie-based-affinity Disabled \
 --frontend-port 80 \
 --http-settings-port 80 \
 --http-settings-protocol Http \
 --public-ip-address myAGPublicIPAddress \
 --priority 100
```

It may take several minutes for the application gateway to be created. After the application gateway is created, you'll see these new features:

* appGatewayBackendPool - An application gateway must have at least one backend address pool
* *appGatewayBackendHttpSettings* - Specifies that port 80 and an HTTP protocol is used for communication.
* *appGatewayHttpListener* - The default listener associated with appGatewayBackendPool.
* *appGatewayFrontendIP* - Assigns myAGPublicIPAddress to appGatewayHttpListener.
* *rule1* - The default routing rule that is associated with appGatewayHttpListener.

### Test the application gateway

To get the public IP address of the application gateway, use az network public-ip show. Copy the public IP address, and then paste it into the address bar of your browser.

```
az network public-ip show \
 --resource-group myResourceGroupAG \
 --name myAGPublicIPAddress \
 --query [ipAddress] \
 --output tsv
```

### Clean up resources

When no longer needed, remove the resource group, application gateway, and all related resources.
```
az group delete --name myResourceGroupAG --location eastus
```

