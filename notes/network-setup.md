**Home Network Lab – Setup Notes**

>This lab was designed to simulate a segmented enterprise-style network environment using virtualization and open-source tools. It combines routing, DNS filtering, and a media server behind a pfSense firewall on Proxmox.

---

**Infrastructure**

- Proxmox VE – Hypervisor hosting the entire lab
- pfSense – Virtual firewall with VLAN support
- AdGuard Home – DNS-level ad and tracker blocking
- Media Server – SMB shares and local streaming via Jellyfin (planned)
- Management VM – for updates, file transfers, and remote access

---

**Network Layout**

```
[WAN]
  |
[pfsense VM]
  ├── VLAN 10: LAN (AdGuard, Media Server)
  ├── VLAN 20: Admin (Proxmox WebUI, SSH, Updates)
  └── VLAN 30: IoT Test (Optional future segment)
```
