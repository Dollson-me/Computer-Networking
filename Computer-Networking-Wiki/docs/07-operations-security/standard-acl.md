# Standard ACL

[← Indeks wiki](../index.md)

> **Źródło główne:** Computer Networking Textbook.pdf, s. 191–194. Treść została uporządkowana tematycznie; pełny ekstrakt źródłowy znajduje się w `_source-archive/`.


## Materiał kanoniczny

Standard ACLs are placed as close to the destination as possible. Cisco set this rule
because placing standard ACLs at the source of traffic will prevent communication with
any network hosting interfaces to which the ACL applies.
Standard ACLs filter traffic only according to the source IP address.
Named or Numbered ACLs
ACLs can be assigned unique names or numbers.
Standard Named Access Control Lists allow unique names and numbers to be assigned
to ACLs.
The Standard Numbered ACL range is 1-99 and 1300-1999.
Standard Numbered ACL Command
Command F F f 1 :
Router(config)# i access-list <access-list-number> | <deny | permit |remark>i <source-address>! <source-wildcard>
0 : 1 ! 2 ! 3 ! 4 i 5
</>
0- To run the command, you must be in terminal configuration mode.
1 - Initial syntax to configure a Standard ACL.
2 - Decimal number from 1 to 99, or 1300 to 1999 (only for Standard ACLs).
3 - Deny - denies access if the conditions match, Permit - permits access if the
conditions match, Remark - adds a remark about entries.
4 - IP of the network or host from which the packets were sent. You can specify any
instead of using a 32-bit address.
5 - 32-bit wildcard mask that will be applied on the source.
Example:
R1(config)# access-list 10 permit 192.168.10.0 @.0.0.255

Standard ACL Scenario
Scenario #1:
A network administrator decided that new users on network 10.0.0.0/24 will not have
access to the server network, but will be able to communicate with neighboring
network 192.168.0.0/24
Scenario #2:
After malicious software was discovered on Host A, an administrator decided to
temporarily block access from the host to 10.0.0.0/24, until the threat is removed.
ml
—M™e:s nh =
= vets
Host A GigO/1 Gigd/2 10,0.0.10/24
192.168.0.10/24 bom] pra
+—————-*,
ans ‘
? Host C
10.0.0.20/24
=] al
— <=
DNS Server FIP Server
172.16,1.1/24 172.16,1.2/24
Standard Numbered ACL Configuration Example
The following ACL configuration example is based on scenario #1 above.
Step 1 - Create a numbered ACL using the access-list command.
Step 2 - Choose the interface for which the ACL will apply, using the interface command.
Step 3 — The ip access-group 1 out command links ACL 1 to the Gigabitethernet 0/3
interface in the outbound direction.

R1(config)#access-list 1 deny 10.0.0.0 @.0.0.255
R1(config)#access-list 1 permit any
R1(config)# interface Gigabitethernet 0/3
R1(config-if)#ip access-group 1 out
R1(config-if)#exit
Standard Named ACL Configuration Example
The following ACL configuration example is based on scenario #2 above.
Step 1 - Use the ip access-list standard command to create a named ACL.
Step 2 - In ACL configuration mode, create Deny and Permit ACE statements.
Step 3 - Apply the ACL on an interface using the ip access-group command, and specify
the traffic direction (in or out).
R1(config)# ip access-list standard
R1(config-std-nacl)#deny host 192.168.0.10
R1(config-std-nacl)#permit any
R1(config-std-nacl)#exit
R1(config)#interface Gigabitethernet 0/2
R1(config-if)#ip access-group out
R1(config-if)#exit
Verify ACL Settings
ACL rules can be verified in different ways, one of which is by searching the running-
config file using an include filter.
Run show running-config to display on which interface each ACL is applied.
The show access-list command can also be used.

R2#
Standard IP access list Block_Host_A
10 deny host 192.168.0.10
28 permit any
Standard IP access list 1
10 deny 10.0.0.0 0.0.0.255
28 permit any
R1#
interface GigabitEthernet0/2
ip address 10.0.0.15@ 255.255.255.0
ip access-group Block__Host_A out
!
interface GigabitEthernet0/3
ip address 172.16.0.15@ 255.255.255.080
ip access-group 1 out
E Lab Assignment — Implement Standard and Extended ACLs (Tasks 1-3)
— Jf | Configure and verify standard and extended ACLs.
—
Perform the instructions in lab document NET-11-L1.

## Powiązane laboratoria

- [NET-11-LS1](../labs/net-11-ls1.md)


## Uzupełnienia z notatek Riseup / zajęć

<details>
<summary>Pokaż notatki prowadzącego, dodatkowe komendy i linki powiązane z tym tematem</summary>

R2(config)#ip access-list standard 1
R2(config-std-nacl)#exit
R2(config)#access-list 1 deny 172.16.2.0 0.0.0.255

R2(config)#access-list 1 permit any
R2(config)#interface gigabitEthernet 0/0
R2(config-if)#ip access-group 1 out
R2(config-if)#exit
R1>enable
R1#configure terminal
R1(config)#ip access-list standard BLOCK_HOST
R1(config-std-nacl)#deny host 192.168.2.1
R1(config-std-nacl)#permit any
R1(config-std-nacl)#exit

---

R2(config)#ip access-list extended 100
R2(config-ext-nacl)#exit
R2(config)#access-list 100 deny ip host 172.16.2.1 host 192.168.1.2
R2(config)#access-list 100 permit ip any any
R2(config)#interface gigabitEthernet 0/1
R2(config-if)#ip access-group 100 in
R2(config-if)#exit
R2(config)#do show access-list
R1(config)#ip access-list extended BLOCK_HTTP

</details>

## Powiązane tematy

- [ACL overview](acl-overview.md)
- [Extended ACL](extended-acl.md)

## Źródła w zestawie

- `Computer Networking Textbook.pdf` — strony 191–194.
- `Computer Networking.pdf` — prezentacja kursowa; odpowiadający rozdział zachowany w `_source-archive/02-Course-Slides.md`.
- `Padriseup Computer Networking.pdf` — uzupełnienia i materiały dodatkowe, jeśli występowały dla tego tematu.
