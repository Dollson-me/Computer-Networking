# Projekt Cisco — integracja całego materiału

Źródło: `Cisco projekt.pdf` (9 stron).

## Lab Task 1 — podział 172.16.10.0/24 na 8 podsieci

Maska: `/27` = `255.255.255.224`, rozmiar bloku 32 adresy.

| # | Network address | Usable hosts | Broadcast |
|---:|---|---|---|
| 1 | 172.16.10.0/27 | 172.16.10.1–172.16.10.30 | 172.16.10.31 |
| 2 | 172.16.10.32/27 | 172.16.10.33–172.16.10.62 | 172.16.10.63 |
| 3 | 172.16.10.64/27 | 172.16.10.65–172.16.10.94 | 172.16.10.95 |
| 4 | 172.16.10.96/27 | 172.16.10.97–172.16.10.126 | 172.16.10.127 |
| 5 | 172.16.10.128/27 | 172.16.10.129–172.16.10.158 | 172.16.10.159 |
| 6 | 172.16.10.160/27 | 172.16.10.161–172.16.10.190 | 172.16.10.191 |
| 7 | 172.16.10.192/27 | 172.16.10.193–172.16.10.222 | 172.16.10.223 |
| 8 | 172.16.10.224/27 | 172.16.10.225–172.16.10.254 | 172.16.10.255 |

## Lab Task 2 — VLAN, access ports, trunk i native VLAN

Tworzone VLAN-y:

```text
vlan 10
 name Management
vlan 20
 name Marketing
vlan 30
 name Accounting
vlan 100
 name Native
```

Przypisania access:

```text
interface range FastEthernet 0/1-10
 switchport mode access
 switchport access vlan 10
interface range FastEthernet 0/11-20
 switchport mode access
 switchport access vlan 20
interface range FastEthernet 0/21-24
 switchport mode access
 switchport access vlan 30
```

Trunki i native VLAN:

```text
interface range GigabitEthernet 0/1-2
 switchport mode trunk
 switchport trunk native vlan 100
```

Weryfikacja: `show interfaces switchport`, `show interfaces trunk`. Dla portów access użyto także `switchport nonegotiate`. Konfiguracja jest zapisywana przez `copy running-config startup-config`.

## Lab Task 3 — adresacja interfejsów i hostów

- R3 `GigabitEthernet0/0`: `172.16.10.1 255.255.255.224`, `no shutdown`.
- R3 `GigabitEthernet0/1`: `172.16.10.33 255.255.255.224`, `no shutdown`.
- Weryfikacja: `do show ip route`.
- Adresy wykorzystywane na łączach szeregowych w projekcie: `172.16.10.65`, `.66`, `.97`, `.98`, `.129`, `.130` z maską `/27`.
- Konfiguracja hostów w Packet Tracerze obejmuje m.in. CEO1 `.189`, CEO2 `.190`, Copyrighter1 `.221`, Copyrighter2 `.222`, Dialer1 `.253`, Dialer2 `.254`, a także hosty Office 2/Office 3, Guest, Admin, Syslog/NTP Server i E-mail Server. Pełne wartości ze screenshotów są zachowane niżej w transkrypcji stron 4–5.

## Lab Task 4 — Router-on-a-Stick

Fizyczny `GigabitEthernet0/0` jest uruchamiany `no shutdown`. Powstają subinterfejsy:

```text
interface GigabitEthernet 0/0.10
 encapsulation dot1Q 10
 ip address 172.16.10.161 255.255.255.224
interface GigabitEthernet 0/0.20
 encapsulation dot1Q 20
 ip address 172.16.10.193 255.255.255.224
interface GigabitEthernet 0/0.30
 encapsulation dot1Q 30
 ip address 172.16.10.225 255.255.255.224
```

Weryfikacja: `show ip interface brief`. Po stronie switcha porty GigabitEthernet są ustawiane jako trunk, a native VLAN to 100; używane jest `show interfaces trunk`.

## Task 5 — Port Security

```text
show port-security address
interface FastEthernet 0/2
 switchport mode access
 switchport port-security
 switchport port-security violation restrict
 switchport port-security mac-address sticky
show interfaces status
```

Konfiguracja jest powtarzana na S1 i S2 m.in. dla `Fa0/1`, `Fa0/11`, `Fa0/21`. Nieużywane zakresy portów są wyłączane przez `shutdown` (w materiale pokazano m.in. `interface range FastEthernet 0/12-20`). Na końcu `copy running-config startup-config`.

## Task 6 — OSPF

- `show ip route connected`;
- uruchomienie wymaganych interfejsów (`no shutdown`);
- `router ospf 1`;
- ustawienie `router-id`;
- polecenia `network ... wildcard ... area 0`;
- `passive-interface`;
- weryfikacja: `show ip protocols`, `show ip ospf interface`, `show ip ospf neighbor`;
- zapis konfiguracji.

## Task 7 — ACL

Materiał pokazuje rozszerzoną regułę blokującą komunikację pomiędzy konkretnymi hostami:

```text
access-list 137 deny ip host 172.16.10.60 host 172.16.10.29
show access-lists
```

## Task 8 — lokalne konto i zabezpieczenie konfiguracji

```text
username Admin password ACDC1973
enable password beatles1960
service password-encryption
banner motd #Only authorized personnel are allowed accessing this device#
wr
```

## Task 9 — SSH

```text
ip domain-name Cyber.local
hostname R1
crypto key generate rsa
# modulus: 1024
ip ssh version 2
line vty 0 4
 login local
 transport input ssh
show ip ssh
show ssh
```

W logu widoczny jest komunikat aktywacji SSH 1.99/2.0, timeout uwierzytelnienia 120 s, 3 próby oraz sesja z szyfrowaniem AES128-CBC i HMAC-SHA1.



## Powiązania z wiki

- [Subnetting](../05-addressing-routing/subnetting.md)
- [VLANs](../06-vlans-switching/vlans.md)
- [802.1Q trunking](../06-vlans-switching/trunking.md)
- [Inter-VLAN routing / Router-on-a-Stick](../06-vlans-switching/inter-vlan-routing.md)
- [Port Security](../04-switch-security/port-security.md)
- [OSPFv2](../05-addressing-routing/ospfv2.md)
- [ACL](../07-operations-security/acl-overview.md)
- [SSH](../04-switch-security/ssh-svi-vty.md)

> Pełna transkrypcja dziewięciu stron źródła znajduje się w `_source-archive/05-Cisco-Project.md`.
