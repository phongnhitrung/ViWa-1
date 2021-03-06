---
# __SO SÁNH OPEN SOURCE FIREWALL
---

## __1. Core_

|           |                          | PFSENSE                   | IPFire                    | OPNSense                  | Untangle                  | ClearOS                   | IPCop                     | UFW                       |
| --------- | ------------------------ | ------------------------- | ------------------------- | ------------------------- | ------------------------- |-------------------------  | ------------------------- | ------------------------- |
| Layer2    | Technology               | FreeBSD, ipfw, pf         |                           | FreeBSD, ipfw, pf         | Debian                    | CentOS, iptables          |                           |                           |
|           | VLAN                     | no                        | yes                       |                           |                           |                           |                           |                           |
|           | OpenVswitch              | no                        | yes                       |                           |                           |                           |                           |                           |
|           | Bridge                   | yes                       | yes                       |                           |                           |                           |                           |                           | 
| Layer3    | Technology               | FreeBSD, ipfw, pf, carp   |                           | FreeBSD, ipfw, pf, carp   | Debian                    | CentOS, iptables          |                           |                           |
|           | Packet filter            | yes                       | yes                       |                           |                           |                           |                           |                           |
|           | NAT                      | yes                       | yes                       |                           |                           |                           |                           |                           |
|           | Router                   | yes                       | yes                       |                           |                           |                           |                           |                           |
|           | VPN                      | no                        | yes                       |                           |                           |                           |                           |                           | 
|           | GRE Tunnel               | no                        | yes                       |                           |                           |                           |                           |                           | 
|           | OpenVPN                  | no                        | yes                       |                           |                           |                           |                           |                           | 
|           | Multi WAN                | no                        | yes                       |                           |                           |                           |                           |                           | 
|           | Virtual IP               | yes                       | yes                       |                           |                           |                           |                           |                           | 
|           | High Avaibility          | yes                       | yes                       |                           |                           |                           |                           |                           | 
|           | IPSec                    | yes                       | yes                       |                           |                           |                           |                           |                           | 
| Layer4    | Technology               | FreeBSD, ipfw, pf         | IPVS                      | FreeBSD, ipfw, pf         | Debian                    | CentOS, iptables          |                           |                           |
|           | Stateful contrack table  | yes                       | yes                       |                           |                           |                           |                           |                           |
|           | Circuit-level FW         | yes                       | yes                       |                           |                           |                           |                           |                           | 
|           | L4 LB                    | no                        | yes                       |                           |                           |                           |                           |                           |
|           | L4 traffic shaping       | no                        | no                        |                           |                           |                           |                           |                           | 
|           | L4 traffic blocking      | yes                       | yes                       |                           |                           |                           |                           |                           | 
| App layer | Technology               | Snort/Suri, HAProxy (*)   | Snort/Suri                | Snort/Suri                |                           |                           |                           |                           |
|           | Proxy Server             | yes                       | yes                       |                           |                           |                           |                           |                           |  
|           | L7 LB                    | yes                       | yes                       |                           |                           |                           |                           |                           | 
|           | WAF                      | yes                       | yes                       |                           |                           |                           |                           |                           |
|           | DNS server               | yes                       | no                        |                           |                           |                           |                           |                           |
|           | DNS proxy                | yes                       | yes                       |                           |                           |                           |                           |                           |
|           | DHCP server              | yes                       | yes                       |                           |                           |                           |                           |                           | 
|           | IPS                      | yes                       | yes                       |                           |                           |                           |                           |                           |
|           | IDS                      | yes                       | yes                       |                           |                           |                           |                           |                           | 
|           | L7 traffic shaping       | yes                       | yes                       |                           |                           |                           |                           |                           | 
|           | L7 traffic blocking      | yes                       | yes                       |                           |                           |                           |                           |                           |
|           | P2P blocking             | yes                       | yes                       |                           |                           |                           |                           |                           |


- (*): Pfense cho phép tích hợp thêm các optional package ở tầng application để mở rộng tính năng


## __2. UI__

