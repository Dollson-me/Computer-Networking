# VLSM

[← Indeks wiki](../index.md)

> **Źródło główne:** Computer Networking Textbook.pdf, s. 120–121. Treść została uporządkowana tematycznie; pełny ekstrakt źródłowy znajduje się w `_source-archive/`.


## Materiał kanoniczny

VLSM (Variable Length Subnet Mask) is a method by which a network is subnetted, and
the subnets are then subnetted further (when using only CIDR, they are not subnetted
further).
The process can be repeated several times to divide the subnets into various sizes, to
ensure that IP addresses are not wasted.
Formulas are applied to calculate the number of hosts and subnets.
Note: Knowing your address requirements will help determine the range of host
addresses.
VLSM Subnetting Example
As an example, we will start with the network address 10.0.0.0/8. This address is
subnetted into 2 additional networks.
The subnetting process (CIDR) created the networks 10.0.0.0/9 and 10.128.0.0/9.
After creating the networks, each was subnetted (VLSM) to create additional networks,
similar to using CIDR.
VLSM is useful when using CIDR provides too many unused addresses for one network.
Sa Ps
see Pe
a ae
- we
10.0.0.0 /9 10.128.0.0 /9
10.0.0.0/10 10.64.0.0/10 10.128.0.0/10 10.192.0.0 /10
10.0.0.0 /9 used to create 2 —_
11111111.11000000.000000.000000
10.0.0.0 /10 and 10.64.0.0 /10 subnets are created >

‘ Lab — Subnetting Practice
—=J/ | Answer questions based on material covered in the module, including the
= =| topics of how to subnet networks and assign IP addresses.
Perform the instructions in document Net-06-L1.

## Powiązane laboratoria

- [NET-06-LS1](../labs/net-06-ls1.md)

## Powiązane tematy

- [Subnetting](subnetting.md)
- [CIDR and prefix notation](cidr.md)
- [Network address scheme design](address-scheme-design.md)

## Źródła w zestawie

- `Computer Networking Textbook.pdf` — strony 120–121.
- `Computer Networking.pdf` — prezentacja kursowa; odpowiadający rozdział zachowany w `_source-archive/02-Course-Slides.md`.
- `Padriseup Computer Networking.pdf` — uzupełnienia i materiały dodatkowe, jeśli występowały dla tego tematu.
