# Network address scheme design

[← Indeks wiki](../index.md)

> **Źródło główne:** Computer Networking Textbook.pdf, s. 122–123. Treść została uporządkowana tematycznie; pełny ekstrakt źródłowy znajduje się w `_source-archive/`.


## Materiał kanoniczny

Network Planning

A network needs to be well-designed. Addresses must not be assigned randomly!

Planning a network requires examination of how the organization is structured, and

how the subnets will be structured.

Planning addresses involves deciding how many hosts per subnet there will be, how

large each subnet will be, and how host addresses will be assigned.

Note: Knowing your address requirements will help determine the range of host

addresses.

Planning Considerations

Prevent Duplication In an inter-network structure, each host must have a unique
address. Planning and documentation prevent the creation of
duplicate addresses.

Access Control If addresses are randomly assigned, servers that provide
resources to internal and external hosts will not be able to
control access efficiently and effectively.

Monitor Network traffic is examined for source IP addresses generated or
received from packets. With proper planning, finding problematic
devices should be a simple process.

Assignable Address Devices

Clients Most networks use DHCP to dynamically assign addresses,
eliminating the need for network staff to do so, and preventing
entry errors. When the address scheme changes, the DHCP server
must be reconfigured.

Servers In most networks, servers must be made available to remote
users. The servers are assigned private internal addresses, and
the forwarding device will perform additional translations to
public addresses (NAT). Servers are typically configured with
static addresses.

Routers/Switches Routers and switches are assigned IP addresses. Switches can be
managed remotely via the cloud. Routers are assigned IP
addresses because they operate in Layer 3. Routers are typically
configured with static addresses.

Gateway A gateway is a packet-forwarding device, and is typically a firewall
or router. Each interface that serves as a gateway for hosts in the
network must be assigned an IP address.

## Powiązane laboratoria

- [NET-06-LS1](../labs/net-06-ls1.md)

## Powiązane tematy

- [Subnetting](subnetting.md)
- [VLSM](vlsm.md)
- [IPv4 static and default routing](static-routing-ipv4.md)

## Źródła w zestawie

- `Computer Networking Textbook.pdf` — strony 122–123.
- `Computer Networking.pdf` — prezentacja kursowa; odpowiadający rozdział zachowany w `_source-archive/02-Course-Slides.md`.
- `Padriseup Computer Networking.pdf` — uzupełnienia i materiały dodatkowe, jeśli występowały dla tego tematu.
