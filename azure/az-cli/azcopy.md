PS: If you'd rather use a SAS token to authorize access to blob data, then you can append that token to the resource URL in each AzCopy command. For example: `https://<storage-account-name>.blob.core.windows.net/<container-name><SAS-token>`

#### Download the [AzCopy portable binary](https://learn.microsoft.com/en-us/azure/storage/common/storage-use-azcopy-v10?tabs=dnf#download-the-azcopy-portable-binary)
```
wget -O azcopy_v10.tar.gz https://aka.ms/downloadazcopy-v10-linux && tar -xfv azcopy_v10.tar.gz --strip-components=1
```

#### Download a blob
```
azcopy copy 'https://mystorageaccount.blob.core.windows.net/mycontainer/myTextFile.txt' '/tmp/myTextFile.txt'
```

#### Download a directory
```
azcopy copy 'https://<storage-account-name>.<blob or dfs>.core.windows.net/<container-name>/<directory-path>' '<local-directory-path>' --recursive
```
