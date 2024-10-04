### Install specific version of PostgreSQL e.g 14
```
brew install postgresql@14
```

### Uninstall specific version of PostgreSQL e.g 14
```
brew uninstall postgresql@14
```

### Check PostgreSQL version
```
postgres -V
```

### Upgrade PostgreSQL formulae within a version 
```
brew upgrade postgresql
```

#### Check status of PostgreSQL server Mac OS X
```
brew info postgresql
```

### Start or restart PostgreSQL automatically
```
brew services start | restart postgresql@14
```

### Connect to postgres shell
```
psql postgres
```

### PostgreSQL connection string. For Mac hostname use `localhost` 
```
psql://<UserName>:<DBPassword>@<Database Host>/<Database Name>
```
