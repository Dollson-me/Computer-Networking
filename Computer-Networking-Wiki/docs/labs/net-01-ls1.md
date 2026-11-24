# NET-01-LS1 — Local Network Configuration

[← Wszystkie laboratoria](index.md)

> **Typ:** laboratorium z rozwiązaniem. Zachowano wszystkie kroki, pytania, odpowiedzi, komendy i wartości z materiału źródłowego; usunięto jedynie techniczne nagłówki stron OCR.

## Powiązana teoria

- [Network types and devices](../01-foundations/network-types-devices.md)
- [Network protocols and Windows commands](../01-foundations/network-protocols-commands.md)

## Pełny przebieg laboratorium

> Zakres źródłowy: strony 1–14.

Computer Networking
Lab Assignment Introduction
& Solution to Networks
eo Vat NET-01-LS1
“alk F U | Local Network
Configuration
Copyright © 1996-2020 HackerU Ltd.
All Rights Reserved.

Note: Solutions for the instructor appear in a green colored box.
G Lab Objective
Learn about and practice using CLI networking commands in Windows.
* Lab Mission
Configure a local network using CMD-based commands.
ea .
© Lab Duration
15-30 minutes
fe Requirements
e Familiarity with the Windows command line.
e Familiarity with the nslookup tool.
Lt

[ra] Resources
¢ Environment & Tools

Windows 7, 8, or 10

Internet connection

Lab Task 1: Windows 10 Virtual Machine Installation
If you do not have a Windows 10 VM installed, set up a new machine.
You can follow the instructions in the Windows 10 Installation Guide located in the
Installation Guide module in your Canvas course.

Lab Task 2: Local Network Configuration
In this task, you will use commands to view and document the local network
configuration of a Windows machine.
1 Open CMD on the local machine.

Press Win Key + R and type CMD.
2 Run the ipconfig command to display local PC network settings.

Type ipconfig and press Enter.

Connection-specific DNS Suffix . :

Ethernet adapter Bluetooth Network Connection:

3 According to the ipconfig command output, how many network cards are there?
Why do some PCs display information regarding more than one network card?
The ipconfig command displays information regarding all interfaces on the local
machine. For example, laptops usually have wired, wireless, and Bluetooth interfaces
installed.
4 Document the information in Notepad or a personal notebook.
Copy the details marked in red in Step 2 above.

5 The command in Step 2 above does not show the physical and DNS address. Issue
the same command with the appropriate option to display the network settings in
more detail.

6 Which Help option displays all ipconfig option combinations and their purposes?

7 Which CMD command displays the physical address?

8 Run the cls command to clear the screen.

Page5

Lab Task 3: Test Connectivity

In this task, we will verify connectivity to an internet based IP, and document

connection metrics such as latency and path.

1. Using the Ping command, verify connectivity between the local PC and another PC
in the same network (for example, the PC of an adjacent student or another device
on your network).

Ask another student for his/her IP address and ping it, or ping your default gateway.

2 Document the following details located in the ping statistics:

e Packets sent, received, and lost.
e Average round trip time.
Document only the details marked in red below.
C:\Windows \system32>ping 1@.21.6.3
Pinging 10.21.0.3 with 32 bytes of data:
Reply from 16.21.@.3: bytes=32 time-16ms TTL=128
Reply from 10.21.6.3: bytes=32 time=4ms TTL=128
Reply from 10.21.6.3: bytes=32 time=5ms TTL=128
Reply from 16.21.@.3: bytes=32 time=31ms TITL=128
\Approximate round trip times in milli-seconds:
Minimum = 4ms, Maximum = 31ms, Average = 12ms
i
3 Runtracert for the same target as in Step 1 above.
Run the tracert command for the IP address from Step 1 above.
C:\Windows\system32>tracert 10.21.6.3
Tracing route to 10.21.@.3 over a maximum of 3@ hops
2 4ms 4ms 7 ms 10.21.0.3
Trace complete.

4 What is a Hop?
A router on the way to a packet's destination, from one network to another.
5 Document the number of hops.
C:\Windows \system32>tracert 168.21.6.3
Tracing route to 16.21.6.3 over a maximum of 38 hops
6 Use the ping command again to test connectivity to an external source (such as a
website or Google DNS public server, 8.8.8.8).
Ping an external source, such as a URL or public address (www.facebook.com, 8.8.8.8).
C: \Windows\system32>ping 8.8.8.8
Pinging 8.8.8.8 with 32 bytes of data:
Reply from 8.8.8.8: bytes=32 time=57ms TTL=55
Reply from 8.8.8.8: bytes=32 time=59ms TTL=55
Reply from 8.8.8.8: bytes=32 time=60ms TTL=55
Reply from 8.8.8.8: bytes=32 time=59ms TTL=55
Packets: Sent = 4, Received = 4, Lost = @ (0% loss),
Approximate round trip times in milli-seconds:
Minimum = 57ms, Maximum = 60ms, Average = 5S8ms

7 Document the following details in the ping statistics:
e Packets sent, received, and lost.
e Average round trip time (latency as ms).
Document only the details marked in red below.
Reply from 8.8.8.8: bytes=32 time=S9ms TTL=55
Ping statistics for 8.8.8.8:
iWpproximate round trip times in milli-seconds:
Minimum S7ms, Maximum 6@ms, Average 5Bms
8 Run tracert for the same target as in Step 7 above.
Run tracert for the IP address in Step 7.
9 Document the number of hops.
1 6 ms 5 ms 8 ms 10.21.8.100
2 S ms 4 ms 38 ms b2q-252-97 .red.bezeqint.net [212.179.252.97]
3 6G ms 6 ms 6 ms bzq-179-16-121.cust.bezegint.net [212.179.16.121]
6 60 ms 6@ m 59 ms 108.170.252.65
i 62 ms 62 ms 62 ms 216.239.56.149

10 Compare the findings. Why are the round-trip times and hop count results in
Steps 1-4 less than those in Steps 7-10?
The adjacent student's PC is in the same network, so no router is needed. The external
source is in a different network, which means the packet must be forwarded through
several routers.

Lab Task 4: Domain Names and IPs
In this task, you will demonstrate knowledge of the nslookup command, document
your machine’s DNS servers, and find IP addresses of URLs.
1 Using the nslookup command, discover which DNS server is configured on the local
machine.
Type nslookup to enter resolve mode.
C:\Windows \system32>ns lookup
2 Using nslookup, what is the public IP address of www.cisco.com?
Default Server: dns.google
Addresses: 2a02:26f0:c00:584: :b33
www. cisco. com.akadns .net
wewds .cisco.com.edgekey net

3 ADNS record can also work in reverse order. Which service or organization uses IP
address 185.60.216.35?
> 185.66.216.35
Server: dns.google
Name: edge-star-mini-shv-@1-frx5,. facebook. com
Address: 185.60.216.35
4 Press Ctrl+c to exit nslookup mode, or type exit, and close CMD.

Lab Task 5: Domain CLI Vs GUI
In this task, you will configure your network interface using only the CLI.
There are two universal ways to communicate with a PC: via graphic interface (GUI), or
via a Command Line Interface (CLI).
The netsh command is run via the CLI, and is used to configure all network settings.
1 Open CMD as administrator.
Search for cmd, and right-click “Run as Administrator”.
w
=F
o Ea ~
& PD emder —
® ed commands
P mdb
P emda vs
2 amd
2 and nyse 1
==
a
o Ee 2D Web
«a Eo = @ a =
2 Display the local PC network configuration using netsh interface ip show config .
Command: netsh interface ip show config
Note: Interface names may be different.

3 Configure the following addresses statically on the wired or wireless interface:
e |Pv4 192.168.0.5
e Subnet Mask: 255.255.255.0
e Default Gateway: 192.168.0.1
Use the following command:
netsh interface ip set address "Ethernet" static 192.168.10.5 255.255.255.0
192.168.0.1
Run:
netsh interface ip set address "Ethernet" static 192.168.10.5 255.255.255.0
192.168.0.1
Make sure to substitute “Local Area Connection*1” with the name of your interface (for
example “Ethernet”).
4 Use the command in Step 2 above to verify the new configuration.
Run: netsh interface ip show config
5 Which network protocol is responsible for allocating IP addresses and network
configurations dynamically to devices on the network?
DHCP
6 Revert the changes by enabling DHCP on the interface with the command:
netsh interface ip set address "Ethernet" dhcp
Run: netsh interface ip set address "Ethernet" dhcp
7 Disable the interface, with the following command:
netsh interface set interface "Ethernet" admin=DISABLED
Run: netsh interface set interface "Ethernet" admin=DISABLED
8 Enable the interface, with the following command:
netsh interface set interface "Ethernet" admin=ENABLE
Run: netsh interface set interface "Ethernet" admin=ENABLE

9 Ping 8.8.8.8 to verify connectivity.
Run: Ping 8.8.8.8
Verify that the command was successful.
