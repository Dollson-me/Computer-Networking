# Command reference

[← Indeks wiki](../index.md)

Ta strona grupuje polecenia występujące w materiałach według środowiska i celu. Szczegółowy kontekst każdego polecenia jest na stronach tematycznych i w laboratoriach.

## Windows networking CLI

| Cel | Polecenie |
|---|---|
| test łączności | `ping <host>` |
| konfiguracja IP | `ipconfig` |
| pełna konfiguracja IP | `ipconfig /all` |
| zwolnienie dzierżawy DHCP | `ipconfig /release` |
| odnowienie dzierżawy DHCP | `ipconfig /renew` |
| wyczyszczenie cache DNS | `ipconfig /flushdns` |
| DNS / reverse DNS | `nslookup <host-or-ip>` |
| konkretny typ rekordu DNS | `nslookup -q=TXT <domain>` |
| śledzenie trasy | `tracert <host>` |
| konfiguracja sieci | `netsh interface ip ...` |
| tablica ARP | `arp -a` / `arp -g` |
| usunięcie cache ARP | `arp -d` |
| statyczny wpis ARP | `arp -s <ip> <mac>` |
| aktywne porty / procesy | `netstat -ab` |
| tablica routingu hosta | `route print` |
| dodanie trasy | `route add ...` |
| usunięcie trasy | `route delete ...` |

## Cisco IOS — nawigacja i konfiguracja

```text
enable
configure terminal
conf t
exit
end
show running-config
show startup-config
copy running-config startup-config
write memory
wr
```

## Cisco IOS — podstawowa konfiguracja i bezpieczeństwo

```text
hostname <name>
username <user> password <password>
enable password <password>
service password-encryption
banner motd #message#
line console 0
 login local
```

## Interfejsy i diagnostyka

```text
interface GigabitEthernet 0/0
ip address <ip> <mask>
no shutdown
shutdown
show ip interface brief
show interfaces status
show interfaces switchport
show interfaces trunk
show mac-address-table
show ip route
show ip route connected
```

## VLAN / trunk / router-on-a-stick

```text
vlan <id>
 name <name>
interface range FastEthernet 0/1-4
 switchport mode access
 switchport access vlan <id>
interface GigabitEthernet 0/1
 switchport mode trunk
 switchport trunk native vlan <id>
 switchport nonegotiate
interface GigabitEthernet 0/0.<id>
 encapsulation dot1Q <id>
 ip address <ip> <mask>
show vlan brief
```

## Port Security

```text
switchport port-security
switchport port-security maximum <n>
switchport port-security mac-address <mac>
switchport port-security mac-address sticky
switchport port-security violation shutdown
switchport port-security violation restrict
switchport port-security violation protect
show port-security
show port-security address
show port-security interface <interface>
```

## SSH / VTY / SVI

```text
ip domain-name <domain>
crypto key generate rsa
ip ssh version 2
line vty 0 4
 login local
 transport input ssh
interface vlan 1
 ip address <ip> <mask>
 no shutdown
ip default-gateway <ip>
show ip ssh
show ssh
```

## Routing statyczny

```text
ip route <network> <mask> <next-hop|exit-interface>
ip route 0.0.0.0 0.0.0.0 <next-hop|exit-interface>
no ip route <network> <mask> <next-hop|exit-interface>
ipv6 route <prefix/length> <next-hop|exit-interface>
```

## RIPv2

```text
router rip
 version 2
 no auto-summary
 network <network>
 passive-interface <interface>
 default-information originate
show ip protocols
show ip route rip
```

## OSPFv2

```text
router ospf <process-id>
 router-id <id>
 network <network> <wildcard> area <area>
 passive-interface <interface>
 auto-cost reference-bandwidth <value>
show ip route ospf
show ip protocols
show ip ospf interface
show ip ospf neighbor
```

## ACL

```text
access-list <number> permit|deny ...
ip access-list standard <name>
ip access-list extended <name>
ip access-group <acl> in|out
show access-list
show access-lists
```

## Konfiguracja / IOS / TFTP

```text
copy running-config tftp:
copy tftp: flash:
boot system flash:<image>
config-register 0x2102
show version
reload
```

## IPv6

```text
ipv6 unicast-routing
interface <interface>
 ipv6 address <prefix/length>
show ipv6 interface brief
```
