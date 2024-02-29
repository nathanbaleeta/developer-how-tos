## Manage Azure Active Directory [group members](https://learn.microsoft.com/en-us/cli/azure/ad/group/member?view=azure-cli-latest)

#### Add a member to a group
```
az ad group member add \
            --group <displayName> \
            --member-id <objectId of user, service principal, group> 
```

#### Check if a member is in a group
```
az ad group member check \
            --group MyGroupDisplayName \
            --member-id xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
```

#### Get the members of a group
```
az ad group member list \
            --group <MyGroupDisplayName>
```

#### Remove a member from a group
```
az ad group member remove \
            --group MyGroupDisplayName \
            --member-id xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
```
