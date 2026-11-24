# Initial Cisco device configuration

[← Indeks wiki](../index.md)

> **Źródło główne:** Computer Networking Textbook.pdf, s. 72–75. Treść została uporządkowana tematycznie; pełny ekstrakt źródłowy znajduje się w `_source-archive/`.


## Materiał kanoniczny

Device Name
This command sets the local network device name. For example, S-Floor1.
Command:
hostname <device name>
Example:
Switch(config)#hostname S1-Floor1
S1-Floor1(config)#
Create User Account
Creates a Local User Account on the device.
Command:
username <user-name> password <password>
Example:
Switch(config)#username Admin password p@nd@
Switch(config)#username Peter password Spiderm@n

Secure Privileged Mode
Enables password authentication when accessing the Privileged EXEC mode.
Command:
enable password <password>
Example:
Switch(config)#enable password c!sc@
Security Message
Displays a security message each time a user logs in to the system.
Command:
banner motd #security-massage#
Example:
Switch(config)#banner motd #Access to this device is for
authorized personnel only!#
Encrypt Passwords
Configured passwords appear in plain text in the configuration file.
The command encrypts all plain text passwords, using the Cisco Type 7 method.
Command:
service password-encryption
Example:
Switch(config)#service password-encryption

Save Device Configuration
Copies the device configuration from the RAM to the NVRAM (non-volatile memory).
If the configuration isn’t saved to the NVRAM, all of the configurations that were
performed will be lost.
Command:
copy running-config startup-config
Example:
Secure Console Access
Two steps are performed to enable local credential (username & password)
authentication on the console port.
1. Enter the Console port config mode (Line mode).
2. Enter the local login and exit.
Note: Besides the local login command, there is a login command that enables only
password checking.
Command:
line console 0 & login local
Example:
Switch(config-line)#login local
Switch(config-line)#exit

Verify Configuration
All configuration changes are immediately saved in the running-config file.
To display them, run the show running-config or show run command.
Note: The example below is a brief glimpse of the actual file.
Example:
$1-Floorl#show running-config
Building configuration...
Current configuration : 1234 bytes
!
version 12.2
service password-encryption
!
hostname S1-Floor1
!
enable password 7 9822@D5D@A49
!
username Admin privilege 1 password 7 @8316C4@@D39
!
banner motd “CAccess to this device is for authorized personnel only!
!
line con @
login local
b Lab — Initial Cisco Device Configuration
—J | Learn to connect to and access the device IOS using the out-of-band
=== =| management method.
Understand how to work in the different Cisco IOS modes.
Understand and practice Cisco IOS commands used to configure a network
device for the first time, focusing on switch settings.
Perform the instructions in lab document Net-03-L1.

## Powiązane laboratoria

- [NET-03-LS2](../labs/net-03-ls2.md)


## Uzupełnienia z notatek Riseup / zajęć

<details>
<summary>Pokaż notatki prowadzącego, dodatkowe komendy i linki powiązane z tym tematem</summary>

racer_821_Windows_64bit.exe
configure terminal
hostname S1-Floor1
username Admin password p@nd@
show running-config
conf t
service password-encryption
exit
show running-config
copy running-config startup-config

---

https://www.cloudshark.org/captures/849d3c7f09d3
LAB SSH1
hostname S1
username Admin password p@nd@
enable password c!sc0
service password-encryption
banner motd #Authorized Access only. Hacking is illegal, log out#
ip domain-name CyberPro.com
exit
wr

---

Switch>enable
Switch#conf t
Switch(config)#hostname S1
S1(config)#username Admin password p@nd@
S1(config)#enable password c!sc0
S1(config)#ip ssh version 2
S1(config)#do show ip ssh

---

Router#conf t
Router(config)#hostname R1
R1(config)#username Admin password p@nd@
R1(config)#enable password c!sc0
R1(config)#service password-encryption
R1(config)#banner motd #Access to this device is for authorized personnel only!#
R1(config)#line console 0
R1(config-line)#login local
R1(config-line)#exit

---

R1(config)#do show ip interface brief
R1(config)#do show ip route
banner motd # Access to this device is for authorized personnel only!#
// troubleshooting nie pingujących routerów ,sprawdzamy:
R1(config)#do show ip interface brief
Interface

</details>

## Powiązane tematy

- [Cisco IOS and CLI](cisco-ios.md)
- [IOS backup, TFTP and configuration register](ios-backup-and-register.md)
- [Remote access, VTY, SVI and SSH](../04-switch-security/ssh-svi-vty.md)

## Źródła w zestawie

- `Computer Networking Textbook.pdf` — strony 72–75.
- `Computer Networking.pdf` — prezentacja kursowa; odpowiadający rozdział zachowany w `_source-archive/02-Course-Slides.md`.
- `Padriseup Computer Networking.pdf` — uzupełnienia i materiały dodatkowe, jeśli występowały dla tego tematu.
