### Tutorials
- [Use the Azure Key Vault provider for Secrets Store CSI Driver in an Azure Kubernetes Service (AKS) cluster](https://learn.microsoft.com/en-us/azure/aks/csi-secrets-store-driver)
- [Connect your Azure identity provider to the Azure Key Vault Secrets Store CSI Driver in Azure Kubernetes Service (AKS)](https://learn.microsoft.com/en-us/azure/aks/csi-secrets-store-identity-access?tabs=azure-portal&pivots=access-with-service-connector)

#### Checking the expiration date of the SSL certificate
```
openssl x509 -noout -dates -in domain.crt
```

#### Verify certificate file
```
openssl x509 -noout -text -in domain.crt
```

#### Check CSR file
```
openssl req -noout -text -in domain.csr
```

#### Check PEM file
```
openssl x509 -in certificate.pem -text
```

#### Check private key file
```
openssl rsa -in privateKey.key -check
```
OR
```
openssl rsa -noout -text -in domain.key
```

#### Checking the server’s SSL certificate
```
openssl s_client -showcerts -connect example.org:443
```

### Verify Distinguished Name of SSL Certificate
```
openssl x509 -noout -subject -in domain.crt
```
