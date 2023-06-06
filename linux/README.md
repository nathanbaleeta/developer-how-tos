# Linux commands for Ubuntu or Debian

#### Display all network interfaces
```
ip link show
```
#### Check an IP address of a specific network interface
```
ip addr show eth2 
ip --color addr show eth2  # displays IP address in coloured output
```
#### Enable or disable network interface
```
ip link set eth2 up | down
```
