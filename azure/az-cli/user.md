## Manage Azure Active Directory [users and user authentication](https://learn.microsoft.com/en-us/cli/azure/ad/user?view=azure-cli-latest#az-ad-user-create)

#### Create an Azure Active Directory user
```
az ad user create --display-name <SomeUser>
                  --password <pass>
                  --user-principal-name <someuser@contoso.com>
```