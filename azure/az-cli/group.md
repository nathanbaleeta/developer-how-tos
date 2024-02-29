## Manage Azure Active Directory groups

#### Create a group in the directory
```
az ad group create --display-name <MyDisplay> --mail-nickname <MyDisplay>
```

#### Delete a group from the directory
```
az ad group delete --group <display-name> | <groupId>
```

#### List groups in the directory
```
az ad group list
```

#### Get group information from the directory
```
az ad group show --group <display-name> | <groupId>
```
