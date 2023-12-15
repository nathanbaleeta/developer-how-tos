#### Install PostgreSQL on Mac local machine

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

####  Restart the service immediately and persist across reboots:
```
brew services restart postgresql@14
```
