PS: If you'd rather use a SAS token to authorize access to blob data, then you can append that token to the resource URL in each AzCopy command. For example: 
```
https://<storage-account-name>.blob.core.windows.net/<container-name><SAS-token>
```

#### Download the [AzCopy portable binary](https://learn.microsoft.com/en-us/azure/storage/common/storage-use-azcopy-v10?tabs=dnf#download-the-azcopy-portable-binary)
```
wget https://aka.ms/downloadazcopy-v10-linux
```

### Extract [tar.gz](https://askubuntu.com/questions/25347/what-command-do-i-need-to-unzip-extract-a-tar-gz-file)
```
tar -xvzf downloadazcopy-v10-linux
```

#### Download a blob
```
azcopy copy 'https://mystorageaccount.blob.core.windows.net/mycontainer/myTextFile.txt' '/tmp/myTextFile.txt'
```

#### Download a directory
```
azcopy copy 'https://<storage-account-name>.<blob or dfs>.core.windows.net/<container-name>/<directory-path>' '<local-directory-path>' --recursive
```
