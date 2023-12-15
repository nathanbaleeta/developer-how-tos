#### Install PostgreSQL on Mac local machine

```
brew install postgresql@14
```

#### View information about PostgreSQL on machine
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
