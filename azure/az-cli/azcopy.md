#### Download the [AzCopy portable binary](https://learn.microsoft.com/en-us/azure/storage/common/storage-use-azcopy-v10?tabs=dnf#download-the-azcopy-portable-binary)

#### Download a blob
```
azcopy copy 'https://mystorageaccount.blob.core.windows.net/mycontainer/myTextFile.txt' '/tmp/myTextFile.txt'
```

#### Download a directory
```
azcopy copy 'https://<storage-account-name>.<blob or dfs>.core.windows.net/<container-name>/<directory-path>' '<local-directory-path>' --recursive
```
