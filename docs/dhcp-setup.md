# 🛠 DHCP Setup Guide

## Goals
- Dynamically assign IPs in VLANs 10, 20, 30
- Exclude gateway addresses

### Commands

```plaintext
ip dhcp excluded-address 192.168.10.1 192.168.10.9
ip dhcp pool VLAN10
 network 192.168.10.0 255.255.255.0
 default-router 192.168.10.1
 dns-server 8.8.8.8 1.1.1.1
 lease 7
```

### Validation
- `show ip dhcp binding`
- Client `ipconfig /renew`
