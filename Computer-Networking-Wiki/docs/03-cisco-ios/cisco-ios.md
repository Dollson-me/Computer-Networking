# Cisco IOS and CLI

[← Indeks wiki](../index.md)

> **Źródło główne:** Computer Networking Textbook.pdf, s. 66–71. Treść została uporządkowana tematycznie; pełny ekstrakt źródłowy znajduje się w `_source-archive/`.


## Materiał kanoniczny

Every network device, such as a switch or a router, has an operating system that tells it
how to forward packets and execute network operations.
An operating system for a device is known as a Network Operating System (NOS).
NOS does not operate the same way as PC and server operating systems.
Internetworking Operation System (IOS) is a CLI-based system, and users interface with
it using Cisco text-based commands.
Most Cisco devices, regardless of their size or type, run the IOS, which is an advantage
due its singularity and familiarity.
While all devices come with a default IOS and feature set, it is possible to upgrade the
IOS version or feature set to obtain additional capabilities.
The versions of the IOS may be different, depending on the device hardware.
This course focuses on versions 12 and 15.
10S Interface Features
CLI - IOS uses a command line interface (CLI) to enable administrators and technicians
to interact with the system via special Cisco commands.
CLI is a means of interacting with programs by entering commands in a command line.
Using a CLI-based system has many advantages, such as minimum resource usage,
faster ability to operate in the system, and others.
Terminal Emulation - Many network devices are configured and managed using
Terminal Emulation software, such as PuTTY. TE programs enable the configuration of
local devices using a serial cable or a remote management protocol, such as SSH.

Terminal Software
PuTTY — PuTTY is a very versatile tool for remote access to another computer. It is often
used by people who want secure remote shell access to UNIX or Linux systems, though
that is only one of its many uses.
Category:
Leeeeeaee Specify the destination you want to connectio
| Keyboard Host Name (orlP address) Port
eee p2
es Raia, Connection type:
+ ‘Apaeatenee’ CRaw ©Telnet CRiogn @SSH COSerial
Behaviour Load, save or delete a stored session
rf apo ‘Saved Sessions
i §-Colours
Ei Gommecton [Detauesetngs da
Fs
Tenet Ean
Rlegin Delete
SSH
Serial
Close window on exit:
CAways (Never = @Only onclean exit
= Hep cam
Tera Term — Tera Term is an open-source, free, software-based terminal emulator
(communication) program. It emulates different types of computer terminals, from DEC
VT100 to DEC VT382, and supports telnet, SSH 1 and 2, and serial port connections.
SecureCRT — SecureCRT is a commercial SSH and Telnet client and terminal emulator by
VanDyke Software. Originally a Windows product, VanDyke recently added Mac OS X
and Linux versions.
Access Methods
Out-of-Band - This method uses a dedicated management console cable that must be
physically connected to the device. Initial configuration is usually done using this
method.
In-Band - This method uses management protocols, such as SSH or Telnet, which access
the device remotely over the network.

Qut-of-Band Management
Out-of-Band management requires two main items:
© PC with terminal software
¢ Console cable
Terminal - A network device is like a PC, but without a mouse, keyboard, or screen. PC
with a terminal provides a way to input commands and view output from the device.
Console Cable - A console cable or management cable is like a bridge between the PC
and the device. Almost every device has a designated console cable for this purpose.
Older cables use an RS232 connector, while modern ones use USB.
10S Modes
IOS can operate in one of three work modes, each with different capabilities and
permissions. For example, one mode may have a lower level of privileges compared
with another mode.
The division of modes is meant to separate the management levels and increase the
efficiency of network device security and configuration.
Cisco OS modes have a hierarchical structure and are similar among switches and
routers.
User EXEC Mode
This mode has low-level capabilities but is useful for basic operations. It has a limited
amount of monitoring commands, but does not allow any device configuration changes.
Privilege EXEC Mode
This mode has a large number of monitoring commands and device configuration
viewing commands (Show commands). It also enables file management operations,
such as device configuration backup, and IOS upgrade.

Global Configuration Mode
Global configuration is the only mode that allows administrators to change device
configuration. This mode is only accessible from the Privilege EXEC mode.
Mode Navigation
Navigating the system and understanding the differences among the modes is
important when working in the system.
The default display name of a device appears before the prompt. In the example on
below, the name is Switch.
The enable command moves the user from User mode to Privilege mode.
The configure terminal command moves the user from User mode to Global
configuration mode.
The exit command takes the user one mode back.
Example:

Switch>enable

Switch#configure terminal

Enter configuration commands, one per line. End with CNTL/Z.

Switch(config)#exit

Switch#exit

Switch>
10S Error Messages
Incomplete Command - The command is correct, but not complete.
Ambiguous Command - Not enough characters were entered for the command to be
recognized. Or, more than one command exists with the same name.
Invalid Input - The command was entered incorrectly (i.e. typo) or inserted in the
wrong mode.

Example:

Switch>di

% Ambiguous command: "di"

Switch#show

%Incomplete Command.

Switch(config)#hostnme S1

A

% Invalid input detected at '*' marker.
Hotkeys and Shortcuts
TAB - Completes a partial entry.
CTRL + D - Erases the character at the cursor.
CTRL + K - Erases all characters from the cursor to the end of the command line.
ESC + D - Erases all characters from the cursor to the end of the word.
CTRL + Shift + 6 - Break sequence used to abort DNS lookups, traceroutes, pings, etc.
CTRL + W - Erases the word to the left of the cursor.
CTRL + P - Recalls a command from the history buffer.
CTRL + Z - Ends Configuration mode and returns to Privileged EXEC mode.
Cisco Device Components
RAM - Volatile memory that stores the system configuration (running-config) and
tables (such as the MAC table).
ROM — Non-volatile memory responsible for the POST (Power-On Self-Test) process and
bootstrap, which is the initial program that is responsible for booting the IOS.
Flash — Non-volatile memory that stores the operating system itself (IOS).
NVRAM — Non-volatile memory that stores the startup config file.

Device Boot Process
1 - POST (Power-On Self-Test) and bootstrap program load — This part of the sequence
checks the CPU, RAM, and NVRAM. When done, the device copies the bootstrap
program from the ROM to the RAM.
2 - Load IOS — After copying the bootstrap program from the ROM to the RAM, the IOS
(which is still stored in flash memory) is copied to the RAM for execution.
3 - Load Configuration — The bootstrap program now copies the startup configuration
file from the NVRAM to the RAM.

## Powiązane laboratoria

- [NET-03-LS2](../labs/net-03-ls2.md)


## Uzupełnienia z notatek Riseup / zajęć

<details>
<summary>Pokaż notatki prowadzącego, dodatkowe komendy i linki powiązane z tym tematem</summary>

https://wiki.wireshark.org/SampleCaptures
https://wiki.wireshark.org/uploads/moin_import/attachments/SampleCaptures/dhcp.pcap
#Podstawowe komendy CISCO (IOS)
https://rioco.pl/komendy/komendy-ciscoios/
odświeżenie interfejsu
Ctrl-R - refresh
automatyczne odświeżanie interfejsu
logging synchronous
https://wiki.wireshark.org/uploads/moin_import/attachments/SampleCaptures/dns-icmp.pca
png.gz
https://ia601604.us.archive.org/20/items/cisco-packet-tracer-821-ubuntu-64bit/CiscoPacketT
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
show interfaces FastEthernet 0/1
show mac-address-table

---

S1#show port-security address
S1#show port-security interface fastEthernet 0/4
S1#show running-config
interface FastEthernet0/3
switchport mode access
switchport port-security

---

R1(config-line)#exit
R1(config)#exit
R1#show running-config

R1#copy running-config startup-config
Destination filename [startup-config]? --> [ENTER klawisz]

---

R2(config-if)#exit
R1>enable
R1#configure terminal
R1(config)#ip access-list standard BLOCK_HOST
R1(config-std-nacl)#deny host 192.168.2.1
R1(config-std-nacl)#permit any

</details>

## Powiązane tematy

- [Initial Cisco device configuration](initial-device-configuration.md)
- [IOS backup, TFTP and configuration register](ios-backup-and-register.md)
- [Remote access, VTY, SVI and SSH](../04-switch-security/ssh-svi-vty.md)

## Źródła w zestawie

- `Computer Networking Textbook.pdf` — strony 66–71.
- `Computer Networking.pdf` — prezentacja kursowa; odpowiadający rozdział zachowany w `_source-archive/02-Course-Slides.md`.
- `Padriseup Computer Networking.pdf` — uzupełnienia i materiały dodatkowe, jeśli występowały dla tego tematu.
