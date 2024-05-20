# Native VLAN VLAN 1:

----------

1. Default VLAN: **All switch ports are assigned to VLAN 1 by default** when the switch is first set up. This means that without any additional configuration, all ports can communicate with each other as they are on the same network.

2. Management VLAN: **VLAN 1 is typically used as the management VLAN**. This VLAN is used for remote management of the switch via protocols such as Telnet, SSH, SNMP, or HTTP/HTTPS.

3. Native VLAN for Trunks: **On trunk links, which are ports set to carry traffic for multiple VLANs, VLAN 1 is often used as the native VLAN.** This means that if an Ethernet frame does not have a VLAN tag when it reaches a trunk port, it is assumed to belong to VLAN 1.

4. Control Plane Traffic: **VLAN 1 is also used for various types of control plane traffic, such as Cisco Discovery Protocol (CDP), VLAN Trunking Protocol (VTP), and Spanning Tree Protocol (STP).**

5. Untagged Traffic: The native VLAN serves as the default VLAN for all untagged traffic on a trunk port.

**To configure the native VLAN on a Cisco switch trunk port, you would use the following interface configuration command:**

```shell
Switch(config-if)# switchport trunk native vlan <VLAN-ID>
```

Here `<VLAN-ID>` is the VLAN number you want to assign as the native VLAN for the trunk port.

# Loopback Address:

----------

- **IPv4:** The default localhost address for IPv4 is **`127.0.0.1`**. **The entire range `127.0.0.0` to `127.255.255.255` is reserved for loopback purposes**, meaning that any address within this block will loop back to the local machine. However, `127.0.0.1` is the most commonly used address for testing purposes.

- **IPv6:** The default localhost address for IPv6 is **`::1`**. This is the short notation for the loopback address, which is actually **`0000:0000:0000:0000:0000:0000:0000:0001`**. In IPv6, the `::` notation is used to compress the zeros in the address.

In IPv4, any IP address in the range of 127.0.0.1 to 127.255.255.255 can be assigned to a loopback interface on a Cisco device, but in practice, most administrators will choose an address from the assignable range of their network, something that doesn't conflict with other IP addresses.

For example, here's how you would configure a loopback interface with an IPv4 address on a Cisco router:

```shell
Router(config)# interface loopback 0
Router(config-if)# ip address 192.168.1.1 255.255.255.0
Router(config-if)# no shutdown
```

In this example, `loopback 0` is the logical name of the loopback interface, `192.168.1.1` is the IP address assigned, and `255.255.255.0` is the subnet mask. The `no shutdown` command is used to ensure that the interface is active, although loopback interfaces are not actually shut down like physical interfaces.

# Multicast Address:

----------
- **224.0.0.0 to 224.0.0.255**: Reserved for **local network control and maintenance multicast traffic**. These addresses are not forwarded by routers and are meant for local segment (subnet) multicast traffic. For example, 224.0.0.1 is the all-hosts multicast group, which reaches all multicast-capable hosts on the local network segment.
- **224.0.1.0 to 238.255.255.255**: **Globally scoped addresses used for multicast applications and services that are reachable across the internet**.
- **239.0.0.0 to 239.255.255.255**: **Reserved for organization-local scope, used within an individual organization or a site and not intended to be routed across the internet**.

**IPv6 Multicast Addresses:**
The IPv6 multicast address range starts with the prefix FF00::/8. Similar to IPv4, certain addresses within this range are reserved for specific functions. For example:

- **FF02::1**: All nodes address, **which targets all devices on the local network segment.**
- **FF02::2**: All routers address, **which targets all routers on the local network segment.**

# Broadcast Address:

----------

**IPv4 Broadcast Addresses:**
**IPv4 supports broadcast addresses,** which are **used to send traffic to all hosts on a local network segment**. The **default IPv4 broadcast address is typically the last address in the subnet.** For example, if the subnet is **192.168.1.0/24 (with a subnet mask of 255.255.255.0), the broadcast address would be 192.168.1.255**. When a packet is sent to this address, it is delivered to all hosts in the subnet.

Broadcasting is a less efficient method of sending the same data to all hosts on a network because it can lead to unnecessary traffic and congestion. **Therefore, while IPv4 includes a broadcast mechanism, IPv6 does not.**

# Default Broadcast MAC Address:

----------

**The default broadcast MAC address, which is recognized by all networked devices, is `FF:FF:FF:FF:FF:FF`**. This address is used to send frames to all devices on the local network segment (broadcast domain) in an Ethernet network. When a device's network interface sees a frame with a destination MAC address of `FF:FF:FF:FF:FF:FF`, it knows that the frame is a broadcast and processes it accordingly.

**Broadcasts are typically used for network discovery protocols or for communication that needs to reach every device on the local network**. For instance, ARP (Address Resolution Protocol) requests are sent as broadcasts to resolve an IP address to its corresponding MAC address.

In Cisco devices, like other vendors' network equipment, the broadcast MAC address is not configurable—it is a universal constant in Ethernet networking and does not vary from one manufacturer to another. **It's important to note that layer 2 broadcasts are limited to the local broadcast domain and are not routed across different subnets or VLANs**.

# IPv4 Class Ranges:

----------

**Class A:**
**- First bit is "0"**
- Address Range: 0.0.0.0 to 127.255.255.255
- Default Subnet Mask: 255.0.0.0 (or /8 prefix)
- Usage: Intended for very large networks, such as multinational corporations. The first 8 bits are used for the network portion, while the remaining 24 bits are for host addresses within that network. Notably, the range 0.0.0.0 to 0.255.255.255 is reserved for special purposes, and 127.0.0.0 to 127.255.255.255 is reserved for loopback addresses.

**Class B:**
**- First two bits are "10"**
- Address Range: 128.0.0.0 to 191.255.255.255
- Default Subnet Mask: 255.255.0.0 (or /16 prefix)
- Usage: Used for medium-sized networks, like universities or large businesses. The first 16 bits are the network portion, with the remaining 16 bits available for host addresses.

**Class C:**
**- First three bits are "110"**
- Address Range: 192.0.0.0 to 223.255.255.255
- Default Subnet Mask: 255.255.255.0 (or /24 prefix)
- Usage: Designed for small-sized networks, such as small businesses. Class C provides up to 256 addresses, with the first 24 bits used for the network and the last 8 bits for hosts.

**Class D:**
**- First four bits are "1110"**
- Address Range: 224.0.0.0 to 239.255.255.255
- Usage: Reserved for multicast groups. These addresses are used to deliver traffic to multiple hosts in a group simultaneously, rather than to a single recipient.

**Class E:**
**- First four bits are "1111"**
- Address Range: 240.0.0.0 to 255.255.255.255
- Usage: Reserved for experimental purposes, research, or future use. This class is not used in public networks.

# Octet to Binary Conversion:

----------

1. **Memorize Common Conversions**:
   Certain numbers and their binary equivalents are more common than others (e.g., multiples of 16, 32, 64, etc.). Memorizing these can save time:
   - 128 = 10000000
   - 192 = 11000000 (128 + 64)
   - 224 = 11100000 (128 + 64 + 32)
   - 240 = 11110000 (128 + 64 + 32 + 16)
   - 248 = 11111000 (128 + 64 + 32 + 16 + 8)
   - 252 = 11111100 (128 + 64 + 32 + 16 + 8 + 4)
   - 254 = 11111110 (128 + 64 + 32 + 16 + 8 + 4 + 2)
   - 255 = 11111111 (All bits set to 1)

2. **Bitwise Patterns**:
   Recognizing patterns in the octet can help you quickly identify the binary equivalent. For example:
   - If the decimal is greater than or equal to 128, the first binary digit is 1; otherwise, it's 0.
   - If the decimal is an odd number, the last binary digit is 1; if it's even, it's 0.
   - If the decimal number is a power of 2 (e.g., 1, 2, 4, 8, 16, 32, 64, 128), only one binary digit is 1, and all others are 0.

3. **Subnet Mask Shortcuts**:
   Subnet masks are often in contiguous binary sequences of 1s followed by 0s. Knowing the common subnet masks can make conversion faster:
   - 255.255.255.0 = 11111111.11111111.11111111.00000000
   - 255.255.0.0 = 11111111.11111111.00000000.00000000
   - 255.0.0.0 = 11111111.00000000.00000000.00000000

4. Here's an example, converting the binary sequence 11001100 to an octet:
```
Binary:       1    1    0    0    1    1    0    0
Powers of 2: 128  64   32   16    8    4    2    1
```

# Protocols and Services and Port Numbers:

----------

**TCP Protocols:**
- FTP (File Transfer Protocol): Ports 20 (Data Transfer) and 21 (Control Commands)
- SSH (Secure Shell): Port 22
- Telnet: Port 23
- SMTP (Simple Mail Transfer Protocol): Port 25
- HTTP (Hypertext Transfer Protocol): Port 80
- POP3 (Post Office Protocol version 3): Port 110
- IMAP (Internet Message Access Protocol): Port 143
- HTTPS (HTTP Secure): Port 443
- SNMP (Simple Network Management Protocol) over TLS/DTLS: Port 651
- BGP (Border Gateway Protocol): Port 179
- NetBIOS (used for file sharing in Windows networks):
  - Name service: Port 137 (UDP)
  - Datagram service: Port 138 (UDP)
  - Session service: Port 139 (TCP)

**UDP Protocols:**
- DNS (Domain Name System): Port 53
- TFTP (Trivial File Transfer Protocol): Port 69
- SNMP (Simple Network Management Protocol): Port 161 (SNMP requests), Port 162 (SNMP traps)
- DHCP (Dynamic Host Configuration Protocol):
  - Server: Port 67
  - Client: Port 68
- NTP (Network Time Protocol): Port 123
- Syslog: Port 514 (for UDP, although Syslog can also use TCP)

**Other Protocols (can use either TCP or UDP):**
- LDAP (Lightweight Directory Access Protocol): Port 389
- LDAPS (LDAP over SSL/TLS): Port 636
- SIP (Session Initiation Protocol): Port 5060 (TCP or UDP), Port 5061 (SIP over TLS)

# OSPF and usage of OSPF:

----------

OSPF, or Open Shortest Path First, is a dynamic routing protocol used for routing Internet Protocol (IP) packets within a single routing domain, such as an autonomous system. It is a link-state routing protocol that uses cost as its metric, which is often a measure of the hop count or the bandwidth on the link. OSPF is standardized by the Internet Engineering Task Force (IETF) and defined in RFC 2328 for IPv4 and RFC 5340 for IPv6.

**OSPF Features:**
- **Fast Convergence**: OSPF quickly converges to a stable state after a change in network topology.
- **Scalability**: Suitable for both small and large networks through the use of areas and hierarchical design.
- **Efficiency**: Minimizes routing update traffic because it only sends updates when there is a topology change, not periodically like distance-vector protocols.
- **Robustness**: Utilizes the Dijkstra algorithm to compute the shortest path through a network.
- **Support for VLSM and CIDR**: OSPF can work with Variable Length Subnet Masks and Classless Inter-Domain Routing, which are techniques to optimize the use of IP address space.
- **Load Balancing**: OSPF supports equal-cost multipath (ECMP) routing, allowing traffic to be balanced across multiple paths to the same destination.
- **Route Authentication**: OSPF supports the authentication of routing updates, which can enhance the security of the routing domain.

**Usage of OSPF in Cisco Devices:**
OSPF can be used on Cisco routers and multi-layer switches to manage the routing of IP packets within a network. Here's how OSPF is typically used in Cisco devices:

1. **Network Design**: OSPF is often used in a hierarchical network design. It allows for the division of the network into smaller areas, which reduces routing overhead and improves manageability.

2. **Inter-Area Routing**: OSPF can route between different areas, with Area 0 (known as the backbone area) being the central point through which all other areas must communicate.

3. **Route Summarization**: OSPF allows for the summarization of routes at area boundaries, which can reduce the size of the routing table and improve efficiency.

4. **Redistribution**: OSPF can redistribute routes from other routing protocols (such as RIP, EIGRP, or BGP) and static routes into the OSPF domain.

5. **Route Filtering**: While OSPF does not filter routes during the routing process, it can be configured to control route advertisement through route maps and distribute-lists.

6. **Multi-Vendor Environments**: Because OSPF is a standard protocol, it can be used to facilitate routing in environments that include equipment from multiple vendors.

```shell
Router(config)# router ospf 1
Router(config-router)# network 192.168.1.0 0.0.0.255 area 0
Router(config-router)# network 192.168.2.0 0.0.0.255 area 1
```

In this example, the router is configured to participate in OSPF process ID 1. It advertises two networks, 192.168.1.0/24 in area 0 (backbone area) and 192.168.2.0/24 in area 1.

# OSI Layers

----------


1. **Layer 1: Physical Layer**
   - **Functionality**: Deals with the physical connection between devices and the transmission and reception of raw bit streams over a physical medium.
   - **Components**: Includes cables (coaxial, fiber, twisted pair), switches, hubs, and the physical aspects of connectors, voltage, and pin layout.
   - **Purpose**: To establish, maintain, and deactivate the physical link between devices.

2. **Layer 2: Data Link Layer**
   - **Functionality**: Responsible for node-to-node data transfer between two directly connected nodes, and also handles error correction from the physical layer.
   - **Sublayers**: Divided into two sublayers—Logical Link Control (LLC) and Media Access Control (MAC).
   - **Components**: Network interface cards (NICs), bridges, and switches.
   - **Purpose**: To establish, maintain, and decide how transfer is accomplished over the physical layer.

3. **Layer 3: Network Layer**
   - **Functionality**: Manages device addressing, tracks the location of devices on the network, and determines the best way to move data.
   - **Components**: Routers and layer 3 switches.
   - **Protocols**: Internet Protocol (IP), Internet Control Message Protocol (ICMP), and Open Shortest Path First (OSPF).
   - **Purpose**: To route packets of data from the source to the destination.

4. **Layer 4: Transport Layer**
   - **Functionality**: Provides reliable, transparent transfer of data between end systems, or hosts, and is responsible for end-to-end error recovery and flow control.
   - **Protocols**: Transmission Control Protocol (TCP) and User Datagram Protocol (UDP).
   - **Purpose**: To provide reliable data transfer across the network, and to ensure that messages are delivered error-free, in sequence, and with no losses or duplications.

5. **Layer 5: Session Layer**
   - **Functionality**: Manages sessions between applications. It establishes, manages, and terminates the connections between the local and remote application.
   - **Components**: APIs and sockets that manage sessions between applications.
   - **Purpose**: To establish, manage, and terminate connections between applications on each end.

6. **Layer 6: Presentation Layer**
   - **Functionality**: Ensures that the data is in a usable format and is where data encryption and decryption occurs.
   - **Protocols/Standards**: SSL/TLS, MIME, JPEG, TIFF, ASCII, EBCDIC, etc.
   - **Purpose**: To translate data between the format the network requires and the format the computer expects.

7. **Layer 7: Application Layer**
   - **Functionality**: The layer closest to the end user, which means that both the OSI application layer and the user interact directly with the software application.
   - **Protocols**: Hypertext Transfer Protocol (HTTP), File Transfer Protocol (FTP), Simple Mail Transfer Protocol (SMTP), and Domain Name System (DNS).
   - **Purpose**: To provide network services to the applications of the user, such as email, file transfer, and terminal emulation.

# IPv4 Reserved Addresses

----------


1. **Private Address Ranges (RFC 1918)**:
   - `10.0.0.0` to `10.255.255.255` (10.0.0.0/8): A single class A network used for local communications within a private network.
   - `172.16.0.0` to `172.31.255.255` (172.16.0.0/12): 16 contiguous class B networks used for local communications within a private network.
   - `192.168.0.0` to `192.168.255.255` (192.168.0.0/16): 256 contiguous class C networks used for local communications within a private network.

2. **Loopback Addresses (RFC 1122)**:
   - `127.0.0.0` to `127.255.255.255` (127.0.0.0/8): Used for loopback and internal testing on the local machine. The most commonly used address for testing is `127.0.0.1`.

3. **Link-Local Addresses (RFC 3927)**:
   - `169.254.0.0` to `169.254.255.255` (169.254.0.0/16): Used for automatic IP address configuration when no external method of address configuration (such as DHCP) is available.

4. **APIPA (Automatic Private IP Addressing)**:
   - The same range as Link-Local, `169.254.0.0` to `169.254.255.255`, APIPA is a feature of Windows operating systems for automatic assignment of a unique IP address to a device when DHCP fails.

5. **Multicast Addresses (RFC 1112)**:
   - `224.0.0.0` to `239.255.255.255` (224.0.0.0/4): Used to send traffic to multiple destinations in a single transmission.

6. **Subnet Zero and Broadcast (Older Conventions)**:
   - Historically, the first subnet in a block was reserved as "subnet zero" and the last subnet as "all ones" for broadcast. Modern networking practices use all subnets, and the concept of subnet zero and all-ones subnet is obsolete due to the standardization of CIDR.

7. **Broadcast Address**:
   - The broadcast address is the last address in a given subnet and is used to communicate with all hosts on that subnet.

8. **Reserved for Future Use**:
   - `240.0.0.0` to `255.255.255.254` (240.0.0.0/4): Reserved by IANA for future use, with the exception of `255.255.255.255` which is used for limited broadcast on the local network.

9. **Special-Purpose Address Blocks (RFC 6890)**:
   - Various blocks are reserved for special purposes such as documentation, network testing, and protocols.

10. **Documentation and Example Code (RFC 5737)**:
   - `192.0.2.0` to `192.0.2.255` (192.0.2.0/24)
   - `198.51.100.0` to `198.51.100.255` (198.51.100.0/24)
   - `203.0.113.0` to `203.0.113.255` (203.0.113.0/24)

# IPv6 Reserved Addresses

----------


1. **Unspecified Address**:
   - `::/128`: Indicates the absence of an address. It's equivalent to `0.0.0.0` in IPv4 and used in software to indicate the absence of an IPv6 address.

2. **Loopback Address**:
   - `::1/128`: Used for loopback to the local host. It's equivalent to `127.0.0.1` in IPv4.

3. **Global Unicast Addresses**:
   - `2000::/3`: The range for globally routable addresses, similar to regular public IPv4 addresses.

4. **Unique Local Addresses (ULA)**:
   - `fc00::/7`: Similar to IPv4 private address ranges. These addresses are routable only within a private network and are not globally routable on the internet.
   - Specifically, the `fd00::/8` range is commonly used for ULA.

5. **Link-Local Unicast**:
   - `fe80::/10`: Used for automatic address configuration on a single link and for local communication; not routable beyond the link (local network segment).

6. **Multicast Addresses**:
   - `ff00::/8`: Used for multicast groups. Unlike IPv4, IPv6 doesn't have broadcast addresses; multicast addresses are used instead.

7. **IPv4-Mapped IPv6 Addresses**:
   - `::ffff:0:0/96`: Used to represent IPv4 addresses within an IPv6 environment.

8. **IPv6 Address Space Reserved for Documentation and Examples (RFC 3849)**:
   - `2001:db8::/32`: Reserved for use in documentation and example code.

9. **6to4 Addressing**:
   - `2002::/16`: Used for the 6to4 transition mechanism, which enables IPv6 packets to be transmitted over an IPv4 network without the need to configure explicit tunnels.

10. **Teredo Addressing**:
   - `2001::/32`: Used for the Teredo tunneling protocol, which allows IPv6 connectivity across the IPv4 internet.

11. **Site-Local Addresses (Deprecated)**:
   - `fec0::/10`: Initially intended for addresses local to a site. These addresses have been deprecated in favor of Unique Local Addresses (ULA).

# Available Subnet and Host Addresses Calulation:

----------

**Number of Available Subnets**:
If you are subnetting a larger network into smaller subnets, the formula to calculate the number of available subnets is:
\[ \text{Number of subnets} = 2^{(n-m)} \]
where:
- \( n \) is the number of bits used for subnetting (new subnet bits).
- \( m \) is the number of bits originally used for subnetting in the original network (old subnet bits).

When not dealing with subnetting inside an already subnetted address space, and you are simply using the standard classful network as your starting point, the formula simplifies to:
\[ \text{Number of subnets} = 2^n \]
where \( n \) is the number of bits borrowed from the host portion to create additional subnets.

**Number of Available Hosts Per Subnet**:
The formula to calculate the number of available hosts per subnet is:
\[ \text{Number of hosts} = 2^h - 2 \]
where:
- \( h \) is the number of bits remaining for the host portion of the address (after subnetting).
- The subtraction of 2 accounts for the network address and the broadcast address, which cannot be assigned to hosts.

Here's a step-by-step example of how to use these formulas. Let's say we have the IP address 192.168.1.0 with a subnet mask of 255.255.255.192 (/26).

1. **Calculate Subnets**:
The subnet mask /26 means that 26 bits are used for the network portion. If this is a Class C address (which normally has a 24-bit network portion), then we have borrowed 2 bits for subnetting (26 - 24).
\[ \text{Number of subnets} = 2^{(26-24)} = 2^2 = 4 \]
So, we have 4 subnets.

2. **Calculate Hosts**:
There are 32 bits in an IPv4 address, so if 26 are used for the network portion, then 6 are left for the host portion.
\[ \text{Number of hosts} = 2^6 - 2 = 64 - 2 = 62 \]
So, each subnet has 62 usable host addresses.

# Steps to Network and Broadcast Addresses:

----------

1. **Calculate the Network Address**:
   - Convert the IPv4 address and its subnet mask to binary.
   - Perform a logical AND operation between the binary IP address and the binary subnet mask.
   - Convert the resulting binary number back to decimal. This is the network address.

2. **Calculate the Broadcast Address**:
   - Convert the network address (obtained in the previous step) to binary.
   - Invert the subnet mask (change 1s to 0s and 0s to 1s) to get the wildcard mask.
   - Perform a logical OR operation between the binary network address and the binary wildcard mask.
   - Convert the resulting binary number back to decimal. This is the broadcast address.

Let's go through an example. Assume we have the following IP address and subnet mask:

IP Address: `192.168.1.10`
Subnet Mask: `255.255.255.240` (or /28 in CIDR notation)

**Calculate the Network Address**:

1. Convert IP address and subnet mask to binary:
   ```
   IP Address:      11000000.10101000.00000001.00001010    (192.168.1.10)
   Subnet Mask:     11111111.11111111.11111111.11110000    (255.255.255.240)
   ```

2. Perform a logical AND operation:
   ```
   Network Address: 11000000.10101000.00000001.00000000    (192.168.1.0)
   ```

3. Convert back to decimal:
   The network address is `192.168.1.0`.

**Calculate the Broadcast Address**:

1. Invert the subnet mask to obtain the wildcard mask:
   ```
   Subnet Mask:     11111111.11111111.11111111.11110000    (255.255.255.240)
   Wildcard Mask:   00000000.00000000.00000000.00001111
   ```

2. Perform a logical OR operation between the network address and the wildcard mask:
   ```
   Network Address: 11000000.10101000.00000001.00000000    (192.168.1.0)
   Wildcard Mask:   00000000.00000000.00000000.00001111
   Broadcast Addr:  11000000.10101000.00000001.00001111
   ```

3. Convert back to decimal:
   The broadcast address is `192.168.1.15`.
#### Reference Link: Sample data for the IPv4 network and broadcast addresses for a given IP address

https://www.calculator.net/ip-subnet-calculator.html?cclass=any&csubnet=28&cip=192.168.1.10&ctype=ipv4&x=Calculate

IPv4 Subnet Calculator Result:

| IP Address:             | 192.168.1.10                        |

----------
| Network Address:        | 192.168.1.0                         |
| Usable Host IP Range:   | 192.168.1.1 - 192.168.1.14          |
| Broadcast Address:      | 192.168.1.15                        |
| Total Number of Hosts:  | 16                                  |
| Number of Usable Hosts: | 14                                  |
| Subnet Mask:            | 255.255.255.240                     |
| Wildcard Mask:          | 0.0.0.15                            |
| Binary Subnet Mask:     | 11111111.11111111.11111111.11110000 |
| IP Class:               | C                                   |
| CIDR Notation:          | /28                                 |
| IP Type:                | Private                             |
|                         |                                     |
| Short:                  | 192.168.1.10 /28                    |
| Binary ID:              | 11000000101010000000000100001010    |
| Integer ID:             | 3232235786                          |
| Hex ID:                 | 0xc0a8010a                          |
| in-addr.arpa:           | 10.1.168.192.in-addr.arpa           |
| IPv4 Mapped Address:    | ::ffff:c0a8.010a                    |
| 6to4 Prefix:            | 2002:c0a8.010a::/48                 |


All 16 of the Possible /28 Networks for 192.168.1.*

| Network Address | Usable Host Range             | Broadcast Address: |

----------
| 192.168.1.0     | 192.168.1.1 - 192.168.1.14    | 192.168.1.15       |
| 192.168.1.16    | 192.168.1.17 - 192.168.1.30   | 192.168.1.31       |
| 192.168.1.32    | 192.168.1.33 - 192.168.1.46   | 192.168.1.47       |
| 192.168.1.48    | 192.168.1.49 - 192.168.1.62   | 192.168.1.63       |
| 192.168.1.64    | 192.168.1.65 - 192.168.1.78   | 192.168.1.79       |
| 192.168.1.80    | 192.168.1.81 - 192.168.1.94   | 192.168.1.95       |
| 192.168.1.96    | 192.168.1.97 - 192.168.1.110  | 192.168.1.111      |
| 192.168.1.112   | 192.168.1.113 - 192.168.1.126 | 192.168.1.127      |
| 192.168.1.128   | 192.168.1.129 - 192.168.1.142 | 192.168.1.143      |
| 192.168.1.144   | 192.168.1.145 - 192.168.1.158 | 192.168.1.159      |
| 192.168.1.160   | 192.168.1.161 - 192.168.1.174 | 192.168.1.175      |
| 192.168.1.176   | 192.168.1.177 - 192.168.1.190 | 192.168.1.191      |
| 192.168.1.192   | 192.168.1.193 - 192.168.1.206 | 192.168.1.207      |
| 192.168.1.208   | 192.168.1.209 - 192.168.1.222 | 192.168.1.223      |
| 192.168.1.224   | 192.168.1.225 - 192.168.1.238 | 192.168.1.239      |
| 192.168.1.240   | 192.168.1.241 - 192.168.1.254 | 192.168.1.255      |

#  Study Notes:

**Ethernet switches:** Ethernet switches form the aggregation point for LANs. Ethernet switches operate at Layer 2 of the Open Systems Interconnection (OSI) model and provide intelligent distribution of frames within the LAN.

**Routers:** Routers, sometimes called gateways, provide a means to connect LAN segments and provide connectivity to the internet. Routers operate at Layer 3 of the OSI model.

**APs:** APs provide wireless connectivity to LAN devices. APs operate at Layer 2 of the OSI model.

**Protocols:** Protocols are rules that govern how data is transmitted between components of a network. Here are some commonly used LAN protocols:

**Ethernet protocols (IEEE 802.2 and IEEE 802.3):**
* IP
* TCP
* UDP
* Address Resolution Protocol (ARP) for IPv4 and Neighbor Discovery Protocol (NDP) for IPv6
* Common Internet File System (CIFS)
* DHCP

----------

Switches have the following features and functions:

Operate at the link layer of the TCP/IP protocol suite

Selectively forward individual frames

Have many ports to segment a large LAN into many smaller segments

Have high speed and support various port speeds


What is the main purpose of a switch?
    To **forward frames as fast and as efficiently as possible** on the connected segments that require them.


**Characteristics and Features of Switches:**
* Dedicated communication between devices
* Multiple simultaneous conversations

Some important characteristics of switches:

High port density: Switches have high port densities: 24-, 32-, and 48-port switches operate at speeds of 100 Mbps, 1 Gbps, 10 Gbps, 25 Gbps, 40 Gbps, and 100 Gbps. Large enterprise switches may support hundreds of ports.

Large frame buffers: The ability to store more received frames before having to start dropping them is useful, particularly when there may be congested ports connected to servers or other heavily used parts of the network.

Port speed: Depending on the switch, port speed may be possible to support a range of bandwidths. Ports of 100 Mbps, 1Gbps, and 10 Gbps are expected, but 40- or 100-Gbps ports allow even more flexibility.

Fast internal switching: Having fast internal switching allows higher bandwidths: 100 Mbps, 1 Gbps, 10 Gbps, 25 Gbps, 40 Gbps, and 100 Gbps.

Low per-port cost: Switches provide high port density at a lower cost. For this reason, LAN switches can accommodate network designs that feature fewer users per segment. This feature, therefore, increases the average available bandwidth per user.


Which switch feature allows switches to operate at a high speed of 10 Gbps?
	fast internal switching

What are the two defining characteristics of a LAN? (Choose two.)
	higher data transfer rates in contrast to WAN
	smaller geographic area in contrast to WAN

What are the two typical hosts or endpoints on a LAN? (Choose two.)
	servers
	laptops

Which switch characteristic can accommodate network designs that feature fewer users per segment?
	low per-port cost

Which advantage does a switch bring to a LAN environment?
	breaks up segments

Which of the following provides a channel for data to travel from one point to another in the network?
	interconnections

What are the three functions of a switch? (Choose three.)
	Switches operate at the link layer of the TCP/IP protocol suite.
	Switches selectively forward individual frames.
	Switches have many full-duplex ports to segment a large LAN into many smaller segments.

Which statement regarding switch characteristics is correct?
	A generic CPU is too slow for forwarding traffic in a switch.



**Unshielded Twisted-Pair Cable:**

    Characteristic => Value
    Speed and throughput => From 10 Mbps to 40 Gbps
    Average cost per node => Least expensive
    Media and connector size => Small
    Maximum cable length => 100 m (30 m for 40 Gbps)

Several categories of UTP cable exist:

	Category 5: Capable of transmitting data at speeds of up to 100 Mbps
	Category 5e: Used in networks running at speeds of up to 1000 Mbps (1 Gbps)
	Category 6: Comprises four pairs of 24-gauge copper wires, which can transmit data at speeds of up to 10 Gbps
	Category 6a: Used in networks running at speeds of up to 10 Gbps
	Category 7: Used in networks running at speeds of up to 10 Gbps
	Category 8: Used in networks running at speeds of up to 40 Gbps

Crossover Cables:

	Switch-to-Switch
	Router-to-Router
	Router-to-PC
	PC-to-PC

Straight-Through Cables:

	Switch-to-Router
	Switch-to-PC
	Switch-to-Server


Fiber Types:

	Multimode Fiber (MMF)
	Single-Mode Fiber (SMF)


MMF and SMF Characteristics:

	MMF Characteristics:
		LED transmitter is usually used
		Lower bandwidth and speed
		Shorter distances
		Less expensive

	SMF Characteristics:
		Laser transmitter is usually used
		Higher bandwidth and speed
		Longer distances
		More expensive

----------
Which two connections were traditionally made by using crossover cables? (Choose two.)
	switch-to-switch and router-to-router

----------

# IPv6 Basic Configuration:


Configuring and verifying basic IPv6 connectivity on a Cisco device involves several steps:

1. **Entering Configuration Mode**:
   ```
   Router> enable
   Router# configure terminal
   Router(config)#
   ```

2. **Assigning an IPv6 Address**:
   You can assign an IPv6 address to an interface using the following commands (replace `Ethernet0/0` with your interface identifier and use a valid IPv6 address):
   ```
   Router(config)# interface Ethernet0/0
   Router(config-if)# ipv6 address 2001:db8::1/64
   Router(config-if)# no shutdown
   ```

3. **Enabling IPv6 Routing** (if needed):
   By default, IPv6 routing is not enabled on Cisco devices. You can enable it using:
   ```
   Router(config)# ipv6 unicast-routing
   ```

4. **Verifying the Configuration**:
   You can verify that the interface has been assigned the correct IPv6 address using:
   ```
   Router# show ipv6 interface Ethernet0/0
   ```
   This command will display the IPv6 address assigned to the interface, along with other interface-specific IPv6 information.

5. **Testing Connectivity**:
   Use the `ping` command to test connectivity to another IPv6 address:
   ```
   Router# ping ipv6 2001:db8::2
   ```
   If the ping is successful, it indicates that basic IPv6 connectivity is functioning properly.

----------

# Link Aggregation Sample Config:

----------


Configuring **link aggregation using EtherChannel on a Cisco switch involves bundling several physical Ethernet links to form a single logical link to provide higher bandwidth and redundancy**. EtherChannel can be configured to use either the Port Aggregation Protocol (PAgP), which is Cisco proprietary, or the Link Aggregation Control Protocol (LACP), which is an IEEE standard (802.3ad).

Here's a basic step-by-step guide to configure EtherChannel using LACP on a Cisco device:

1. **Enter Global Configuration Mode**:
   ```
   Switch> enable
   Switch# configure terminal
   Switch(config)#
   ```

2. **Select the Interfaces**:
   Choose the interfaces that you want to aggregate. For example, to configure EtherChannel on interfaces GigabitEthernet0/1 and GigabitEthernet0/2, you would begin by entering interface range configuration mode:
   ```
   Switch(config)# interface range GigabitEthernet0/1 - 2
   ```

3. **Assign the Interfaces to an EtherChannel Group**:
   While in the interface range configuration mode, assign the interfaces to an EtherChannel group. You can also specify the protocol to use (in this case, LACP). The channel-group number is an identifier for the EtherChannel (in this example, we're using number 1).
   ```
   Switch(config-if-range)# channel-group 1 mode active
   ```
   The `active` keyword sets the interfaces to actively negotiate an LACP EtherChannel. If you want to set up the EtherChannel without LACP negotiation, you could use `on`, but this is not recommended because it doesn't ensure both ends of the EtherChannel are configured consistently.

4. **Configure the Port-Channel Interface**:
   After assigning physical interfaces to a channel-group, a logical port-channel interface is created automatically. You need to configure this interface next:
   ```
   Switch(config)# interface Port-channel1
   ```
   Now you can configure the logical interface just like any other interface. For instance, you could assign it to a VLAN or configure its IP address (if it's a Layer 3 EtherChannel).

5. **(Optional) Configure Load Balancing**:
   Configure how the switch will distribute traffic over the EtherChannel links. For example:
   ```
   Switch(config)# port-channel load-balance src-dst-ip
   ```
   This command would configure the switch to distribute packets across the EtherChannel links based on the source and destination IP addresses.

6. **Save the Configuration**:
   Save your configuration to avoid losing changes if the switch restarts:
   ```
   Switch(config)# end
   Switch# write memory
   ```
   or
   ```
   Switch# copy running-config startup-config
   ```

7. **Verify the EtherChannel Configuration**:
   Use the `show` command to verify that the EtherChannel is up and running:
   ```
   Switch# show etherchannel summary
   ```
   Look for the `Port-channel1` in the output and make sure the status is `P`, which stands for 'in port-channel', and `U`, which means 'up'.

# DCHP Sample Configuration:

----------
1. **Configure the Router as a DHCP Server**:
   To configure the Cisco router to provide DHCP services to clients, you need to define a DHCP pool with the range of IP addresses to be assigned to clients, along with other necessary parameters.

   Enter global configuration mode:
   ```bash
   Router> enable
   Router# configure terminal
   ```

   Define the DHCP pool:
   ```bash
   Router(config)# ip dhcp pool LAN_POOL
   Router(dhcp-config)# network 192.168.1.0 255.255.255.0
   Router(dhcp-config)# default-router 192.168.1.1
   Router(dhcp-config)# dns-server 8.8.8.8 8.8.4.4
   Router(dhcp-config)# lease 7
   ```

   Here, `192.168.1.0` is the network address with a subnet mask of `255.255.255.0`, `192.168.1.1` is the default gateway, and the `dns-server` command specifies the DNS servers to be used by the DHCP clients. The `lease 7` specifies the duration of the lease in days.

2. **Exclude IP Addresses**:
   If there are IP addresses within the pool that you don’t want the DHCP server to assign (e.g., addresses for printers, servers, or other statically assigned devices), you need to exclude them:

   ```bash
   Router(config)# ip dhcp excluded-address 192.168.1.1 192.168.1.10
   ```

3. **Verify DHCP Configuration**:
   You can verify that the DHCP server is configured correctly and view the assigned IP addresses using the following command:

   ```bash
   Router# show ip dhcp binding
   ```

   This shows a list of all IP addresses that have been leased to clients.

# Configure and Verify NAT:

----------
Network Address Translation (NAT) is commonly used to translate private IP addresses to a single public IP address or a pool of public addresses. This is necessary to allow devices on a local network to access the Internet using a limited number of public IP addresses.

1. **Define Inside and Outside Interfaces**:
   Typically, the "inside" interface connects to the private network, and the "outside" interface connects to the public network (the Internet).

   Enter interface configuration mode for the inside interface:
   ```bash
   Router(config)# interface GigabitEthernet0/0
   Router(config-if)# ip nat inside
   Router(config-if)# exit
   ```

   Then, do the same for the outside interface:
   ```bash
   Router(config)# interface GigabitEthernet0/1
   Router(config-if)# ip nat outside
   Router(config-if)# exit
   ```

2. **Create an Access Control List (ACL)**:
   An ACL is used to define which local IP addresses are allowed to be translated.

   ```bash
   Router(config)# access-list 1 permit 192.168.1.0 0.0.0.255
   ```

   This command allows all IP addresses from the `192.168.1.0/24` network to be subject to NAT.

3. **Set Up the NAT Overload (PAT)**:
   Configure NAT with Port Address Translation (PAT) to allow multiple devices to share a single public IP address.

   ```bash
   Router(config)# ip nat inside source list 1 interface GigabitEthernet0/1 overload
   ```

   This command instructs the router to translate any IP addresses that match ACL 1 to the IP address assigned to `GigabitEthernet0/1` and use PAT to allow multiple hosts to share the single address.

4. **Verify NAT Configuration**:
   You can verify that NAT is working correctly using the following command:

   ```bash
   Router# show ip nat translations
   ```

   This command displays a table of current NAT translations active on the router.

Remember to replace the interface identifiers (`GigabitEthernet0/0`, `GigabitEthernet0/1`), IP addresses

----------

Configure and verify basic IOS system monitoring tools on a Cisco device?

Configuring and verifying basic IOS system monitoring tools on a Cisco device can involve several steps, depending on what specifically you need to monitor. Here are some common system monitoring tools and commands used on Cisco devices:

# Configure Logging:

----------
1. **Console Logging**:
   By default, Cisco devices log messages to the console terminal. You can configure the level of messages displayed:

   ```bash
   Router(config)# logging console informational
   ```

   The above command sets the console logging level to "informational," which means that all messages with a severity level of informational or higher will be displayed on the console.

2. **Buffered Logging**:
   To save log messages to the router's internal buffer, use:

   ```bash
   Router(config)# logging buffered 10000
   ```

   This command sets the buffer size to 10,000 bytes. The buffer size and severity level can be adjusted as needed.

3. **Remote Logging**:
   To send log messages to a syslog server, you can configure:

   ```bash
   Router(config)# logging host 192.168.1.100
   ```

   Replace `192.168.1.100` with the IP address of your syslog server.

### Verify Logging

To verify your logging configuration, you can use:

```bash
Router# show logging
```

This command displays the logging configuration and the log buffer contents.

### Monitor Interfaces and Traffic

1. **Interface Status**:
   To check the status of an interface, use:

   ```bash
   Router# show interface GigabitEthernet0/1
   ```

   Replace `GigabitEthernet0/1` with the appropriate interface identifier. This command shows a variety of information including the interface status, protocol status, MAC address, and statistics about the traffic passing through the interface.

2. **Interface Traffic**:
   To monitor the real-time traffic on an interface, you can use:

   ```bash
   Router# show interfaces GigabitEthernet0/1
   ```

   This will give you a detailed view of the traffic statistics on the specified interface.

### Monitor CPU and Memory Usage

1. **CPU Usage**:
   To check the CPU utilization on the device, use:

   ```bash
   Router# show processes cpu
   ```

   This command shows the CPU utilization for processes over the last 5 seconds, 1 minute, and 5 minutes.

2. **Memory Usage**:
   To view the memory usage, use:

   ```bash
   Router# show memory
   ```

   This command displays the memory usage statistics of the device, including the total memory and free memory.

### Configuration and Routing Information

1. **Running Configuration**:
   To view the current running configuration, use:

   ```bash
   Router# show running-config
   ```

2. **Routing Table**:
   To view the routing table, use:

   ```bash
   Router# show ip route
   ```

   This command displays the IP routing table, which shows how the router would route packets to various network destinations.

### Monitor Network Connectivity

1. **Ping**:
   To verify network connectivity to another IP address, use:

   ```bash
   Router# ping 192.168.1.100
   ```

   Replace `192.168.1.100` with the target IP address.

2. **Traceroute**:
   To trace the path packets take to reach a destination, use:

   ```bash
   Router# traceroute 192.168.1.100
   ```

3. **Connectivity Test with Extended Ping**:
   You can perform an extended ping test by entering the `ping` command and then responding to the prompts for more detailed options:

   ```bash
   Router# ping
   Protocol [ip]:
   Target IP address: 192.168.1.100
   Repeat count [5]:
   Datagram size [100]:
   Timeout in seconds [2]:
   Extended commands [n]: y
   Source address or interface:
   Type of service [0]:
   Set DF bit in IP header? [no]:
   Validate reply data? [no]:
   Data pattern [0xABCD]:
   Loose, Strict, Record, Timestamp, Verbose[none]:
   Sweep range of sizes [n]:
   ```

----------
# Cisco Discovery Protocol (CDP)

CDP is a Cisco proprietary protocol that is enabled by default on most Cisco devices. It allows devices to discover and view detailed information about directly connected Cisco devices, including model number, IP address, connected interface, and software version.

# Configure CDP

1. **Enable CDP Globally (if disabled)**:
   ```bash
   Router(config)# cdp run
   ```

2. **Enable CDP on an Interface (if disabled)**:
   To enable CDP on a specific interface, enter interface configuration mode and then enable CDP:
   ```bash
   Router(config)# interface GigabitEthernet0/0
   Router(config-if)# cdp enable
   ```

# Verify CDP

1. **Check CDP Status Globally**:
   To verify if CDP is enabled globally on the device:
   ```bash
   Router# show cdp
   ```

2. **Check CDP Neighbors**:
   To view information about CDP neighbors (other Cisco devices connected directly to this device):
   ```bash
   Router# show cdp neighbors
   ```

   To get detailed information about a neighbor, including the interface on the neighbor that connects to your device:
   ```bash
   Router# show cdp neighbors detail
   ```

----------
# Link Layer Discovery Protocol (LLDP)

LLDP is an industry-standard protocol similar to CDP that provides a method for network devices to advertise information about themselves to other devices on the network. LLDP is not enabled by default on Cisco devices.

# Configure LLDP

1. **Enable LLDP Globally**:
   ```bash
   Router(config)# lldp run
   ```

2. **Enable LLDP on an Interface**:
   To enable LLDP on a specific interface, enter interface configuration mode and then enable LLDP:
   ```bash
   Router(config)# interface GigabitEthernet0/0
   Router(config-if)# lldp transmit
   Router(config-if)# lldp receive
   ```

# Verify LLDP

1. **Check LLDP Status Globally**:
   To verify if LLDP is enabled globally on the device:
   ```bash
   Router# show lldp
   ```

2. **Check LLDP Neighbors**:
   To view information about LLDP neighbors:
   ```bash
   Router# show lldp neighbors
   ```

   For detailed information about a neighbor:
   ```bash
   Router# show lldp neighbors detail
   ```

# Disabling CDP or LLDP

If you need to disable these protocols for security or other reasons:

1. **Disable CDP Globally**:
   ```bash
   Router(config)# no cdp run
   ```

2. **Disable CDP on an Interface**:
   ```bash
   Router(config)# interface GigabitEthernet0/0
   Router(config-if)# no cdp enable
   ```

3. **Disable LLDP Globally**:
   ```bash
   Router(config)# no lldp run
   ```

4. **Disable LLDP on an Interface**:
   ```bash
   Router(config)# interface GigabitEthernet0/0
   Router(config-if)# no lldp transmit
   Router(config-if)# no lldp receive
   ```

When enabling or disabling these protocols, always ensure that the changes align with your network policy and security guidelines. Remember to replace `GigabitEthernet0/0` with the appropriate interface identifier on your device.

----------

# Verify the Default Gateway Configuration

1. **Enter Global Configuration Mode**:
   ```
   Router> enable
   Router# configure terminal
   Router(config)#
   ```

2. **Configure the Default Route**:
1. **On a Router**:
   The default route is used to forward packets destined for networks not explicitly listed in the routing table. It is typically pointed towards the next-hop router that connects to the ISP or the wider internet.

   For IP routing, you would configure a default route to define the default gateway like this:
   ```bash
   Router(config)# ip route 0.0.0.0 0.0.0.0 [next-hop-ip-address or exit-interface]
   ```

   For example, if the next-hop IP address is `192.168.1.254`, you would use:
   ```bash
   Router(config)# ip route 0.0.0.0 0.0.0.0 192.168.1.254
   ```

   Or if you prefer to specify the exit interface, say `GigabitEthernet0/1`:
   ```bash
   Router(config)# ip route 0.0.0.0 0.0.0.0 GigabitEthernet0/1
   ```

   To verify the default route has been configured, use the following command:
   ```bash
   Router# show ip route
   ```
   Look for the `S*` entry, which indicates the static default route.

2. **On a Switch**:

1. **Enter Global Configuration Mode**:
   ```
   Switch> enable
   Switch# configure terminal
   Switch(config)#
   ```

2. **Set the Default Gateway**:
   Specify the IP address of the default gateway (the router interface that's on the same network as the switch's management interface).

   ```bash
   Switch(config)# ip default-gateway [gateway-ip-address]
   ```

   For example:
   ```bash
   Switch(config)# ip default-gateway 192.168.1.254
   ```

3. **Save the Configuration**:
   ```bash
   Switch(config)# end
   Switch# write memory
   ```
   or
   ```bash
   Switch# copy running-config startup-config
   ```

   To verify the default gateway setting on a switch, use:
   ```bash
   Switch# show ip default-gateway
   ```
   or
   ```bash
   Switch# show running-config
   ```
   The running configuration should display the default gateway that you have set.

----------

### Configure IPv4 Static Routes

1. **Enter Global Configuration Mode**:
   ```
   Router> enable
   Router# configure terminal
   Router(config)#
   ```

2. **Add a Static Route**:
   To add a static route, you need to specify the destination network, the subnet mask, and either the next-hop IP address or the exit interface. Here is the general command:

   ```bash
   Router(config)# ip route [destination-network] [subnet-mask] [next-hop-ip-address | exit-interface]
   ```

   For example, if you need to route traffic destined for the `192.168.2.0` network with a `255.255.255.0` subnet mask to a next-hop router with an IP address of `10.0.0.2`, you would use:

   ```bash
   Router(config)# ip route 192.168.2.0 255.255.255.0 10.0.0.2
   ```

   Alternatively, if you prefer to specify the exit interface instead of the next-hop IP address, for example, `GigabitEthernet0/1`, use:

   ```bash
   Router(config)# ip route 192.168.2.0 255.255.255.0 GigabitEthernet0/1
   ```

3. **Save the Configuration**:
   After configuring your static routes, save the configuration:

   ```bash
   Router(config)# end
   Router# write memory
   ```
   or
   ```bash
   Router# copy running-config startup-config
   ```

### Verify IPv4 Static Routes

1. **Show the Routing Table**:
   To verify that the static route has been added, look at the IP routing table:

   ```bash
   Router# show ip route
   ```

   This command displays the device’s routing table. You should see the static route(s) you configured listed with an `S` to indicate a static route.

2. **Test Connectivity**:
   You can test connectivity to the destination network by trying to ping a device on that network:

   ```bash
   Router# ping [destination-ip-address]
   ```

   Replace `[destination-ip-address]` with an IP address on the `192.168.2.0` network to ensure the static route is working.

3. **Detailed Static Route Verification**:
   To verify a particular static route, you can use an extended `show ip route` command:

   ```bash
   Router# show ip route static
   ```

   This will list only the static routes in the routing table.

4. **Trace the Path**:
   Use the `traceroute` command to see the path that traffic takes to reach the destination. This can help verify that traffic is following the static route you have configured:

   ```bash
   Router# traceroute [destination-ip-address]
   ```

----------

### Configure IPv6 Static Routes

1. **Enter Global Configuration Mode**:
   ```
   Router> enable
   Router# configure terminal
   Router(config)#
   ```

2. **Add an IPv6 Static Route**:
   To add a static route for IPv6, you need to specify the destination network, the prefix length (similar to subnet mask in IPv4), and either the next-hop IPv6 address or the exit interface. Here is the general command:

   ```bash
   Router(config)# ipv6 route [ipv6-destination-prefix]/[prefix-length] [ipv6-next-hop-address | exit-interface]
   ```

   For example, if you need to route traffic destined for the `2001:DB8:ACAD:2::/64` network to a next-hop router with an IPv6 address of `2001:DB8:ACAD:1::2`, you would use:

   ```bash
   Router(config)# ipv6 route 2001:DB8:ACAD:2::/64 2001:DB8:ACAD:1::2
   ```

   Alternatively, if you prefer to specify the exit interface instead of the next-hop IPv6 address, for example, `GigabitEthernet0/1`, use:

   ```bash
   Router(config)# ipv6 route 2001:DB8:ACAD:2::/64 GigabitEthernet0/1
   ```

3. **Save the Configuration**:
   After configuring your static routes, save the configuration:

   ```bash
   Router(config)# end
   Router# write memory
   ```
   or
   ```bash
   Router# copy running-config startup-config
   ```

### Verify IPv6 Static Routes

1. **Show the IPv6 Routing Table**:
   To verify that the static route has been added, look at the IPv6 routing table:

   ```bash
   Router# show ipv6 route
   ```

   This command displays the device’s IPv6 routing table. You should see the static route(s) you configured listed with an `S` to indicate a static route.

2. **Test Connectivity**:
   You can test connectivity to the destination network by trying to ping an IPv6 address on that network:

   ```bash
   Router# ping ipv6 [ipv6-destination-address]
   ```

   Replace `[ipv6-destination-address]` with an IPv6 address on the `2001:DB8:ACAD:2::/64` network to ensure the static route is working.

3. **Detailed Static Route Verification**:
   To verify a particular static route, you can use an extended `show ipv6 route` command:

   ```bash
   Router# show ipv6 route static
   ```

   This will list only the static IPv6 routes in the routing table.

4. **Trace the Path**:
   Use the `traceroute` command to see the path that traffic takes to reach the destination. This can help verify that traffic is following the static route you have configured:

   ```bash
   Router# traceroute ipv6 [ipv6-destination-address]
   ```

----------
### Configure VLANs on a Cisco Switch

1. **Enter Global Configuration Mode**:
   ```
   Switch> enable
   Switch# configure terminal
   Switch(config)#
   ```

2. **Create VLANs**:
   Use the `vlan` command to create a new VLAN and then give it a name with the `name` command.
   ```bash
   Switch(config)# vlan 10
   Switch(config-vlan)# name Sales
   Switch(config-vlan)# exit

   Switch(config)# vlan 20
   Switch(config-vlan)# name Engineering
   Switch(config-vlan)# exit
   ```

3. **Assign Interfaces to VLANs**:
   Assign switch ports to the VLANs you created.
   ```bash
   Switch(config)# interface FastEthernet0/1
   Switch(config-if)# switchport mode access
   Switch(config-if)# switchport access vlan 10
   Switch(config-if)# exit

   Switch(config)# interface FastEthernet0/2
   Switch(config-if)# switchport mode access
   Switch(config-if)# switchport access vlan 20
   Switch(config-if)# exit
   ```

   Repeat the process for all interfaces that you want to associate with VLANs.

4. **Save the Configuration**:
   ```bash
   Switch(config)# end
   Switch# write memory
   ```
   or
   ```bash
   Switch# copy running-config startup-config
   ```

### Configure Trunking on a Cisco Switch

1. **Identify the Trunk Port**:
   Choose the interface that will act as the trunk link, usually connecting to another switch or a router for inter-VLAN routing.

2. **Set the Interface to Trunk Mode**:
   ```bash
   Switch(config)# interface GigabitEthernet0/1
   Switch(config-if)# switchport mode trunk
   ```

3. **(Optional) Specify Allowed VLANs**:
   By default, a trunk port will allow all VLANs across the link. To restrict the trunk to carry only specific VLANs, use the following command:
   ```bash
   Switch(config-if)# switchport trunk allowed vlan 10,20
   ```

4. **(Optional) Set the Native VLAN**:
   The native VLAN is the VLAN that is untagged on the trunk link. By default, it is VLAN 1, but it can be changed:
   ```bash
   Switch(config-if)# switchport trunk native vlan 99
   ```

5. **Save the Configuration**:
   ```bash
   Switch(config-if)# end
   Switch# write memory
   ```
   or
   ```bash
   Switch# copy running-config startup-config
   ```

### Verify VLANs and Trunk Configuration

1. **Show VLAN Information**:
   To verify that VLANs have been created and to see which ports are assigned to them:
   ```bash
   Switch# show vlan brief
   ```

2. **Show Specific VLAN**:
   To see details about a specific VLAN (e.g., VLAN 10):
   ```bash
   Switch# show vlan id 10
   ```

3. **Show Trunk Status**:
   To verify trunk configuration and status:
   ```bash
   Switch# show interfaces trunk
   ```

   This will display information about the trunk, including the native VLAN and allowed VLANs on the trunk.

4. **Check Interface Switchport**:
   To check the mode and characteristics of a specific interface:
   ```bash
   Switch# show interface GigabitEthernet0/1 switchport
   ```

----------

### Configure Inter-VLAN Routing on a Cisco Router (Router-on-a-Stick)

1. **Enter Global Configuration Mode**:
   ```
   Router> enable
   Router# configure terminal
   Router(config)#
   ```

2. **Create Subinterfaces**:
   For each VLAN, create a subinterface on the router's physical interface connected to the switch's trunk port.
   ```bash
   Router(config)# interface GigabitEthernet0/0.10
   Router(config-subif)# encapsulation dot1Q 10
   Router(config-subif)# ip address 192.168.10.1 255.255.255.0
   Router(config-subif)# exit

   Router(config)# interface GigabitEthernet0/0.20
   Router(config-subif)# encapsulation dot1Q 20
   Router(config-subif)# ip address 192.168.20.1 255.255.255.0
   Router(config-subif)# exit
   ```

   Here, `GigabitEthernet0/0` is the physical interface on the router connected to the switch's trunk port. `10` and `20` after the interface are the VLAN IDs, and `encapsulation dot1Q` is the trunking protocol used.

3. **Enable the Physical Interface**:
   Make sure the physical interface that the subinterfaces are linked to is up and not administratively down.
   ```bash
   Router(config)# interface GigabitEthernet0/0
   Router(config-if)# no shutdown
   ```

4. **Save the Configuration**:
   ```
   Router(config)# end
   Router# write memory
   ```
   or
   ```bash
   Router# copy running-config startup-config
   ```

### Configure Inter-VLAN Routing on a Layer 3 Switch (Using SVIs)

1. **Enter Global Configuration Mode**:
   ```
   Switch> enable
   Switch# configure terminal
   Switch(config)#
   ```

2. **Create VLANs**:
   ```bash
   Switch(config)# vlan 10
   Switch(config-vlan)# exit

   Switch(config)# vlan 20
   Switch(config-vlan)# exit
   ```

3. **Create SVIs for Each VLAN**:
   ```bash
   Switch(config)# interface vlan 10
   Switch(config-if)# ip address 192.168.10.1 255.255.255.0
   Switch(config-if)# no shutdown
   Switch(config-if)# exit

   Switch(config)# interface vlan 20
   Switch(config-if)# ip address 192.168.20.1 255.255.255.0
   Switch(config-if)# no shutdown
   Switch(config-if)# exit
   ```

   Each SVI acts as the default gateway for the corresponding VLAN.

4. **Enable IP Routing (if not already enabled)**:
   ```bash
   Switch(config)# ip routing
   ```

5. **Save the Configuration**:
   ```
   Switch(config)# end
   Switch# write memory
   ```
   or
   ```bash
   Switch# copy running-config startup-config
   ```

### Verify Inter-VLAN Routing

1. **Show IP Interfaces**:
   Verify that the subinterfaces or SVIs are correctly configured with IP addresses.
   ```bash
   Router# show ip interface brief
   ```
   or for a Layer 3 switch:
   ```bash
   Switch# show ip interface brief
   ```

2. **Test Connectivity**:
   From devices on different VLANs, test connectivity to the IP address of the other VLAN's gateway, and then to devices on other VLANs. You can use the `ping` command for this purpose.

3. **Show Routing Table**:
   Check the routing table to ensure routes to the VLANs exist.
   ```bash
   Router# show ip route
   ```
   or for a Layer 3 switch:
   ```bash
   Switch# show ip route
   ```

----------
### Configure Single-Area OSPF

1. **Enter Global Configuration Mode**:
   ```
   Router> enable
   Router# configure terminal
   Router(config)#
   ```

2. **Start OSPF Process**:
   You need to start an OSPF process and assign a unique process ID.
   ```bash
   Router(config)# router ospf 1
   ```

   Here, `1` is the OSPF process ID and can be any number. It is locally significant to the router.

3. **Configure OSPF Router ID** (optional but recommended):
   Define a router ID, which is a unique identifier for the OSPF process.
   ```bash
   Router(config-router)# router-id 1.1.1.1
   ```

   Choose an IP-address-like number that's easy to identify and remember. It doesn't have to be an actual IP address on the router, but it must be unique within the OSPF domain.

4. **Assign Interfaces to OSPF Area**:
   Go to each interface that you want to include in the OSPF process and assign it to an area. For a single-area OSPF, all interfaces are typically in area 0.
   ```bash
   Router(config)# interface GigabitEthernet0/0
   Router(config-if)# ip ospf 1 area 0
   Router(config-if)# exit

   Router(config)# interface GigabitEthernet0/1
   Router(config-if)# ip ospf 1 area 0
   Router(config-if)# exit
   ```

   Repeat this step for all interfaces that you want to include in the OSPF area.

5. **Save the Configuration**:
   ```bash
   Router(config)# end
   Router# write memory
   ```
   or
   ```bash
   Router# copy running-config startup-config
   ```

### Verify Single-Area OSPF

1. **Check OSPF Interface Configuration**:
   Verify that OSPF is enabled on the interfaces and they are assigned to the correct area.
   ```bash
   Router# show ip ospf interface
   ```

2. **Review OSPF Neighbor Relationships**:
   Check that OSPF neighbor relationships (adjacencies) have been established.
   ```bash
   Router# show ip ospf neighbor
   ```

   You should see a list of OSPF neighbors and their states. In a correctly functioning OSPF network, the state should be "Full" for neighbors on point-to-point and broadcast networks.

3. **Review OSPF Routes in the Routing Table**:
   Verify that the OSPF routes are present in the routing table.
   ```bash
   Router# show ip route ospf
   ```

   This command will show you all routes learned via OSPF. Look for routes marked with "O".

4. **Check the OSPF Database**:
   To get more detailed information about the OSPF topology.
   ```bash
   Router# show ip ospf database
   ```

5. **Test Connectivity**:
   Ensure there is connectivity between the devices in the OSPF network by using ping or traceroute between different networks.

----------


### Configure EtherChannel

1. **Enter Global Configuration Mode**:
   ```
   Switch> enable
   Switch# configure terminal
   Switch(config)#
   ```

2. **Select the Interfaces**:
   Choose the physical interfaces that you want to aggregate into an EtherChannel. Make sure that they are the same speed and duplex.

3. **Assign the Physical Interfaces to a Channel Group**:
   Configure the interfaces with the same channel-group number and specify the mode (`on`, `active`, or `passive`). For the purpose of this example, we'll use LACP (Link Aggregation Control Protocol), which means we'll use `active` or `passive` modes.
   ```bash
   Switch(config)# interface range GigabitEthernet0/1 - 2
   Switch(config-if-range)# channel-group 1 mode active
   Switch(config-if-range)# exit
   ```

   The `channel-group 1 mode active` command creates a port-channel with an ID of 1 and configures LACP to actively negotiate forming an EtherChannel.

4. **Configure the Port-Channel Interface**:
   By adding the interfaces to a channel-group, the logical port-channel interface is created automatically. You can now configure the port-channel interface as you would any other interface.
   ```bash
   Switch(config)# interface Port-channel1
   Switch(config-if)# switchport mode trunk
   Switch(config-if)# switchport trunk allowed vlan all
   Switch(config-if)# exit
   ```

   In this example, the EtherChannel is set up as a trunk and allowed to carry traffic for all VLANs.

5. **Save the Configuration**:
   ```bash
   Switch(config)# end
   Switch# write memory
   ```
   or
   ```bash
   Switch# copy running-config startup-config
   ```

### Verify EtherChannel

1. **Check Port-Channel and Member Ports**:
   Verify the EtherChannel configuration and check the status of the port-channel and its member ports.
   ```bash
   Switch# show etherchannel summary
   ```

   Look for the `Port-channel` in the output. The flag `P` indicates that the port is bundled in the port-channel, while `I` means it's stand-alone and not bundled.

2. **Verify Port-Channel Interface Status**:
   Check the status of the logical port-channel interface.
   ```bash
   Switch# show interfaces Port-channel1
   ```

   The output provides details about the port-channel, such as its protocol status and any configuration applied to it.

3. **Check Interface Configuration**:
   Verify that the individual interfaces have been configured correctly for the EtherChannel.
   ```bash
   Switch# show running-config interface GigabitEthernet0/1
   Switch# show running-config interface GigabitEthernet0/2
   ```

   Ensure that the interfaces have compatible configurations.

4. **Check for Errors or Misconfigurations**:
   Use the following command to check for common issues that can prevent EtherChannel from forming properly.
   ```bash
   Switch# show etherchannel port-channel
   ```

   This provides information about load-balancing and any misconfiguration on the EtherChannel.

5. **Test Connectivity**:
   Ensure there is connectivity across the EtherChannel link by using ping or other network tests. You should be able to see increased bandwidth and failover capabilities depending on your test methods and the number of links in the EtherChannel.

----------

### Configure IPv4 ACLs

1. **Enter Global Configuration Mode**:
   ```
   Router> enable
   Router# configure terminal
   Router(config)#
   ```

2. **Create a Numbered or Named ACL**:
   - For a numbered ACL (standard or extended), you choose a number:
     ```
     Router(config)# access-list [number] [permit|deny] [conditions]
     ```
   - For a named ACL (more descriptive), you use a name:
     ```
     Router(config)# ip access-list [standard|extended] [name]
     ```

3. **Add ACL Rules**:
   - For a standard ACL (filters by source IP only):
     ```
     Router(config)# access-list 10 permit 192.168.1.0 0.0.0.255
     Router(config)# access-list 10 deny any
     ```
   - For an extended ACL (filters by source and destination IP, protocol, port, etc.):
     ```
     Router(config)# ip access-list extended Sales-ACL
     Router(config-ext-nacl)# permit tcp 192.168.1.0 0.0.0.255 any eq 80
     Router(config-ext-nacl)# deny ip any any
     Router(config-ext-nacl)# exit
     ```

   The `permit tcp 192.168.1.0 0.0.0.255 any eq 80` command allows HTTP traffic from the 192.168.1.0/24 network to any destination. The `deny ip any any` command denies all other traffic.

4. **Apply the ACL to an Interface**:
   Go to the interface configuration mode and apply the ACL in the inbound or outbound direction.
   ```
   Router(config)# interface GigabitEthernet0/1
   Router(config-if)# ip access-group Sales-ACL in
   Router(config-if)# exit
   ```

   The `ip access-group Sales-ACL in` command applies the named ACL `Sales-ACL` to incoming traffic on the GigabitEthernet0/1 interface.

5. **Save the Configuration**:
   ```
   Router(config)# end
   Router# write memory
   ```
   or
   ```bash
   Router# copy running-config startup-config
   ```

### Verify IPv4 ACLs

1. **Show ACLs**:
   Verify the ACLs configured on the router.
   ```
   Router# show access-lists
   ```

   This command shows all ACLs on the router, including the rules and hit counts for each rule.

2. **Check Interface for ACLs**:
   Check which ACLs are applied to specific interfaces.
   ```
   Router# show ip interface GigabitEthernet0/1
   ```

   This command shows the ACLs applied to the interface GigabitEthernet0/1, including whether they are applied to inbound or outbound traffic.

3. **Verify ACL Functionality**:
   Test the ACLs to ensure they are filtering traffic as expected. You can use `ping`, `telnet`, or other traffic-generating methods from devices in the relevant source or destination networks.

4. **Debug and Logging** (if needed):
   If the ACL is not working as expected, use debugging and logging to troubleshoot.
   ```
   Router# debug ip packet
   Router# show logging
   ```

----------
### Configure Static NAT

1. **Enter Global Configuration Mode**:
   ```
   Router> enable
   Router# configure terminal
   Router(config)#
   ```

2. **Define the Inside and Outside Interfaces**:
   Identify which interfaces on your router connect to the inside (private) network and which connect to the outside (public) network. Then, mark these interfaces accordingly.
   ```bash
   Router(config)# interface GigabitEthernet0/0
   Router(config-if)# ip nat inside
   Router(config-if)# exit

   Router(config)# interface GigabitEthernet0/1
   Router(config-if)# ip nat outside
   Router(config-if)# exit
   ```

   Replace `GigabitEthernet0/0` and `GigabitEthernet0/1` with the actual interface names on your router.

3. **Create a Static NAT Entry**:
   Map the inside local address (private IP) to an inside global address (public IP).
   ```bash
   Router(config)# ip nat inside source static 192.168.1.10 203.0.113.10
   ```

   In this example, `192.168.1.10` is the private IP address of the internal host you want to make accessible, and `203.0.113.10` is the public IP address you are mapping to the private IP address.

4. **Save the Configuration**:
   ```bash
   Router(config)# end
   Router# write memory
   ```
   or
   ```bash
   Router# copy running-config startup-config
   ```

### Verify Static NAT

1. **Show Current Translations**:
   Verify that the static NAT translation entry is in the translation table.
   ```bash
   Router# show ip nat translations
   ```

   You should see an entry showing the inside local address mapped to the inside global address, indicating that the static NAT is properly configured.

2. **Test Connectivity**:
   From a host on an external network (such as the internet), attempt to connect to the public IP address (203.0.113.10 in the example above) using the appropriate protocol (e.g., HTTP, SSH). If static NAT is working, the connection should be forwarded to the internal private IP address (192.168.1.10).

3. **Clear NAT Translations**:
   If you are troubleshooting or need to clear the NAT translations for any reason, you can use the following command. Be cautious with this as it will temporarily disrupt any active NAT sessions.
   ```bash
   Router# clear ip nat translation *
   ```

4. **Check the Configuration**:
   To see the Static NAT configuration in the running configuration, use:
   ```bash
   Router# show running-config | include ip nat
   ```

----------
### Configure Dynamic NAT

1. **Enter Global Configuration Mode**:
   ```
   Router> enable
   Router# configure terminal
   Router(config)#
   ```

2. **Define Inside and Outside Interfaces**:
   Specify which interfaces on your router are connected to the inside (private) network and which are connected to the outside (public) network, then configure them accordingly.
   ```bash
   Router(config)# interface GigabitEthernet0/0
   Router(config-if)# ip nat inside
   Router(config-if)# exit

   Router(config)# interface GigabitEthernet0/1
   Router(config-if)# ip nat outside
   Router(config-if)# exit
   ```

3. **Create an Access Control List (ACL)**:
   Define an ACL that matches the traffic from the inside network that you want to translate.
   ```bash
   Router(config)# access-list 1 permit 192.168.1.0 0.0.0.255
   ```

4. **Create a NAT Pool**:
   Define a pool of public IP addresses that will be used for dynamic translation.
   ```bash
   Router(config)# ip nat pool NAT_POOL 203.0.113.1 203.0.113.10 netmask 255.255.255.0
   ```

   In this example, the NAT pool named `NAT_POOL` includes public IP addresses from `203.0.113.1` to `203.0.113.10` with a subnet mask of `255.255.255.0`.

5. **Bind the ACL to the NAT Pool**:
   Bind the ACL to the NAT pool to establish the dynamic NAT translation.
   ```bash
   Router(config)# ip nat inside source list 1 pool NAT_POOL
   ```

6. **Save the Configuration**:
   ```
   Router(config)# end
   Router# write memory
   ```
   or
   ```bash
   Router# copy running-config startup-config
   ```

### Configure PAT (NAT Overload)

If instead you want to configure PAT to map multiple private IP addresses to a single public IP address, you would use the following configuration, replacing the Dynamic NAT configuration at steps 4 and 5:

4. **Define a NAT Pool with a Single IP Address (for PAT)**:
   You only need one public IP address for PAT.
   ```bash
   Router(config)# ip nat pool NAT_POOL 203.0.113.1 203.0.113.1 netmask 255.255.255.0
   ```

5. **Bind the ACL to the NAT Pool with Overload**:
   Use the `overload` keyword to enable PAT.
   ```bash
   Router(config)# ip nat inside source list 1 pool NAT_POOL overload
   ```

### Verify Dynamic NAT and PAT

1. **Show Current NAT Translations**:
   Verify the NAT translations table to see the dynamic entries and any PAT translations.
   ```bash
   Router# show ip nat translations
   ```

   For PAT, you will see multiple inside local addresses (private IPs) being translated to the same inside global address (public IP) but with different port numbers.

2. **Show the NAT Statistics**:
   Check the usage and statistics of NAT translations.
   ```bash
   Router# show ip nat statistics
   ```

   This output includes information about the total number of active translations, hits, misses, and the pool of public IP addresses.

3. **Test Connectivity**:
   From an inside host, initiate traffic to an outside network (like the internet) and verify that the translation is working as expected.

4. **Clear NAT Translations (if needed for troubleshooting)**:
   Clear the dynamic entries in the NAT translation table.
   ```bash
   Router# clear ip nat translation *
   ```

5. **Check Access Control Lists and NAT Configuration**:
   To review the NAT configuration in the router's running configuration, including the ACLs and NAT

----------

### Configure NTP

1. **Enter Global Configuration Mode**:
   ```
   Router> enable
   Router# configure terminal
   Router(config)#
   ```

2. **Set the Timezone** (Optional but recommended):
   This step is important for logs and debugging.
   ```
   Router(config)# clock timezone [TZ] [offset]
   ```
   Replace `[TZ]` with your timezone abbreviation and `[offset]` with the offset from UTC (e.g., `Router(config)# clock timezone EST -5`).

3. **Configure the NTP Server**:
   Point your Cisco device to an NTP server. You can use the IP address or domain name of the server.
   ```
   Router(config)# ntp server [ntp-server-address]
   ```
   Replace `[ntp-server-address]` with the actual server address (e.g., `0.pool.ntp.org`). You can specify multiple NTP servers for redundancy.

4. **Set the NTP Client** (Optional):
   If you want your Cisco device to act as an NTP client and update its clock from an NTP server, use this command. It's usually enabled by default.
   ```
   Router(config)# ntp master
   ```

5. **Configure NTP Authentication** (Optional):
   If you use NTP servers that require authentication, set the authentication keys.
   ```
   Router(config)# ntp authentication-key [key-number] md5 [key]
   Router(config)# ntp trusted-key [key-number]
   Router(config)# ntp authenticate
   ```
   Replace `[key-number]` with the key identifier (a number) and `[key]` with the actual key.

6. **Save the Configuration**:
   ```
   Router(config)# end
   Router# write memory
   ```
   or
   ```bash
   Router# copy running-config startup-config
   ```

### Verify NTP

1. **Check NTP Associations**:
   To verify that your Cisco device has formed associations with the NTP servers, use:
   ```
   Router# show ntp associations
   ```

2. **Check NTP Status**:
   Check the status of the NTP peer and synchronization:
   ```
   Router# show ntp status
   ```

3. **Check the Device Clock**:
   To verify that the clock is set correctly, use:
   ```
   Router# show clock
   ```

4. **Check NTP Configurations**:
   Review the NTP configurations in the running configuration:
   ```
   Router# show running-config | include ntp
   ```

----------
### Configure System Message Logging

1. **Enter Global Configuration Mode**:
   ```
   Router> enable
   Router# configure terminal
   Router(config)#
   ```

2. **Set Syslog Logging Levels**:
   Define the severity level of messages to be logged. Levels range from 0 (emergencies) to 7 (debugging), where lower numbers represent higher severity.
   ```
   Router(config)# logging trap level
   ```
   Replace `level` with the desired logging level, for example:
   ```
   Router(config)# logging trap informational
   ```

3. **Enable Timestamps on Log Messages** (Optional but recommended):
   For better log tracking, enable timestamps on log messages:
   ```
   Router(config)# service timestamps log datetime msec localtime show-timezone
   ```
   
4. **Specify the Syslog Server** (if using remote logging):
   Send log messages to a remote syslog server by specifying its IP address.
   ```
   Router(config)# logging host [syslog-server-ip]
   ```
   Replace `[syslog-server-ip]` with the actual IP address of your syslog server.

5. **Configure Console Logging** (if desired):
   You can enable logging to the console, which can be useful for troubleshooting.
   ```
   Router(config)# logging console level
   ```
   Replace `level` with the desired severity level, similar to the `logging trap` command.

6. **Configure Terminal Line (vty) Logging** (if desired):
   For users connected via Telnet or SSH, you can enable logging for their sessions.
   ```
   Router(config)# line vty 0 4
   Router(config-line)# logging synchronous
   Router(config-line)# exit
   ```

7. **Enable Logging to the Device’s Buffer** (if desired):
   Store log messages in the device’s internal buffer.
   ```
   Router(config)# logging buffered level
   ```
   Replace `level` with the desired severity level, as before.

8. **Save the Configuration**:
   ```
   Router(config)# end
   Router# write memory
   ```
   or
   ```bash
   Router# copy running-config startup-config
   ```

### Verify System Message Logging

1. **Show Logging Configuration**:
   To display the logging configuration on the device:
   ```
   Router# show logging
   ```

2. **Check Syslog Messages**:
   View the syslog messages stored in the device’s buffer:
   ```
   Router# show logging buffered
   ```

3. **Verify Remote Logging**:
   If you have configured remote logging, verify that the syslog server is receiving logs from the Cisco device. This typically involves checking the syslog server directly.

4. **Check Console Logging**:
   If console logging is enabled, you should see log messages appear on the console as they occur.

5. **Test Syslog Functionality**:
   To test if syslog messages are being generated, you can perform an action that triggers a log message, such as enabling or disabling an interface, and then check the logs.

----------

### Configure Port Security

1. **Enter Global Configuration Mode**:
   ```
   Switch> enable
   Switch# configure terminal
   Switch(config)#
   ```

2. **Navigate to the Interface Configuration Mode**:
   Select the interface where you want to enable port security. This is typically done on access ports.
   ```
   Switch(config)# interface [interface-id]
   ```
   Replace `[interface-id]` with the actual interface identifier, such as `FastEthernet0/1`.

3. **Set the Interface as an Access Port**:
   ```
   Switch(config-if)# switchport mode access
   ```

4. **Enable Port Security**:
   ```
   Switch(config-if)# switchport port-security
   ```

5. **Set the Maximum Number of MAC Addresses**:
   Define the maximum number of MAC addresses allowed on the port (the default is 1).
   ```
   Switch(config-if)# switchport port-security maximum [number]
   ```
   Replace `[number]` with the maximum number of allowed MAC addresses.

6. **Specify a Static MAC Address** (Optional):
   Manually specify an allowed MAC address if needed. If not set, the switch dynamically learns the first MAC addresses up to the maximum number specified.
   ```
   Switch(config-if)# switchport port-security mac-address [mac-address]
   ```
   Replace `[mac-address]` with the actual hardware MAC address of the device you want to allow.

7. **Define the Violation Mode** (Optional):
   Choose the action the switch should take when a port security violation occurs. The options are `protect`, `restrict`, or `shutdown` (the default).
   ```
   Switch(config-if)# switchport port-security violation {protect | restrict | shutdown}
   ```

8. **Enable Sticky MAC Address Learning** (Optional):
   Make the dynamically learned MAC addresses sticky (persistent across reboots).
   ```
   Switch(config-if)# switchport port-security mac-address sticky
   ```

9. **Save the Configuration**:
   ```
   Switch(config-if)# end
   Switch# write memory
   ```
   or
   ```bash
   Switch# copy running-config startup-config
   ```

### Verify Port Security

1. **Check Port Security Settings**:
   Display the port security settings for the interface.
   ```
   Switch# show port-security interface [interface-id]
   ```
   Replace `[interface-id]` with the actual interface identifier.

2. **View Port Security Summary**:
   See a summary of port security for all interfaces.
   ```
   Switch# show port-security
   ```

3. **Check for Violations**:
   Display any security violations that have occurred.
   ```
   Switch# show port-security address
   ```
   This will list all learned MAC addresses and any violations.

4. **Verify Sticky MAC Addresses**:
   If sticky learning is enabled, verify the MAC addresses that have been added to the running configuration.
   ```
   Switch# show running-config interface [interface-id]
   ```
   You will see `switchport port-security mac-address sticky` followed by the learned MAC addresses.

----------

### Configure an Open Wireless Network (Cisco Access Point)

1. **Enter Global Configuration Mode**:
   ```
   AP> enable
   AP# configure terminal
   AP(config)#
   ```

2. **Define the Dot11 Radio Interface**:
   Navigate to the radio interface that you want to configure. This could be the 2.4 GHz (`0`) or 5 GHz (`1`) radio.
   ```
   AP(config)# interface dot11Radio0
   ```

3. **Configure the SSID**:
   Create an SSID for the open wireless network.
   ```
   AP(config-if)# ssid OPEN_NETWORK
   ```

4. **Set the SSID as a Guest Mode SSID**:
   This command broadcasts the SSID to make it visible to clients.
   ```
   AP(config-if)# guest-mode
   ```

5. **Return to Global Configuration Mode and Create a VLAN** (Optional):
   If you want to associate the SSID with a particular VLAN, create it (if it does not already exist).
   ```
   AP(config-if)# exit
   AP(config)# vlan [vlan-id]
   AP(config-vlan)# name [vlan-name]
   ```

6. **Bridge the SSID to the VLAN** (Optional):
   If using VLANs, associate the SSID with the VLAN.
   ```
   AP(config)# interface Dot11Radio0.[vlan-id]
   AP(config-subif)# encapsulation dot1Q [vlan-id]
   AP(config-subif)# bridge-group [vlan-id]
   ```

7. **Enable the Radio Interface**:
   Activate the radio interface.
   ```
   AP(config)# interface dot11Radio0
   AP(config-if)# no shutdown
   ```

8. **Configure the BSS for the Open Network**:
   Associate the BSS with the SSID and ensure no encryption is set.
   ```
   AP(config-if)# ssid OPEN_NETWORK
   AP(config-if-ssid)# authentication open
   AP(config-if-ssid)# exit
   ```

9. **Save the Configuration**:
   ```
   AP(config)# end
   AP# write memory
   ```
   or
   ```bash
   AP# copy running-config startup-config
   ```

### Verify the Open Wireless Network

1. **Show SSID Information**:
   To verify that the SSID is configured and broadcasting:
   ```
   AP# show dot11 bssid
   ```

2. **Check Interface Status**:
   Confirm that the radio interface is up and running.
   ```
   AP# show ip interface brief
   ```

3. **Test Connectivity**:
   Use a wireless client to search for available wireless networks. The SSID `OPEN_NETWORK` should appear in the list of available networks, and you should be able to connect to it without entering any password.

### Configure an Open Wireless Network (Cisco Wireless LAN Controller)

If you're using a Cisco Wireless LAN Controller (WLC), the process will involve creating a WLAN with an open security policy through the WLC's graphical user interface or command line. 

1. **Login to WLC**:
   Access the WLC web interface using its IP address or connect via SSH for CLI access.

2. **Navigate to WLAN Creation Page**:
   In the WLC interface, navigate to the WLANs section and create a new WLAN.

3. **Set WLAN Parameters**:
   Enter the SSID name, ID, and apply the appropriate settings for the WLAN. Ensure that the status is set to Enabled.

4. **Configure Security Settings**:
   Select 'None' or 'Open' for the Layer 2 Security policy. Do not configure any Layer 3 security settings or encryption.

5. **Save and Enable the WLAN**:
   Save the configuration and enable the WLAN.

----------

To configure a WLAN with WPA2 Personal (also known as WPA2-PSK for Pre-Shared Key) on a Cisco wireless device, you need to set up an SSID with WPA2 encryption and a pre-shared key. Here's how you can do this on a Cisco standalone Access Point (AP) and on a Cisco Wireless LAN Controller (WLC):

### Configure WPA2 PSK on a Cisco Standalone Access Point

1. **Enter Global Configuration Mode**:
   ```
   AP> enable
   AP# configure terminal
   AP(config)#
   ```

2. **Define the Dot11 Radio Interface**:
   Navigate to the radio interface configuration mode. Choose the appropriate radio interface (e.g., `dot11Radio0` for 2.4 GHz or `dot11Radio1` for 5 GHz).
   ```
   AP(config)# interface dot11Radio0
   ```

3. **Configure the SSID**:
   Create an SSID for your wireless network.
   ```
   AP(config-if)# ssid YOUR_SSID
   ```

4. **Set the Security Mode to WPA2**:
   Configure the SSID to use WPA2 with a pre-shared key.
   ```
   AP(config-if)# encryption mode ciphers aes-ccm
   AP(config-if)# authentication key-management wpa version 2
   AP(config-if)# guest-mode
   ```

5. **Specify the WPA2 Pre-Shared Key**:
   Define the pre-shared key that clients will use to connect to the wireless network.
   ```
   AP(config-if-ssid)# wpa-psk ascii YOUR_PSK
   ```

6. **Enable the Radio Interface and SSID**:
   Bring up the radio interface and SSID.
   ```
   AP(config-if-ssid)# exit
   AP(config-if)# no shutdown
   ```

7. **Save the Configuration**:
   ```
   AP(config)# end
   AP# write memory
   ```
   or
   ```bash
   AP# copy running-config startup-config
   ```

### Configure WPA2 PSK on a Cisco Wireless LAN Controller (WLC)

1. **Log into the WLC**:
   Access the WLC web interface using its IP address or connect via SSH for CLI access.

2. **Create or Edit a WLAN**:
   Go to the WLANs section and either create a new WLAN or edit an existing one.

3. **Set WLAN Parameters**:
   Configure the SSID and other parameters for the WLAN. Make sure the status is set to Enabled.

4. **Configure Security Settings**:
   Set the Layer 2 security to WPA+WPA2 and select 'WPA2 Policy'. Choose 'AES' as the WPA2 encryption method.

5. **Set the Pre-Shared Key**:
   Enter the pre-shared key for the PSK.

6. **Apply and Save the WLAN Configuration**:
   Save the settings to enable the WLAN with WPA2-PSK security.

### Verify WPA2 PSK Configuration

1. **Check SSID and Security Settings (Standalone AP)**:
   Display the SSID and security settings to verify the configuration.
   ```
   AP# show dot11 ssid YOUR_SSID
   ```

2. **Check SSID and Security Settings (WLC)**:
   On the WLC, navigate to the WLANs section and verify that the WLAN security settings are correct.

3. **Test Connectivity**:
   Use a wireless client to search for the SSID, connect to it using the pre-shared key, and ensure you have network connectivity.

----------

### Unprotected (Clear Text) Password

1. **Console Password**:
   ```
   Switch(config)# line console 0
   Switch(config-line)# password cisco
   Switch(config-line)# login
   ```

2. **Enable Password**:
   ```
   Switch(config)# enable password cisco
   ```

3. **VTY Password** (for Telnet/SSH access):
   ```
   Switch(config)# line vty 0 15
   Switch(config-line)# password cisco
   Switch(config-line)# login
   ```

### Protected (Encrypted) Password

1. **Enable Secret** (This password is automatically encrypted):
   ```
   Switch(config)# enable secret cisco
   ```
   The "enable secret" command uses a stronger MD5 hash by default compared to the "enable password" command.

2. **Encrypt All Plaintext Passwords**:
   To encrypt all current and future plaintext passwords in the configuration file, use the "service password-encryption" command:
   ```
   Switch(config)# service password-encryption
   ```
   This command applies a weak encryption (Type 7) to all clear text passwords. It's better than nothing, but it should not be considered highly secure as it can be easily decrypted.

3. **Username with Encrypted Password** (for login authentication):
   ```
   Switch(config)# username admin secret cisco
   ```
   When using the "secret" keyword, the password is automatically encrypted with a stronger hash (Type 5).

### Verifying the Password Configuration

You can verify the password configuration by viewing the running or startup configuration:

```
Switch# show running-config
Switch# show startup-config
```

You will see plaintext passwords if they are not encrypted, and for encrypted passwords, you will see a hash instead of the actual password.

### Important Security Note

Remember that the `service password-encryption` command only provides very basic protection and should not be solely relied upon for securing passwords. Also, the enable password is less secure than the enable secret, and if both are configured, the enable secret takes precedence.

For stronger security, it's recommended to use the enable secret for privileged exec access and configure local usernames with secrets for console and VTY access. Additionally, you should consider using AAA (Authentication, Authorization, and Accounting) with TACACS+ or RADIUS for more robust password management and security.

Always replace "cisco" with a strong, unique password in a real-world configuration to maintain network security. Never use "cisco" as an actual password, as it is commonly used as an example and would be extremely insecure.

----------
# Steps to configure SSH on a Router:

----------

To configure SSH on a Cisco router and access it from a PC, follow these general steps. Note that you should have basic knowledge of Cisco IOS and networking concepts before proceeding.

### 1. Set Hostname and Domain Name
You need to set a hostname and a domain name on the router to generate the RSA keys required for SSH.
```plaintext
Router> enable
Router# configure terminal
Router(config)# hostname MyRouter
MyRouter(config)# ip domain-name example.com
```

### 2. Generate RSA Keys
Generate the RSA key pair, which is used to encrypt and decrypt the SSH sessions.
```plaintext
MyRouter(config)# crypto key generate rsa
```
You will be asked to specify the size of the key; 1024 bits is commonly used, but 2048 bits is more secure.

### 3. Create a Local User
Create a username and password for SSH authentication.
```plaintext
MyRouter(config)# username admin secret my_secure_password
```
Replace `admin` with your preferred username and `my_secure_password` with a strong password.

### 4. Enable SSH and Set SSH Version (Optional)
Enable SSH on the router and (optionally) set the SSH version. Version 2 is more secure than version 1.
```plaintext
MyRouter(config)# ip ssh version 2
```

### 5. Configure the VTY Lines for SSH
Configure the VTY (Virtual Terminal Lines) to only accept SSH connections.
```plaintext
MyRouter(config)# line vty 0 15
MyRouter(config-line)# transport input ssh
MyRouter(config-line)# login local
MyRouter(config-line)# exit
```

### 6. Set an Access Control List (Optional)
To improve security, you can restrict which IP addresses are allowed to SSH into the router.
```plaintext
MyRouter(config)# access-list 101 permit tcp any host 192.168.1.1 eq 22
MyRouter(config)# line vty 0 15
MyRouter(config-line)# access-class 101 in
MyRouter(config-line)# end
```
Replace `192.168.1.1` with your router's IP address.

### 7. Save Configuration
Save the configuration to ensure that it persists after a reboot.
```plaintext
MyRouter# write memory
or
MyRouter# copy running-config startup-config
```

### Access the Router from a PC

#### Using SSH Client (Windows - PuTTY / Linux - OpenSSH)

**For Windows:**

1. Download and install PuTTY if you haven't already.
2. Open PuTTY and enter the IP address of the router.
3. Select 'SSH' as the connection type.
4. Click 'Open' to initiate the SSH connection.
5. Enter the username and password you configured on the router when prompted.

**For Linux:**

1. Open a terminal.
2. Use the `ssh` command to connect to the router:
```plaintext
ssh admin@192.168.1.1
```
Replace `admin` with the username you set up and `192.168.1.1` with the IP address of your router.

3. Accept the security prompt for the RSA key fingerprint if it appears.
4. Enter the password when prompted.

After following these steps, you should be connected to your Cisco router over SSH from your PC. If you encounter any issues, double-check the configuration on the router, ensure the PC is on the same network as the router, and that no firewall settings are blocking the SSH connection.

----------

