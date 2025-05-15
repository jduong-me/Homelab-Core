# 🚀 Router‑on‑a‑Stick Setup (Cisco 2901)

1. **Enable trunk port Gi0/1** on switch and router  
2. **Create sub‑interfaces** on the router:

```plaintext
interface Gi0/1.10
 encapsulation dot1Q 10
 ip address 192.168.10.1 255.255.255.0
```

3. **Repeat** for VLAN 20, 30, 100  
4. **Verify** with `show ip int br` and `ping` gateways  
5. **Save** with `write memory`
