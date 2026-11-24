# Remote access, VTY, SVI and SSH

[← Indeks wiki](../index.md)

> **Źródło główne:** Computer Networking Textbook.pdf, s. 86–92. Treść została uporządkowana tematycznie; pełny ekstrakt źródłowy znajduje się w `_source-archive/`.


## Materiał kanoniczny

Today, other than for initial configuration, most access to deployed switches is done
remotely.
Remote access allows administrators to manage and monitor their network devices
from anywhere in the network.
This is important since some switches may be located in physically inaccessible areas.
Telnet vs. SSH
Telnet and SSH are the two most widely used CLI-based remote access protocols.
Telnet - Telnet was developed many years ago to allow users to manage devices from
anywhere, via a simple and minimal configuration. However, using Telnet involves a
potential security risk because usernames and passwords are sent in plain text on TCP
port 23.
SSH - SSH is similar to Telnet, but with a significant difference: SSH encrypts all data
transferred between the user and end device. SSH uses RSA encryption, a robust and
reliable encryption type. It operates on TCP port 22.
SSH Encryption
Modern encryption relies heavily on the RSA algorithm since most methods use public
and private encryption keys.
The public and private encryption key method, also known as asymmetric cryptography,
uses two different, but mathematically linked keys.
The public key is shared with everyone, while the private key is only given to specific
persons.
RSA ensures implementation of the CIA triangle, and avoids authentication rejection.
Protocols like SSH and SSL/TLS use RSA to encrypt communication and digital
signatures.
Although RSA works through the computational difficulty of factoring large integers,
computational complexity grows exponentially every day, and larger and larger
numbers are required to maintain secure communication.

RSA is dependent on a powerful computational system. More complex keys require
more computation.
Recently, ECC (Elliptic Curve Cryptography) is becoming popular, since it can create
faster, smaller, and more efficient cryptographic keys.
Asymmetric Encryption
Asymmetric encryption is when two different keys are used to encrypt and decrypt
messages.
The keys are mathematically related in a way that messages encrypted with one key,
usually the public key, cannot be decrypted by it. The decryption can be done only using
the corresponding private key in the key pair.
This method is considered more complex and slower than symmetric encryption which
uses one key for both encryption and decryption.
Public key
a
of fo Decryption ap
ee SEE Sanaa!
[se] Encryption [ieee] Q cor
Private key
————— EEE
Data transfer
42222 noo ee een ---------
P Key publicly available —_
Encryption-Decryption Process

## Powiązane laboratoria

- [NET-04-LS2](../labs/net-04-ls2.md)


## Uzupełnienia z notatek Riseup / zajęć

<details>
<summary>Pokaż notatki prowadzącego, dodatkowe komendy i linki powiązane z tym tematem</summary>

Remote Access

Telnet-TCP/23
SSH-TCP/22
Przechwycenie protokołu SSH
https://www.cloudshark.org/captures/849d3c7f09d3
LAB SSH1

---

exit
wr
line vty 0 15
login local
transport input ssh
exit
interface vlan 1

ip add
ip address 10.0.0.150 255.255.255.0
no shutdown
exit
Generowanie klucza:
crypto key generate rsa
1024
S1#show ip ssh - pokaże, że ssh uruchomiono
https://beyond.hackampus.com/canvas/general/general-LLcAf-2021.12.12.10.09.23-Extra%2
0Files.rar
conf t

---

S1(config)#enable password c!sc0
S1(config)#ip ssh version 2
S1(config)#do show ip ssh

02.09.2023
https://www.cisco.com/c/en/us/support/docs/routers/7200-series-routers/12219-17.html

---

S1>enable
S1#conf t
S1(config)#interface vlan 1
S1(config-if)#ip address 192.168.0.4 255.255.255.0
S1(config-if)#no shutdown
S1(config-if)#exit
S1(config)#
S2>enable
S2#conf t
S2(config)#interface vlan 1
S2(config-if)#ip address 10.0.0.4 255.255.255.0
S2(config-if)#no shutdown
S2(config-if)#exit

</details>

## Powiązane tematy

- [Port security](port-security.md)
- [Initial Cisco device configuration](../03-cisco-ios/initial-device-configuration.md)

## Źródła w zestawie

- `Computer Networking Textbook.pdf` — strony 86–92.
- `Computer Networking.pdf` — prezentacja kursowa; odpowiadający rozdział zachowany w `_source-archive/02-Course-Slides.md`.
- `Padriseup Computer Networking.pdf` — uzupełnienia i materiały dodatkowe, jeśli występowały dla tego tematu.
