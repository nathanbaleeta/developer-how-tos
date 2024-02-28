## Manage [Azure subscription](https://learn.microsoft.com/en-US/cli/azure/account?view=azure-cli-latest#az_account_show) information

#### Get a list of subscriptions for the logged in account
```
az account list
```

#### Get the details of a subscription
```
az account show
```

#### Set a subscription to be the current active subscription
```
az account set --subscription <mysubscription>
```

#### Clear all subscriptions from the CLI's local cache
```
az account clear
```
