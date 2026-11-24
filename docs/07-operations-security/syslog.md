# Syslog

[← Indeks wiki](../index.md)

> **Źródło główne:** Computer Networking Textbook.pdf, s. 179–184. Treść została uporządkowana tematycznie; pełny ekstrakt źródłowy znajduje się w `_source-archive/`.


## Materiał kanoniczny

Syslog is a standard for logging messages. Each device records actions and events that
occur, similar to a private diary. Among other tasks, network administrators need to
monitor the network to ensure smooth, errorless functionality. Monitoring the network
improves troubleshooting capability and helps identify issues such as device health and
network load.
Why are logs useful?
System notification logging increases a network administrator's awareness of hardware
or software malfunctions, service status, and security accountability. In some cases, logs
can be used to predict component failures. Log analysis can help administrators
troubleshoot the system, and can be useful to information security experts when
investigating security breaches.
Syslog messages can be stored locally on the device, or on a Syslog server in the
network.
Device Logs
The following points should be considered when working wth device logs:
e Log storage takes up space, and can, in some cases, degrade system performance.
e Log message count is limited due to buffer size.
e Collecting logs from separate devices can take a long time.
e RAM is erased upon device power off.
Syslog Server
A Syslog Server is a computer that runs Syslog software. The Syslog software
concentrates logs from all devices (PC, router, etc.) on the network into one centralized
location, which makes management and backup easier. It also offers a convenient user
interface. This way of working is more efficient than storing logs in RAM.
Many free and enterprise versions of Syslog exist, such as the Kiwi Syslog Viewer.

Storage Methods
Logging Buffer - A Logging Buffer is a predetermined storage space allocated on RAM
for Syslog messages.
Console Line - Console Line is a method of viewing messages locally via the console
window.
Terminal Line - Terminal Line is a method of viewing messages via a CLI program (such
as Putty).
Syslog Server - If a Syslog Server is configured on the device, the device will send all
Syslog messages to the server over the UDP 514 port.
Messages
Status - Network devices generate Syslog status messages in response to events in the
network (such as when the status of a device changes, login attempts, etc.).
Fields - Fields in Syslog messages include:

Severity — The urgency of the message.

Facility — Specifies in which component of the device the message originated.
Severity & Facility
Syslog messages include several pieces of information, of which the most important
are:
Message Severity - The urgency of the log message is represented by its severity level,
which is a number from 0 to 7. Level 0 indicates emergencies, and 7 indicates system
debugging. The values also represent critical malfunctions and system warnings.
Message Facility - The facility parameter indicates the source that generated the
message, which, for example, can be a network card or routing protocol. The facility can
be a hardware component, protocol, or system service.

Message Severity
The severity of a Syslog message is represented by a number called the Syslog Security
Level. The lower the number, the higher the severity.
Message Type Severity Explanation
Emergency Level 0 System unusable
Alert Level 1 Immediate action needed
Critical Level 2 Critical condition
Error Level 3 Error condition
Warning Level 4 Warning condition
Notification Level 5 Normal, but significant
Information Level 6 Informative message
Messages related to the
Debug Level 7 es
debugging process
Log Message Format
7 Log Event 7 7 " i t
Dec 28 19:01! %LINK} -5- | CHANGED: | Interface GigabitEthernet@/1, changed state to up!
' 1 fo2 tsi oa H 5 H
</>
1. Timestamp: Records the time and date of the log (this service is disabled by default,
and should be enabled once to update the system’s time).
2. Facility: The category of the source that created the log message. In the example
above, the link represents the state of the router's hardware ports.
3. Severity: The severity level, which in the example above, indicates that it is a
notification message.
4. Mnemonic: A device-specific code that identifies the log message.
5. Text Description: The log/event description and other details.
Messages in the console consist of the following:
*Dec 28 19:01 %LINK-5-CHANGED: Interface GigabitEthernet@/1, changed state to up

Syslog Configuration Commands
Command Meaning
Logging host [IP address] Sets the log server.
| Determines what log severity levels to
Logging trap
send to the server.
Service timestamps lo
; Ps (08 Sends alerts with time included.
datetime msec
| Shows system messages on the screen
Terminal monitor ;
of a remote connection (Telnet, SSH).
Shows system messages on the screen
Logging console of the console connection (enabled by
default).
Saves system messages to RAM
Login buffered ” B
(enabled by default).

Syslog Config Example
The logging host command sets the destination IP of the Syslog server, to which all logs
are sent. The logging trap command sends all severity log levels to the server (levels 7
and above). The remaining commands in the example below are used to add time
records.
R1(config)#logging host 172.16.0.250
R1(config)#logging trap debugging
R1(config)#logging userinfo
R1(config)#service timestamps log datetime msec
R1(config)#do show logging
<Output Omitted>
ESM: @ messages dropped
» 9 message lines logged
(udp port 514, audit disabled,
authentication disabled, encryption disabled, link up),
2 message lines logged,
@ message lines rate-limited,
@ message lines dropped-by-MD,
xml disabled, sequence number disabled
£iltaning dinahtad

Server Configuration
To simulate Syslog in your packet tracer environment, first create the server.
Open the server configuration window, search for Syslog, and make sure that it is
turned on.
The IP address will be used in the host configuration statement.
Physical Config _Senmices_ Desktop Programming Attributes.
SERVICES svsea
Sune Syslog
DHCP ne
ST Senice @on Oo
Pqer TTF Time Hoanane —
1 “ONS
fs canst %SYS-5-CONFIG_E Configur.
AAA
: ae s eee or S6LINK-5-CHANGED: Interfac
= ae 3° 1229821 SULINEPROTO 5. UPOOWE L
at tl IoT 4)- 192.168.2.1 ‘%LINK-5-CHANGED: Interfac.
VM Management
Saas Pie 1eeB2 1 ‘%LINEPROTO-5-UPDOWN: L.
IsAk321
-
Server-PT
Syslog
Clear Log
C1 tep
Syslog Server Service Activation

## Powiązane laboratoria

- [NET-10-LS1](../labs/net-10-ls1.md)

## Powiązane tematy

- [Troubleshooting methodology](troubleshooting.md)
- [NTP](ntp.md)

## Źródła w zestawie

- `Computer Networking Textbook.pdf` — strony 179–184.
- `Computer Networking.pdf` — prezentacja kursowa; odpowiadający rozdział zachowany w `_source-archive/02-Course-Slides.md`.
- `Padriseup Computer Networking.pdf` — uzupełnienia i materiały dodatkowe, jeśli występowały dla tego tematu.
