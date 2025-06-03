# VLANs
- Vlan 10: admin (Para poder configurar por SSH)
  - 192.168.10.0/24
- Vlan 20: LAN
  - 172.16.0.0/16
- Vlan 30: streaming
- Vlan 40: servidores
  - 10.11.11.32/27
- Vlan 100: WLAN (Wireless)
  - 10.20.0.0/16
- Vlan 199: prohibido (Todos puertos no en uso)

# VTP
```
vtp mode client/server 
vtp domain Leo
vtp password leonardo
```
