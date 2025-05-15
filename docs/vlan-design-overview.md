# 🌐 VLAN Design Overview

| VLAN | Name | Subnet | Purpose |
|------|------|--------|---------|
| 10 | USERS | 192.168.10.0/24 | Wired clients & lab PCs |
| 20 | WIFI | 192.168.20.0/24 | Wireless devices / APs |
| 30 | SERVERS | 192.168.30.0/24 | Dell R620 VMs, FortiGate |
| 99 | BLACKHOLE | — | Native VLAN, quarantine |
| 100 | MGMT | 192.168.100.0/24 | Switch, router, SonicWall UI, iDRAC |

> **Why this design?**  
> - Clear segmentation for security testing  
> - Matches CCNA study objectives  
> - Allows FortiGate policies between user, Wi-Fi, and server zones
