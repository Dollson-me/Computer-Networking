# Extended ACL

[← Indeks wiki](../index.md)

> **Źródło główne:** Computer Networking Textbook.pdf, s. 195–199. Treść została uporządkowana tematycznie; pełny ekstrakt źródłowy znajduje się w `_source-archive/`.


## Materiał kanoniczny

Extended ACLs filter packets based on the following attributes:
© Source and destination IP addresses.
e Source and destination Layer4 protocols (UDP and TCP).
e Protocol type or number. For example: IP, HTTPS, 80, etc.
Extended ACLs use the following range of numbers: 100 to 199 and 2000 to 2699.
Configure Extended ACLs as close as possible to the source of the traffic being filtered.
Doing so ensures that traffic will be denied, and prevented from traversing the network
infrastructure.
It’s important to understand that even if the ACL is not placed as close as possible to
the source, the ACL will still operate as it should.
Standard Numbered Extended ACL Configuration
The numbers Extended ACLs use are 100-199 and 2000-2699.
In the protocol field, insert the name of the internet protocol, such as UDP, TCP, or
ICMP.
Source — The origin of the packet.
Destination — Where the packet is being sent to.
Operator — Compares source or destination ports, and can be It (less than), gt (greater
than), eq (equal), neq (not equal), or range (inclusive range).
Port is the number or name of an active TCP or UDP port.

Example:
Router(config)#access-list <access-list-number> <deny|permit|remark>
<Protocol> <source-address> <source-wildcard> <operator> <Port
Number\Name> <destination-address> <destination wildcard> <operator>
<Port Number\Name>
Ex1.
R1(config)#access-list 180 deny tcp 192.168.10.1 0.0.0.255 192.168.10.2
@.0.0.255 eq ftp
Ex2.
R1(config)#access-list 181 permit tcp 192.168.10.0 @.0.0.255 any eq www
//Appling on an interface
R1(config)#interface f0/0
R1(config-if)#ip access-group 18@ out
R1(config-if)#ip access-group 181 in
Standard Named ACL Configuration
Step1: Define a Named Access List using the command ip access-list extended.
Step2: Specify the conditions (Permit/Deny).
Step3: In configuration mode, choose an interface on which to apply the ACL, and apply
the ACL using ip access-group (in the correct direction).
Verify that the ACL is configured correctly using the show access-list command, and
save the configuration in the startup-config file.
Example:
R1(config)#ip access-list extended <name>
R1(config-ext-nac1)# <deny|permit|remark> <Protocol> <source-address>
<source-wildcard> <destination-address> <destination-wildcard> <operator>
<port number\name>
Ex.
R1(config)# ip access-list extended WEB
R1(config)# permit tcp 192.168.10.0 @.0.0.255 any eq 443
R1(config)# permit tcp 192.168.10.@ @.0.0.255 192.168.11.1 @.0.0.255 eq
telnet
R1(config)#interface f0/e
R1(config)# ip access-group WEB

Configuration Display Methods
ACL rule verification can be implement in several ways, one of which is to search the
running-config file using an include filter.
The output of the command show running-config | include access-list shows
configured Numbered and Named ACLs.
The command show access-list can also be used.
Example:
Rl#show access-lists
Extended IP access list 180
10 deny tcp 192.168.10.0 0.0.0.255 192.168.10.0 @.0.0.255 eq ftp
Extended IP access list 181
10 permit tcp 192.168.10.0 @.0.@.255 any eq www
Extended IP access list WEB
10 permit tcp 192.168.10.0 @.0.0.255 any eq 443
280 permit tcp 192.168.10.0 0.0.0.255 192.168.11.0 @.0.0.255 eq telnet
Extended ACL Examples
Scenario #1:
Due to new procedures and changes in the organizational structure, Hosts A and C are
not allowed to communicate.
Scenario #2:
The network administrator decided that the enterprise department on network
10.0.0.0/24 cannot access the FTP service on the FTP server, due to the risk of exposing
sensitive information. It can however receive services from the same server, such as
DHCP.

—,
CI a
—— ———/ =i ae)
—M™*s:s nh =
——
Host A Gigo/i Seay Gigo/2 er
192.168.0,10/24 Sew pascal:
Gig0/3 ws
| =
-—— >
—/ ae
10.0.0.20/24
= =|
= Le)
DNS Server FTP Server
172.16.1.1/24 172.16.1.2/24
Extended Numbered ACL Configuration Example
The following extended ACL configuration example is based on scenario #1 above.
Step 1 - Create a numbered ACL using the access-list command.
Step 2 - Choose the interface for which the ACL will apply, using the interface
command.
Step 3 — The ip access-group 1 in command links ACL 1 to the GigabitEthernet 0/1
interface in the inbound direction.
R1(config)#access-list 100 deny ip host 192.168.0.1@ host 10.0.0.20
R1(config)#access-list 100 permit ip any any
R1(config)#interface gigabitEthernet 0/1
R1(config-if)#ip access-group 100 in
R1(config-if)#exit

Extended Named ACL Configuration Example
The following extended ACL configuration example is based on scenario #2 above.
Step 1 - Use the ip access-list standard command to create a named ACL.
Step 2 - In ACL configuration mode, create Deny and Permit ACE statements.
Step 3 - Apply the ACL on an interface using the ip access-group command and specify
the traffic direction (in or out).
R1(config)#ip access-list extended
R1(config-ext-nacl)#deny tcp 10.0.0.0 @.0.0.255 host 172.16.1.2 eq 21
R1(config-ext-nacl)#deny tcp 10.0.0.0 0.0.0.255 host 172.16.1.2 eq 20
R1(config-ext-nacl)#permit ip any any
R1(config-ext-nacl)#exit
R1(config)#interface gigabitEthernet 0/2
R1(config-if)#ip access-group in
R1(config-if)#exit
Verify ACL Settings
ACL rules can be verified in various ways, one of which is by searching the running-
config file using an include filter.
Run the show running-config command to display on which interface each ACL is
applied. The show access-list command can also be used.
R2#
Extended IP access list 100
10 deny ip host 192.168.0.1@ host 10.0.0.20
20 permit ip any any
Extended IP access list Block_FTP
10 deny tcp 10.0.0.0 0.0.0.255 host 172.16.1.2 eq 21
20 deny tcp 10.0.0.0 0.0.0.255 host 172.16.1.2 eq 20
3@ permit ip any any
R1i#
interface GigabitEthernet0/1
ip address 192.168.0.15@ 255.255.255.0
ip access-group 100 in
!
interface GigabitEthernet0/2
ip address 10.0.0.15@ 255.255.255.0
ip access-group Block_FTP in

## Powiązane laboratoria

- [NET-11-LS1](../labs/net-11-ls1.md)


## Uzupełnienia z notatek Riseup / zajęć

<details>
<summary>Pokaż notatki prowadzącego, dodatkowe komendy i linki powiązane z tym tematem</summary>

R2(config)#ip access-list extended 100
R2(config-ext-nacl)#exit
R2(config)#access-list 100 deny ip host 172.16.2.1 host 192.168.1.2
R2(config)#access-list 100 permit ip any any
R2(config)#interface gigabitEthernet 0/1
R2(config-if)#ip access-group 100 in
R2(config-if)#exit
R2(config)#do show access-list
R1(config)#ip access-list extended BLOCK_HTTP
R1(config-ext-nacl)#deny tcp host 192.168.1.2 host 172.16.1.2 eq 80

R1(config-ext-nacl)#permit ip any any
R1(config-ext-nacl)#exit

</details>

## Powiązane tematy

- [ACL overview](acl-overview.md)
- [Standard ACL](standard-acl.md)

## Źródła w zestawie

- `Computer Networking Textbook.pdf` — strony 195–199.
- `Computer Networking.pdf` — prezentacja kursowa; odpowiadający rozdział zachowany w `_source-archive/02-Course-Slides.md`.
- `Padriseup Computer Networking.pdf` — uzupełnienia i materiały dodatkowe, jeśli występowały dla tego tematu.
