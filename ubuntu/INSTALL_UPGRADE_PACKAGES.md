
#### Update your local package index to fetch the latest version details from the repositories
```
# bash
sudo apt update
```
#### Upgrade all installed packages
Updates your existing software to the latest versions
```
# bash
sudo apt upgrade
```

#### Search for a package
Displays matching names and descriptions.
```
# bash
apt search package_name
```
#### Show package info
Shows version details, dependencies, and a full description.
```
# bash
apt show package_name
```

#### List installed packages
Lists every package currently on your system
```
# bash
apt list --installed
```

#### List packages which need upgrading
```
# bash
sudo apt list --upgradable
```

#### Upgrade the specific package
```
# bash
sudo apt install --only-upgrade package
````

#### Upgrade multiple specific packages at once
```
# bash
sudo apt inistall --only-upgrade package1 package2 
```
