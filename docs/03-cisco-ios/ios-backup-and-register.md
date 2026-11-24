# IOS backup, TFTP and configuration register

[← Indeks wiki](../index.md)

> **Źródło główne:** Computer Networking Textbook.pdf, s. 76–80. Treść została uporządkowana tematycznie; pełny ekstrakt źródłowy znajduje się w `_source-archive/`.


## Materiał kanoniczny

TFTP
TFTP (Trivial File Transfer Protocol) is a simple lock-step file transfer protocol that
allows clients to retrieve files from or transfer files to a remote host.
TFTP can also be used to remotely start a computer, back up network or router
configuration files, and upgrade a device’s IOS.
TFTP relies on UDP to transport data, and uses port 69.
Back Up Device Configuration
This process copies the running-configuration file to a remote TFTP server. This is very
useful for when a disaster occurs, and a quick restoration of settings is required.
Command:

copy running-config tftp
Example:
Backup using TFTP
Note: First save the configuration locally, using:

copy running-config startup-config
Step 1 — Copy the file to the server.
Step 2 — Enter the TFTP server IP address.
Step 3 — Select the name of the file saved on the server.
Backing up the IOS file is almost the same. You only need to replace the source location
of the file, meaning flash: instead of running-config.

Example:
Sl#copy running-config tftp:
Address or name of remote host []? 192.168.1.3
Destination filename [R1-confg]? R1-config-backup20.9
Writing running-config....!!
[OK - 1362 bytes]
10S Upgrade
Step 1—The command copy tftp: flash: is used to copy the new IOS file from a TFTP
server to the flash memory.
Step 2 - Upgrading the device can be performed after copying the new IOS to the
device, using the boot system command. This command tells the device which IOS file
to load upon the next startup.
Step 3 — The command copy running-config startup-config is used to save current
configuration to the startup configuration, and reload the device to enable the new IOS
to load.
Example:
Sl1#copy tftp: flash:
Address or name of remote host []? 192.168.1.3
Source filename []? c1901-imoversa;19.mz.SPA.152-4.M3.bin
Destination filename [c1901-imoversa;19.mz.SPA.152-4.M3.bin]?
Accessing tftp://192.168.1.3/ c1901-imoversa;19.mz.SPA.152-4.M3.bin...
Loading c1901-imoversa;19.mz.SPA.152-4.M3.bin from 192.168.1.3:
PEEPEPPPPP rb err repre rrr errr errr rrr errr err rere errr rrr errr errr rrr
[OK - 4670455 bytes]
S1# Configuration terminal
S1(config)#boot system flash®://c1901-imoversa;19.mz.SPA.152-4.M3.bin
S1(config)# exit
S1#copy running-config startup-config
Sl#reload

ROMmon
The purpose of the ROMmon (Read Only Memory MONitor) configuration register is to
change the router’s behavior in several ways:

© Determine how the router will boot.

e Apply options while booting (such as ignore configuration).

e Set the console speed and band rate for terminal emulation sessions.
Configure Register Value
In the Configuration terminal mode, we can change the register value, which will affect
the next boot process.
In the example below, the register value is changed to the default 0x2102, and the
configuration is saved in startup config, which will revert the settings to the factory
default.
Example:

Router(config)# config-register @x2102

Router(config)# end

Router# copy running-config startup-config

Destination filename [startup-config]?

Building configuration

[OK]

Router# Reload

ROMmon Register Value
The default configuration register is Ox2102, which can be verified using the show
version command.
Use the configreg command to change the register value and the router’s behavior.
Common Settings
Register Value Device Behavior
- Ignores break key
0x102 - 9600 console baud rate (maximum transfer rate of the
console port in bits per second, in this case 9600 bits per
second)
0x1202 - 1200 baud rate
- Boots into bootstrap
- Ignores break key
0x2101
- Boots into ROM if initial boot fails
- 9600 console baud rate
- Default register value
- Boots into ROM if initial boot fails
0x2102
- 9600 console baud rate default value for most
platforms

## Powiązane laboratoria

- [NET-03-LS3](../labs/net-03-ls3.md)


## Uzupełnienia z notatek Riseup / zajęć

<details>
<summary>Pokaż notatki prowadzącego, dodatkowe komendy i linki powiązane z tym tematem</summary>

exit
show running-config
copy running-config startup-config
show interfaces FastEthernet 0/1
show mac-address-table
zadanie domowe:

---

R1#show running-config

R1#copy running-config startup-config
Destination filename [startup-config]? --> [ENTER klawisz]
R1#conf t
R1(config)#interface gigabitEthernet 0/0

---

R1(config-router)#exit
R1(config)#exit
R1#copy running-config startup-config
Destination filename [startup-config]?
<KLAWISZ ENTER
Building configuration...

---

R2(config-router)#exit
R2(config)#exit
R2#copy running-config startup-config
Destination filename [startup-config]?
<KLAWISZ ENTER
Building configuration...

---

R3(config-router)#exit
R3(config)#exit
R3#copy running-config startup-config
Destination filename [startup-config]?
<KLAWISZ ENTER
Building configuration...

---

S2(config-if)#switchport trunk native vlan 30
S2(config-if)#exit
S1#copy running-config startup-config
S2#copy running-config startup-config
do copy running-config startup-config
R1>enable
R1#conf t
R1(config)#interface gigabitEthernet 0/0

</details>

## Powiązane tematy

- [Cisco IOS and CLI](cisco-ios.md)
- [Initial Cisco device configuration](initial-device-configuration.md)

## Źródła w zestawie

- `Computer Networking Textbook.pdf` — strony 76–80.
- `Computer Networking.pdf` — prezentacja kursowa; odpowiadający rozdział zachowany w `_source-archive/02-Course-Slides.md`.
- `Padriseup Computer Networking.pdf` — uzupełnienia i materiały dodatkowe, jeśli występowały dla tego tematu.
