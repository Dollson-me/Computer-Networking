# NTP

[← Indeks wiki](../index.md)

> **Źródło główne:** Computer Networking Textbook.pdf, s. 185–187. Treść została uporządkowana tematycznie; pełny ekstrakt źródłowy znajduje się w `_source-archive/`.


## Materiał kanoniczny

NTP (Network Time Protocol) is responsible for the synchronization of all clocks in
devices on the network.
NTP is a client-server protocol. All clients must be configured with the NTP server's IP
address, so that they will all have the same date and time.
Cisco routers and switches can have the date and time set in one of following ways:
Manual configuration — This method requires manual setting of the time and date on
each device on the network.
It is not recommended to work this way for various reasons, among which is the lack of
scalability for large networks. (Setting the clock in every device will waste valuable
time.)
Collective NTP configuration — This method requires an available and configured NTP
server. Only the server's IP address needs to be set on network devices.
This ensures that all devices on the network will be set to the most accurate time and
date automatically.
Cisco routers can be configured to act as NTP servers. End devices on the network are
assigned the NTP server's IP address, and sync their clocks according to the NTP.
Since the entire network depends on the NTP server, it is very important to ensure that
the NTP clock is as accurate as possible.
How NTP Operates
Cisco routers and switches (and many other devices around the world) use NTP to
determine the date and time.
Accurate timestamps are extremely important for troubleshooting, managing, and
securing networks.
NTP operates with UDP, on port 123, and is defined in RFC 1305.

Stratum Model - Stratum levels define the distance from high-precision reference clocks
which begin with stratum 0, to devices connected hierarchically. Servers linked to the
reference clock are Stratum 1, devices that receive the time from the servers are
Stratum 2, and so on. To avoid delays, a maximum of 15 levels are allowed.
Services - Accurate time settings are crucial for many protocols and device functions.
For example, DHCP leases and Syslog events are time-sensitive services. Timestamps
are extremely important for troubleshooting, management, and network security.
Local Clock Configuration
Configuring a clock on the router locally, without using an NTP server.
Command:
Router#clock set hh:mm:ss Day<1-31> Month<January-December> Year<1993-2035>
Example:
Router>enable
Router#clock set 09:21:14 16 January 2019
Setting the clock manually has two drawbacks: a device can become out of sync if it is
shut down, and setting each and every device clock can waste valuable time.
Server Configuration
Configuring a Cisco device to sync its clock with an external NTP server.
Command:
Router(config)#ntp server <ip_address>
Example:
Router>enable
Router#configure terminal
Router(config)#ntp server 172.30.226.100

When configuring a device as an NTP server, the number after "master" in the
command (optional) represents how many hops the NTP server is from an accurate
time source. Value (stratum) n servers are n hops away from an accurate time source
(such as a radio or atomic clock). The default is 8.
Command:
Router(config)#ntp master <1-15>

Example:

Router>enable

Router#configure terminal

Router(config)#ntp master
Logging Alerts with Time
Logging alerts with time included.
Command:

Router(config)#service timestamps log datatime msec

Example:

Router>enable

Router#configure terminal

Router(config)#service timestamps log datetime msec

é Lab Assignment — Configure NTP and Syslog
—/f | Answer questions based on material covered in the lesson, and understand
= | how to configure NTP and Syslog servers.
Perform the instructions in lab document NET-10-L1.

## Powiązane laboratoria

- [NET-10-LS1](../labs/net-10-ls1.md)

## Powiązane tematy

- [Syslog](syslog.md)
- [Troubleshooting methodology](troubleshooting.md)

## Źródła w zestawie

- `Computer Networking Textbook.pdf` — strony 185–187.
- `Computer Networking.pdf` — prezentacja kursowa; odpowiadający rozdział zachowany w `_source-archive/02-Course-Slides.md`.
- `Padriseup Computer Networking.pdf` — uzupełnienia i materiały dodatkowe, jeśli występowały dla tego tematu.
