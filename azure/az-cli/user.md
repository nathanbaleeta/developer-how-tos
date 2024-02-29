## Manage Azure Active Directory [users and user authentication](https://learn.microsoft.com/en-us/cli/azure/ad/user?view=azure-cli-latest#az-ad-user-create)

#### Create an Azure Active Directory user
```
az ad user create --display-name <SomeUser>
                  --password <pass>
                  --user-principal-name <someuser@contoso.com>
```
#### Delete Azure Active Directory user
```
az ad user delete --id <myuser@contoso.com>
```

#### List Azure Active Directory users
```
az ad user list
```

#### Show details for a Azure Active Directory user
```
az ad user show --id <myuser@contoso.com>
```
