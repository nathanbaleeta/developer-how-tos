# Linux commands for Ubuntu or Debian

#### Display all network interfaces
```
ip link show
```
#### Check an IP address of a specific network interface
```
ip addr show eth2 
ip --color addr show eth2  # displays IP address in coloured output
ip -j -p addr show eth2 # display JSON output
```
#### Enable or disable network interface
```
ip link set eth2 up | down
```
#### Add or remove IP address from network interface
```
sudo ip addr add | del 172.19.1.10/24 dev eth2
```
#### Flush (remove all) ip addresses of network interface
```
sudo ip addr flush eth2
```
