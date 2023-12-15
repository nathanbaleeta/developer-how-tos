#### Install PostgreSQL on local machine

```
brew install postgresql@14
```

#### View current services running on machine - to confirm PostgreSQL is inclusive
```
brew services list
```

#### View information about PostgreSQL service
```
brew info postgresql
```

#### Run as foreground service
```
/opt/homebrew/opt/postgresql@14/bin/postgres -D /opt/homebrew/var/postgresql@14
```

#### To start postgresql@14 now and restart at login:
```
brew services start postgresql@14
```

#### Stop the service immediately and unregister from launching at boot 
```
brew services stop postgresql@14
```

####  Restart the service immediately and persist across reboots:
```
brew services restart postgresql@14
```

#### Stop the service but persist across reboots:
```
brew services kill postgresql@14
```
