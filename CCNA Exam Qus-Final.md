From a network perspective, how is a server a different endpoint than a user workstation?

* A server requires lower latency.

* **A server requires more bandwidth. (Ans)**

* A server requires Power over Ethernet (PoE) connectivity.

* A server requires stricter network access control.
--------
Which network topology layer does a wireless access point (WAP) belong to?

* **access**

* collapsed core

* core

* distribution

	Answer
	The correct answer is **access**. Access points connect client devices such as laptops and cameras, which makes them a part of the access layer. The core, collapsed core, and distribution layers are not intended for connection of network devices of this type.
--------
What is the role of a router?

* to connect departmental devices

* **to connect network segments (Ans)**

* to provide wireless network access

* to secure the edge network
--------
HQ# show ip route
	<... output omitted ...>

	Gateway of last resort is not set

	      172.16.0.0/16 is variably subnetted, 2 subnets, 2 masks
	C        172.16.1.0/30 is directly connected, Ethernet0/0
	L        172.16.1.1/32 is directly connected, Ethernet0/0
	D     192.168.0.0/24 [90/409600] via 172.16.1.2, 00:03:52, Ethernet0/0
	D     192.168.16.0/23 [90/307200] via 172.16.1.2, 00:03:52, Ethernet0/0
	D EX  192.168.18.0/24 [170/307200] via 172.16.1.2, 00:03:52, Ethernet0/0
	S     192.168.150.0/24 [1/0] via 172.16.1.2
	
	Refer to the exhibit. What is the metric of the route pointing to the 192.168.18.0/24 network?

* 90

* 170

* **307200**

* 409600

	Answer
	The correct answer is **307200**. Each route in the routing table, apart from directly connected and local ones, has two numeric values: administrative distance and metric. They are written in square brackets and separated with a slash symbol. The route to 192.168.18.0/24 network **has an administrative distance of 170 and a metric value of 307200**.
--------
What are two characteristics of a **pre-shared key wireless implementation**? (Choose two.)

* Access control is centralized.

* An authentication server is required.

* **Encryption uses an optional Advanced Encryption Standard (AES).**

* **Encryption uses the Temporal Key Integrity Protocol (TKIP).**

* The authentication key is rotated automatically.

	Answer
	The correct answers are **Encryption uses an optional Advanced Encryption Standard (AES) and Encryption uses the Temporal Key Integrity Protocol (TKIP)**. TKIP uses a suite of algorithms surrounding Wired Equivalent Privacy (WEP) and Wi-Fi Protected Access (WPA) to enhance its security. AES allows for longer keys and is used for most WLAN security solutions. TKIP and AES are both used in the Personal mode of wireless protected access.
--------
What are two reasons for choosing Transport Layer Security (TLS) over IP Security (IPsec) encryption? (Choose two.)

* IPsec encrypts the IP packet, resulting in lesser application-level security.

* IPsec is less efficient than TLS, and in general not supported on mobile devices.

* **IPsec requires dedicated software installed on client hosts.**

* **TLS can be used for encrypting traffic to public websites.**

* TLS decryption can be easily accelerated in hardware.

	Answer
	The correct answers are **IPsec requires dedicated software installed on client hosts and TLS can be used for encrypting traffic to public websites**. IPsec can encrypt the entire IP packet, while TLS encrypts only the application level data, which makes IPsec a more flexible choice for a broader range of applications. However, IPsec requires a software client installed, as well as a specific configuration on the VPN server, which makes it a worse choice than TLS to encrypt traffic to resources external to the organization. TLS needs only the browser.
--------
Devices in the IT department are pre-configured.

Router R2 is a DHCP server and provides IP addresses to multiple network segments in Department A.

End clients in department A need to be configured so that they receive all relevant network configuration through DHCP. However, router R1 is not yet configured to facilitate this operation.

Perform the following tasks:

Configure router R1 so that the PC1 and PC2 hosts get DHCP information from router R2.

Ensure that both PC1 and PC2 hosts get their addresses via DHCP.

What is the default gateway that PC1 has received through DHCP?

* 10.10.1.1

* **10.10.1.53**

* 10.10.1.100

* 10.10.1.254

	Answer
	The correct answer is **10.10.1.53**. In real networks, **the gateway address is usually either the first or the last assignable IP address of the subnet.**


What is the lease time for the assigned IP address on PC2?

* 1 second

* **1 minute (Ans)**

* 1 hour

* 1 day

What is the IPv4 address of the DNS server assigned by DHCP to PC1?

* 10.10.1.1

* 198.51.100.1

* 203.0.113.1

* **203.0.113.30**

	Answer
	The correct answer is **203.0.113.30**. The DNS server resides on SRV2, which has an IP address of 203.0.113.30.
--------
Which language is used in the Cisco Network Services Orchestrator (NSO) to describe the network service intent?

* Python

* XML

* YAML

* **YANG**

	Answer
	The correct answer is YANG. Network services and network devices are modeled in the Cisco NSO using YANG. XML is used in configuration templates to map the service intent to the actual device configurations, whereas Python is used to code any additional service logic.
--------
Which **mechanism** allows an end user to **make a request** of a network device and receive an answer from that device?

* **application programming interface (API) (Ans)**

* Cisco Discovery Protocol

* routing protocol

* syslog protocol
--------
Refer to the exhibit. The service provider is implementing **Multiprotocol Label Switching Virtual Private Network (MPLS VPN) service**. Which two options indicate the specific VPN type that is implemented and how the service provider appears from the perspective of the customer? (Choose two.)

* The service provider is implementing MPLS L2VPN.

* **The service provider is implementing MPLS L3VPN. (Ans)**

* The service provider is implementing MPLS VPLS.

* **The service provider network can be represented as a router from the customer perspective. (Ans)**

* The service provider network can be represented as a switch from the customer perspective.
--------
Refer to the exhibit. Which two options are common IPsec or SSL VPN implementations? (Choose two.)

* **option 1**

* option 2

* option 3

* option 4

* **option 5**

	Answer
	The correct answers are option 1 and option 5. An IPsec Tunnel VPN is typically established between two network devices, connecting two or more remote networks. An SSL VPN is typically established between a client and a network device. DMVPN and IPsec VTI VPN are typically established between network devices.
--------
Which two types of cables can be used to connect to the console port of a Cisco router? (Choose two.)

* crossover

* **rollover**

* serial

* straight-through

* **USB**

	Answer
	The correct answers are **rollover and USB**. Cisco devices traditionally used rollover cables to connect to the console port. Today, Cisco devices also offer a USB mini console port on the device. Crossover, straight-through, and serial cables are used to interconnect devices.
--------
Which type of cable is typically used to connect a core switch with a data center switch, where bandwidth higher than 40 Gbps and low cost are required?

* Category 5e UTP

* Category 6 UTP

* **multimode fiber (Ans)**

* single-mode fiber
--------
Which three fields are included in a TCP header? (Choose three.)

* destination address

* **destination port**

* **flags**

* frame check sequence

* **window size**

	Answer
	The correct answers are **destination port, flags, and window size**. The destination port is the sequence of the called port (16 bits), window size is the sequence of the data amount the destination can accept (16 bits), and flags are control bits (9 bits). The destination address field is included in Ethernet and IP headers. Frame check sequence is a field in an Ethernet header.
--------
In which situation would you choose to use UDP instead of TCP for IP applications?

* when ensuring accurate file transfers even in the face of network issues

* when ensuring packet headers are not changed during transmission from source to destination

* **when speed of delivery is more important than error correction in IP packet transmissions (Ans)**

* when you require that the recipient of the packets verify that the packets are delivered
--------
Which group of devices in a network receive IPv6 packets with the destination address of ff05::2?

* all IPv6 nodes on all the network segments within a site

* all IPv6 nodes on the local network segments

* **all IPv6 routers on all the network segments within a site**

* all IPv6 routers on the local network segments

* all OSPFv3 routers on all the network segments within a site

* all OSPFv3 routers on the local network segments

	Answer
	The correct answer is **all IPv6 routers on all the network segments within a site**. The hexadecimal digits **“ff”** in the IPv6 address **prefix are an indication of a multicast address.** The **fourth hexadecimal digit indicates the scope**, with the number **five representing a site-local scope**. The **group ID of ::2 represents all IPv6 routers**.
--------
An enterprise wants to provide a global service that would be provided from an enterprise resource nearest to the user. For which three reasons does the **enterprise choose to assign anycast IPv6 addresses** to the relevant devices? (Choose three.)

* Because all the devices configured with the IPv6 anycast address would be aware of the user session.

* **Because IPv6 anycast addresses are globally routable.**

* Because routing of IPv6 anycast addresses is more secure than routing other IPv6 address types.

* **Because routing tables will point to the nearest resource configured with the IPv6 anycast address.**

* **Because using IPv6 anycast addresses provides automatic failover.**

	Answer
	The correct answers are **Because IPv6 anycast addresses are globally routable**, Because routing tables will point to the nearest resource configured with the IPv6 anycast address, and Because using IPv6 anycast addresses provides automatic failover. The nearest resource provides a service to the user; other resources, which are equally capable of providing the service, are not involved. Routing information exchange is no more or less secure for anycast IPv6 addresses than it is for other IPv6 address types.
--------
What is the default VLAN of a port on a Cisco switch?

* VLAN 0

* **VLAN 1 (Ans)**

* VLAN 2

* VLAN 4
--------
Which three commands should you use to configure data and voice VLAN on the same interface? (Choose three.)

* **Switch(config-if)# switchport access vlan 2**

* Switch(config-if)# switchport data vlan 2

* **Switch(config-if)# switchport mode access**

* Switch(config-if)# switchport mode trunk

* Switch(config-if)# switchport trunk allowed vlan 2,3

* **Switch(config-if)# switchport voice vlan 3**

	Answer
	The correct answers are Switch(config-if)# switchport access vlan 2, Switch(config-if)# switchport mode access, and Switch(config-if)# switchport voice vlan 3. When connecting a host to a switch port, you can use the switchport access vlan vlan-id command to assign an interface to a VLAN. To simplify the troubleshooting process, IP phones are often placed into a "voice VLAN." Even though we create a separate logical segment, the port mode is not changed to trunk.
--------
Which component is used to generate a signal for **single-mode fiber connections**?

* cathode

* **laser transmitter (Ans)**

* LED diode

* oscillator
--------
Which three types of devices are typically connected to access switches in an enterprise network? (Choose three.)

* **desktops (Ans)**

* firewalls

* **printers (Ans)**

* **IP phones (Ans)**

* routers
--------
In the Wi-Fi 2.4 GHz band, which three channels do not overlap? (Choose three.)


* 0

* **1**

* 2

* **6**

* **11**

* 15

* 21

	Answer
	The correct answers are **1, 6, and 11.** In the United States and in Europe, the nonoverlapping channels are 1, 6, and 11. In Japan, channel 14 is also nonoverlapping.
--------
Which statement about Service Set Identifiers (SSIDs) is true?

* An administrator can only create one SSID on the same access point.

* **An administrator can create several SSIDs on the same access point.**

* An SSID must be advertised by the Wi-Fi access point.

* An SSID is configured by default on an access point.

	Answer
	The correct answer is **An administrator can create several SSIDs on the same access point**. An SSID is not configured by default. An administrator configures one or more SSIDs on an access point. The administrator can also decide to hide an SSID.
--------
What are two examples of **full hypervisors**? (Choose two.)

* Docker

* DOSBox

* Kubernetes

* **type-1 (Ans)**

* **type-2 (Ans)**
--------
Which two of the following protocols does the **distribution layer use to provide default gateway redundancy**? (Choose two.)

* Device Control Protocol (DCP)

* Distributed Network Protocol (DNP3)

* Dynamic Source Routing Protocol (DSR)

* **First Hop Redundancy Protocol (FHRP)**

* **Hot Standby Router Protocol (HSRP)**

	Answer
	The correct answers are **First Hop Redundancy Protocol (FHRP) and Hot Standby Router Protocol (HSRP)**. FHRP and HSRP are designated to allow two or more routers to take the role of the default gateway in the network. DCP is designed for integration, monitoring and controlling of devices in the network. DSR is a routing protocol for wireless mesh networks. DNP3 is a set of open source protocols, developed for communication mainly in equipment used by utilities such as electric and water companies.
--------
Which command is used to **verify a default gateway** configuration on a Layer 2 switch?

* **show interface description**

* show interface stats

* show ip default-gateway network

* show management

* **show running-config**

	Answer
	The correct answers is **show running-config**. The **show interface description** command displays the interface protocol status and the interface description. The **show interface stats** command displays interface statistics. The **show management** command displays the management applications.
--------
Refer to the exhibit. PC_A wants to communicate with PC_B, which resides on a different network. The hosts are connected via a router that acts as the default gateway for both. The ARP tables on all three devices are empty. When PC_A sends the first frame, which two things happen in the process? (Choose two.)

* PC_A broadcasts the frame intended for PC_B.

* **PC_A sends a broadcast ARP request looking for the MAC address of the router**.

* **The router adds an IPv4 address to the MAC address's mapping for PC_A to its ARP table**.

* The router drops the packet after checking for the mapping of PC_B's IP address.

* The router receives a frame with its own MAC and mismatched IP address, and drops it.

	Answer
	The correct answers are **PC_A sends a broadcast ARP request looking for the MAC address of the router and The router adds an IPv4 to the MAC address's mapping for PC_A to its ARP table**. Since PC_A does not have a destination MAC address for the IP address of host B, it first acquires this information using ARP. The ARP request is broadcast, and the router and all other devices on the same network segment receive the ARP request. Only the router responds to it with its own MAC address.
--------
The network switches must be configured to separate workstations and servers into different VLANs as displayed in the topology. To ensure inter-VLAN connectivity, router R1 is already pre-configured.

Ensure that the devices in one VLAN can communicate with each other. Perform the following tasks:

Configure IPv4 addressing on workstations and servers so that they belong to the appropriate subnet.

Configure the default gateway IPv4 address on workstations and servers.

Configure VLANs and trunking.

Do not change the default configuration on the Ethernet0/3 interface on SW2.

When configuring devices and verifying device configurations, use the information provided in the documentation, that is in the topology figure and Job Aids.


When you examine the MAC address table on SW2, which VLAN does MAC aa-aa-aa-aa-22-22 belong to?

* 1

* **65 (Ans)**

* 80

* 1001

* 1005


On SW2, verify the administrative and operational switching modes on interface Ethernet0/3. Which statement correctly describes the administrative mode and operational mode values?

* Administrative mode is access and operational mode is access.

* Administrative mode is dynamic-auto and operational mode is access.

* Administrative mode is dynamic-desirable and operational mode is access.

* **Administrative mode is dynamic-desirable and operational mode is trunk.**

* Administrative mode is trunk and operational mode is trunk.

	Answer
	The correct answer is **Administrative mode is dynamic-desirable and operational mode is trunk**. Administrative mode displays what you have configured on the interface. Operational mode displays the actual status of the interface. **When manually configuring access or trunking, administrative and operational mode have identical values.** When you configure Dynamic Trunking Protocol (DTP) to negotiate switching status, administrative and operational mode differ. Cisco recommends disabling DTP on a switch."


Examine the topology and the configuration. On PC2, when you use the ping command to check connectivity to Server 1, what is the order of the devices that packets traverse?

* PC2 > SW1 > SW2 > R1 > SW2 > Server1

* PC2 > SW2 > R1 > SW1 > Server1

* PC2 > SW2 > SW1 > R1 > Server1

* **PC2 > SW2 > SW1 > R1 > SW1 > Server1**


Which interfaces on SW1 are trunk interfaces?

* E0/0 and E0/1

* **E0/0 and E0/3**

* E0/1 and E0/2

* E0/1 and E0/3

	Answer
	The correct answer is **E0/0 and E0/3**. SW1 has four interfaces. The interfaces E0/0 and E0/3 are connected to a router and another switch, respectively. As such, **those two interfaces are set up as trunk interfaces in order to carry multiple VLANs.** The interfaces E0/1 and E0/2 are connected to end nodes, and are configured as access interfaces.
--------
Which three IPv4 addresses are private? (Choose three.)

* **10.255.255.254**

* **172.31.255.254**

* 172.32.255.254

* **192.168.1.100**

* 192.169.1.100

	Answer
	The correct answers are **10.255.255.254, 172.31.255.254, and 192.168.1.100**. These ranges of IP addresses are **private: 10.0.0.0 to 10.255.255.255, 172.16.0.0 to 172.31.255.255, and 192.168.0.0 to 192.168.255.255**. Addresses in these ranges are not routed on the internet backbone.
--------
Which Windows Command Prompt command do you use to view the IP address of a host?

* ip address

* ifconfig

* **ipconfig (Ans)**

* show ip address
--------
Which two symptoms are characteristic of a duplex mismatch? (Choose two.)

* The full-duplex side of the link will experience increased collision rates.

* **The half-duplex side of the link will experience increased collision rates**.

* TCP data transfer will perform better than UDP data transfer.

* The connection will not be operational.

* **The full-duplex side of the link will have a large number of CRC errors.**

	Answer
	The correct answers are **The half-duplex side of the link will experience increased collision rates and The full-duplex side of the link will have a large number of CRC errors**. The full-duplex side of the link does not detect any collisions, since Carrier Sense Multiple Access with Collision Detection (CSMA/CD) is disabled on the full-duplex side of the link. The connections with a duplex mismatch are typically operational, but they operate poorly. When used to send a larger amount of data, the TCP data transfer would provoke collisions and trigger TCP retransmissions, which slows down the transfer.
--------
You are tasked with installing and configuring a new PoE-supported IP camera with a power consumption of 20 W. After connecting it to a PoE-enabled switch, the camera does not turn on. What is the likely cause of the problem?

* The cable connecting the switch and the camera is too long.

* The camera requires additional configuration to work with PoE.

* **The switch does not support the PoE Plus standard.**

* The switch requires additional configuration to enable PoE on the interface.

	Answer
	The correct answer is **The switch does not support the PoE Plus standard**. Normal PoE can only provide up to 15.4 W of power, while PoE Plus provides up to 30 W. Devices that support PoE do not need to be configured to use it, as they will power on when connected to the Ethernet. PoE is enabled on all ports. Supplied PoE power decreases with range, but the drop is minimal.
--------
Which type of Cisco **switch memory location stores the MAC address table**?

* **content-addressable memory (CAM) (Ans)**

* flash

* non-volatile random-access memory (NVRAM)

* read-only memory (ROM)
--------
Which two symptoms indicate a **duplex mismatch between a client and an Ethernet switch**? (Choose two.)

* Auto-negotiation will report speed and duplex mismatch errors on the client NIC interface.

* Interface statistics for the full-duplex side of the link will show increasing late collision errors.

* **The full-duplex interface will report increasing numbers of FCS errors or runts on the port**.

* The full-duplex side of the link will slow as CSMA/CD will force it to wait for incoming packets from the other side of the link.

* **The half-duplex side of the link will waste bandwidth due to increased packet retransmissions caused by increasing collisions**.

	Answer
	The correct answers are **The full-duplex interface will report increasing numbers of FCS errors or runts on the port and The half-duplex side of the link will waste bandwidth due to increased packet retransmissions caused by increasing collisions**. Interfaces that operate in full-duplex transmission mode have CSMA/CD disabled and do not detect collisions. Auto-negotiation is usually set when connecting client-end devices, but it would not report the issue, which makes troubleshooting harder.
--------
Which is the correct subnet mask for a host route?

* 0.0.0.0

* 255.254.0.0

* 255.255.255.254

* **255.255.255.255 (Ans)**
--------
Which command would you use to configure a floating static route?

* ip route static 192.168.13.0 255.255.255.0 100

* **ip route 192.168.13.0 255.255.255.0 172.17.10.1 100 (Ans)**

* ip route 192.168.13.0 255.255.255.0 172.17.10.1

* ip route 192.168.13.0 255.255.255.0 172.17.10.1 metric 100
--------
Which of the following is the correct binary representation of the third octet of the IPv4 address 172.20.**170**.50?

* 0001 1110

* 0110 0110

* **1010 1010 (Ans)**

* 1100 1011
--------
Two computers are connected to a Cisco Catalyst Layer 2 switch. PC1 is assigned the address 10.250.20.20/26 and PC2 is assigned the address 10.250.20.50/26. When a user on PC1 issues the ping 10.250.20.63 command, will PC2 respond to it?

* No, because 10.250.20.63 is not in the subnet that PC1 belongs to.

* No, because 10.250.20.63 is not the IP of PC2.

* **Yes, the PC2 will respond to the 10.250.20.63 broadcast if both ports are operationally in access mode and the same VLAN.**

* Yes, if the ip routing command is configured on the switch.

	Answer
	The correct answer is **Yes, the PC2 will respond to the 10.250.20.63 broadcast if both ports are operationally in access mode and the same VLAN**. The IPv4 address 10.250.20.63 is the broadcast address of the 10.250.20.0/26 subnet. A switch forward broadcast communication to all ports in a VLAN. If both ports that connect PC1 and PC2 belong to the same VLAN, then PC2 as well as other devices in the same subnet will receive the ICMP request from PC1 and respond to it.
--------
Which statement regarding **online and offline password attacks is true**?

* **Offline attacks are more dangerous because there is no external authentication system.**

* Offline attacks are more dangerous because they target out-of-band management assets.

* Online attacks are more dangerous because distributed sources can deliver them.

* Online attacks are more dangerous because they can target resources connected on the network.

	Answer
	The correct answer is **Offline attacks are more dangerous because there is no external authentication system.** In an online attack, the password has the protection of the system in which it is stored, but there is no such protection in offline attacks. In an offline attack, the attacker captures the password hash or the encrypted form of the password. The attacker can then make countless attempts to crack the password without being noticed.
--------
What are two differences between the RADIUS and TACACS+ protocols? (Choose two.)

* **RADIUS combines authentication and authorization, while TACACS+ implements two separate processes.**

* RADIUS encrypts the entire payload, while TACACS+ encrypts only the password.

* RADIUS is a TCP-based protocol, while TACACS+ is a UDP-based protocol.

* **RADIUS is a UDP based protocol. TACACS+ is a TCP based protocol.**

* RADIUS supports bidirectional authentication, while TACACS+ supports only unidirectional authentication.

	Answer
	The correct answers are **RADIUS combines authentication and authorization, while TACACS+ implements two separate processes and RADIUS is a UDP based protocol.** TACACS+ is a TCP based protocol. RADIUS is an open standard that combines authentication and authorization services into a single process. TACACS+ is a Cisco proprietary security mechanism that can be used only for authorization and accounting while using another method of authentication. TACACS+ uses the Transmission Control Protocol (TCP) for all three services.
--------
Which feature of **PVST+ is not available in RSTP**?

* fast convergence on topology changes

* per-port STP

* **per-VLAN STP instance (Ans)**

* edge ports
--------
In Cisco **PVST+, how many root ports per VLAN are allowed on a device**?

* **1**

* 8

* 24

* 32

	Answer
	The correct answer is 1. This port exists on non-root bridges. **Only one root port is allowed per switch or per VLAN in Cisco PVST+.** The root port forwards traffic toward the root bridge.
--------
The lab is prepared with the devices that are represented in the topology diagram. All devices have their basic configurations in place, including host names and IPv4 addresses. The SRV2 server is a DNS server for both departments. The domain names of the devices are equal to their host names. Note that static routing is implemented between the routers to ensure connectivity between the network segments.

Perform the following tasks:

On R1, the IP standard access list 10 is already configured. Implement the IP standard access list 10 on the R1 Ethernet0/3 interface by applying it in the outbound direction.

On PC1, change the IP address on Ethernet 0/0 to 10.10.1.11/24.

On R1 Ethernet 0/1, configure an access list to deny Telnet and permit ping from SRV1 to SRV2. Apply the access list to the Ethernet 0/1 interface.


Which line in the preconfigured access list 10 on router R1 will cause the ping connectivity test from PC1 to SRV2 (203.0.113.30) to fail?

* access-list 10 deny 10.0.0.0 0.255.255.255

* **access-list 10 deny 10.10.1.0 0.0.0.255 (Ans)** Note: ACL uses Wildcard masks that is opposite of the IP.

* access-list 10 deny any

* implicit deny


You want to deny Telnet and permit ping from SRV1 to SRV2. The access list 101 will be used and you have already prepared two access list given below. The access list will be applied in the inbound direction on the R1 Ethernet 0/1 interface. Which statement describes the correct configuration?

access-list 101 deny tcp host 10.10.2.20 host 203.0.113.30 eq telnet
access-list 101 permit icmp host 10.10.2.20 host 203.0.113.30

* The deny any any statement should be added at the end of the access list.

* **The order of the two prepared statements is not important. (Ans)**

* The prepared permit statement must be placed before the deny statement.

* The prepared deny statement must be placed before the permit statement.


If you change the IP address on the PC1 Ethernet0/0 interface to 10.10.2.10/24, what will happen with the ping connectivity test from PC1 to SRV2?

* The ping will fail because access list 10 is configured on R1 and is denying packets from 10.10.0.0/16.

* The ping will fail because access list 10 is configured on R1 and is implicitly denying all packets not matched.

* The ping will fail because PC1 and R1 are not in the same subnet, and R1 will not return the echo-reply packet.

* **The ping will fail because PC1 and R1 are not in the same subnet, and PC1 will not send the echo-request packet due to ARP resolution failure.**

	Answer
	The correct answer is **The ping will fail because PC1 and R1 are not in the same subnet, and PC1 will not send the echo-request packet due to ARP resolution failure.** In order for the PC1 to generate and send the ICMP echo-request packet it needs to get the MAC address of the default gateway. The R1 will reject the ARP request as it is sourced from another subnet (10.10.2.0/24). PC1#debug arp  ARP packet debugging is on PC1#ping 203.0.113.30 Type escape sequence to abort. Sending 5, 100-byte ICMP Echos to 203.0.113.30, timeout is 2 seconds: IP ARP: creating incomplete entry for IP address: 10.10.1.1 interface Ethernet0/0 IP ARP: sent req src 10.10.2.10 aabb.cc00.1a00,                  dst 10.10.1.1 0000.0000.0000 Ethernet0/0 <output omitted> PC1#show arp Protocol  Address          Age (min)  Hardware Addr   Type   Interface Internet  10.10.1.1               0   Incomplete      ARPA   Internet  10.10.2.10              -   aabb.cc00.1a00  ARPA   Ethernet0/0 R1#debug arp ARP packet debugging is on R1# IP ARP req filtered src 10.10.2.10 aabb.cc00.1a00, dst 10.10.1.1 0000.0000.0000 wrong cable, interface Ethernet0/0


Which Cisco IOS command displays the sequence numbers of the statements in the access list?

* show ip access-group

* **show ip access-lists (Ans)**

* show running-config

* show running-config all


Which command should you use to access SRV1 from SRV2 using Telnet?

* telnet 10.10.2.20 23

* telnet 10.10.2.20 2323

* telnet 198.51.100.2 23

* telnet 198.51.100.2 2323

	Answer
	The correct answer is telnet **198.51.100.2 2323**. The private address 10.10.2.20 is not reachable from SRV2. The public IP address 198.51.100.2 is configured on R1 Ethernet0/3. R1 Ethernet0/3 is reachable from SRV2, but you should not use Telnet to connect to R1. **The port forwarding or static NAT translation on R1 translates IP 198.51.100.2 port 2323 into IP 10.10.2.20 and port 23.**


When you use Telnet to connect from SRV2 to the IP 198.51.100.2 and port 2323, what message should you get?

* % Connection refused by remote host

* Password required, but none set

* **Welcome!**

* Please log in!

	Answer
	The correct answer is **Welcome!** The Telnet connection from SRV2 to the IP 198.51.100.2 and port 2323 is translated on R1 into the SRV2 IP 10.10.2.20 and port 23. You should be successfully connected from SRV2 to SRV1, and you should see the MOTD message configured on SRV1.


On PC1, issue the ping command to verify connectivity to SRV2. What is the result that you see?

* .....

* **U.U.U**

* !.!.!

* !!!!!

	Answer
	The correct answer is **U.U.U**. There is an access list configured on the SRV2 Ethernet0/0 interface that only permits ICMP packets from 209.165.202.128/27. Based on the R1 configuration, the PC1 IP is translated into R1 Ethernet0/3 (198.51.100.2), and this is why the ping is denied by the SRV2 Ethernet0/0 access list.


Examine the routing table on R2. What does the subnet 209.165.202.128/27 in the static entry refer to?

* **SRV1 to R1 public segment**

* R1 to R2 public segment

* R2 to SRV2 public segment

* SRV1 to R1 private segment

	Answer
	The correct answer is **SRV1 to R1 public segment**. The traffic from the 10.10.2.0/24 subnet is dynamically translated into the pool of public addresses 209.165.202.128/27.
--------
Refer to the exhibit. You must ensure full connectivity in the network. When configuring trunking on SW3, which configuration would you use?

Ans:
	SW3(config)# interface range GigabitEthernet0/1-2
	SW3(config-if-range)# switchport mode trunk
	SW3(config-if-range)# switchport trunk allowed vlan 10,20,30
	SW3(config-if-range)# switchport trunk native vlan 39
	SW3(config-if-range)# end
	SW3# configure terminal
	SW3(config)# vlan 10,20,30
	SW3(config-vlan)# end
--------
On a Cisco device, what is the **default destination for syslog logging** messages?

* **console line (Ans)**

* logging buffer

* syslog server

* terminal lines
--------
Which three SNMP messages are sent from an SNMP agent to an SNMP manager? (Choose three.)

* GetRequest

* GetNextRequest

* **InformRequest**

* **Response**

* SetRequest

* **Trap**

	Answer
	The correct answers are **InformRequest, Response, and Trap**. GetRequest, GetNextRequest and SetRequest are SNMP messages that an SNMP manager sends to an SNMP agent.
--------
Which two Microsoft Windows commands will display the **DNS server address configured** on the host? (Choose two.)

* ipconfig

* **ipconfig /all**

* net config

* netstat -f

* **nslookup**

	Answer
	The correct answers are **ipconfig /all and nslookup**. The letters **"ns" are usually used to indicate the name server service** in the network. The nslookup command is used for querying the configured DNS server to obtain domain name, IP address mapping, or other DNS records. The ipconfig command provides only basic information that does not include DNS server addresses. The net config command can be used to verify configuration or configure server and workstation services. The netstat -f command displays network statistics.
--------
A client issues a DNS request to its local DNS server. The local DNS server does not have the information required. Which entity will finally send a DNS response to the client?

* the authoritative DNS server for the top-level domain

* the authoritative top-level domain and subdomain DNS servers

* **the client's local DNS server**

* the Internet Service Provider's DNS server

	Answer
	The correct answer is **the client's local DNS server**. When the local DNS server cannot find the queried domain in its database, which indicates that the local server is not authoritative for this domain, it will query the authoritative root DNS server for the top-level (root) domain. The root DNS server directs the query to the DNS server for the first subdomain of the queried domain name. The query directing process continues until the local server reaches the authoritative subdomain DNS server. The authoritative subdomain DNS server resolves the initially queried domain name and replies to the local DNS server. This is how the local DNS server gets the resolved IP address. It is then the local DNS who sends the response to the client.
--------
Routers communicate First Hop Redundancy Protocol (FHRP) information between each other through hello messages. What is this mechanism called?

* EtherChannel

* **keepalive**

* link-state

* VLAN tagging
--------
Refer to the exhibit. The administrator has configured Hot Standby Router Protocol (HSRP) to provide default gateway redundancy. Which statement correctly describes the behavior of the network?

* PC1 will be able to reach remote networks if either R1 or R2 fails.

* **PC1 will be able to reach remote networks while R1 is operational.**

* PC1 will not be able to reach remote networks if either R1 or R2 fails.

* PC1 will not be able to reach remote networks if R2 fails.

	Answer
	The correct answer is **PC1 will be able to reach remote networks while R1 is operational**. Because of the explicit default gateway configuration, the ARP table of PC1 has the default gateway IPv4 mapped to the R1 MAC address, and not to the virtual IP address of the HSRP group. When R1 fails, the PC1 ARP table will not be updated, and PC1 will not be able to reach R2, which would take over the role of the default gateway.
--------
For which network entity is the **OSPF designated router/backup designated router (DR/BDR) selection performed**?

* **for each multi-access segment**

* for each OSPF router ID

* for the entire OSPF area

* per transmission state of the link

	Answer
	The correct answer is **for each multi-access segment**. The DR/BDR election is not made per area, per OSPF version, or per transmission state of the link.
--------
Which command would you **use to configure a router ID on a Cisco router**?

* R1 (config-router)# ip router-id ip-address

* **R1 (config-router)# router-id ip-address**

* R1 (config)# ip router-id ip-address

* R1 (config)# router-id ip-address

	Answer
	The correct answer is **R1 (config-router)# router-id ip-address**. For the network device administrator to configure a router ID on a router, the router-id ip-address command is used. The ip router-id ip-address, ip router-id ip-address, and router-id ip-address commands do not configure router IDs.
--------
Which two attack categories does the **smurf attack** belong to? (Choose two.)

* **amplification (Ans)**

* brute-force

* man-in-the-middle

* exfiltration

* **reflection (Ans)**
--------
What is a way **of mitigating social engineering attacks**?

* Avoiding making copies of files on external memory devices.

* Avoiding using personal data to create a password.

* Assigning administration privileges only to people with technical knowledge.

* **Training users about correct security behaviors. (Ans)**
--------
After the Cisco IOS **Software image is loaded and started, from which three components can the device load its configuration**? (Choose three.)

* DHCP server

* DNS server

* RAM

* **NVRAM**

* **SCP server**

* **TFTP server**

	Answer
	The correct answers are NVRAM, SCP server, and TFTP server. If there is an existing saved configuration file (startup-config) in NVRAM, it is executed. If the startup configuration file does not exist in NVRAM, the router may search for a network file server (TFTP, SCP, and so on). RAM stores the current configuration after it is loaded. A DHCP server can provide the URL of the configuration file, where the file can then be loaded from. DNS servers are not used for file transfers.
--------
You have restarted a router, which has the default booting procedure. During the reboot, the following messages appear on the console:

%Error opening tftp://255.255.255.255/network-confg (Timed out)
%Error opening tftp://255.255.255.255/cisconet.cfg (Timed out)
What can you conclude based on the messages?

* The router will attempt to load the configuration from the NVRAM.

* The router configuration will be loaded from the TFTP server.

* The TFTP server URL is incorrect.

* **The configuration file is not found on the TFTP server.**

	Answer
	The correct answer is The configuration file is not found on the TFTP server. By default, the router first attempts to load the startup configuration from the NVRAM. If the startup configuration file does not exist in NVRAM, the router searches for a TFTP server. If the router detects that it has an active link, it sends a broadcast searching for a configuration file across the active link. No specific TFTP URL is used. If the router does not find the configuration source, it will display the error console messages.
--------
This lab tests your knowledge about basic security configuration of the device management plane. IP addressing on all devices is already configured.

The SW2 switch in the topology has already been configured. You will have no direct access to this device, however, you can access it remotely from other devices in the topology.

SW2 already has a local database of user credentials. The Device Access table provides detailed information.

In the task, you will configure the SW1 switch and the R1 router.

On SW1, perform the following tasks:

Restrict access to the privileged EXEC mode. Configure the protected password CiscoSW1! using the default encryption type. Configure the unprotected password Cisco123! and ensure it is obfuscated in the configuration file (that is, it does not show in the plain text).

Define two users in the local database, using the following credentials:

username | password    | privilege level
1. TECH  | CiscoTech1! | default
2. ADMIN | CiscoAdm1!  | 15

On R1, perform the following tasks:

Restrict access to the privileged EXEC mode. Configure the protected password CiscoR1! using the default encryption type.

Configure the unprotected password Cisco123! and ensure it is obfuscated in the configuration file.

Protect the access to the console by requiring a password to access the console. Set the console password to Cisco333!.



From PC1, connect to SW1 using Telnet with the password Cisco111!. Which password did you use to access the privileged EXEC mode on SW1?

* Cisco111!

* Cisco123!

* CiscoAdm1!

* **CiscoSW1!**

* CiscoTech1!

On R1, at the command prompt, issue the exit command as many times as necessary until you get the "Press RETURN to get started" prompt. Which password do you have to type to access the USER exec mode?

* Cisco123!

* Cisco333!

* CiscoR1!

* **password is not required**

Answer
The correct answer is password is not required. **When accessing the USER exec mode, no password is required.**


Which number represents the **default encryption type of the protected password** used to restrict access to the **privileged EXEC mode**?

* **4**

* 5

* 8

* 9

	Answer
	The correct answer is **4**. The enable secret is always stored in a protected fashion in the configuration file. Cisco IOS Software on routers supports several encryption types. **On production routers, you will most likely find encryption type 8 or type 9.** Using the default encryption type 4, which represents the Secure Hashing Algorithm 2 (SHA-2) protection, is not recommended due to security risks. Use the show running-config command to reveal the encryption type used for enable secret.


Examine the Device Access table in the Job Aid. There are four users configured on SW2. The SW2 switch console line access is set to privilege level 5. Presuming command **privileges are set to default, which username should you use to be able to change the SW2 configuration**?

* admin

* monitor

* operator

* **superadmin**

	Answer
	The correct answer is superadmin. By default, Cisco IOS configuration commands require the maximum privilege level, which is 15. This is the privilege level of the user superadmin.


From PC1, connect to SW2 using Telnet and verify the console line configuration. How long can a user be inactive while still connected to the console of SW2?

* **60 minutes and 7 seconds**

* 60 minutes within 7 days

* 67 minutes

* 67 seconds

	Answer
	The correct answer is 60 minutes and 7 seconds. The exec-timeout command specifies the minutes and seconds that define the timeout, after which an inactive user is automatically disconnected from the console. This prevents users from remaining connected to a console port when they leave a station. Using the **exec-timeout 0 0 command disables the timeout;** this should not be used in a production environment because it is not a secure practice.


From PC2, connect to SW2 using Telnet. Examine the running configuration. **Which time zone is set?**

* CET

* **LJUB**

* MDT

* PST

	Answer
	The correct answer is LJUB. When you issue the show running-config command, the outup displays the clock timezone LJUB 8 0. You can obtain the same information using the **show clock** command.
--------
What are two field names corresponding to the **IPv4 header field and the IPv6 header field that contain Differentiated Services Code Point (DSCP) markings?** (Choose two.)

* flow control

* flow label

* IP precedence

* offset

* **traffic class**

* **type of service (ToS)**

	Answer
	The correct answers are traffic class and type of service (ToS). In the original RFC definitions of the ToS field, IP precedence was a 3-bit sub-field. The initial definition of the ToS field has been changed to include the flow control field. The offset field is the IPv4 header field used when packets are fragmented. The flow label IPv6 header field can be used to label a set of packets belonging to the same flow and does not contain DSCP markings.
--------
Which three of the following application characteristic values are determined in the **service level specification** phase **when designing the quality of service (QoS)** policy of a network? (Choose three.)

* generated data flows

* **required bandwidth**

* required responsiveness

* response criticality

* **tolerable jitter**

* **tolerable packet loss**

	Answer
	The correct answers are required bandwidth, tolerable jitter, and tolerable packet loss. When you specify the service levels for a class of traffic, you define specific values for delay and jitter, packet loss tolerance, required bandwidth, and time sensitivity. After the implementation of the QoS policy, the performance of your network can then be measured and evaluated against the specified service levels. You should identify the data flows generated by the application prior to determining service levels, in the first phase of policy design. Required responsiveness and response criticality are performed within the business audit phase, which precedes service-level specification.
--------
Which statement regarding a **small office/home office (SOHO)** of a remote worker is correct?

* **It is a LAN that includes both wireless and wired network devices.**

* It must be permanently connected to the main office.

* It must follow the three-tier architecture model.

* It typically uses dark fiber to connect to the main office.

	Answer
	The correct answer is **It is a LAN that includes both wireless and wired network devices**. The SOHO connectivity to other enterprise network segments can be established when required. To connect to other segments, SOHO networks usually use public internet, which they access via broadband connection. Since SOHO networks are typically small and consist of only a small number of devices, such as a computer and a printer, they do not need to follow the three-tier architecture model to ensure network operation.
--------
What is the network ID of the IPv6 address 2001:db8:deca:abce:45eb:27ff:feba:fa38/48?

* 2001::

* 2001:db8::

* **2001:db8:deca::**

* 2001:db8:deca:abce::

	Answer
	The correct answer is 2001:db8:deca::. **Each hexadecimal character represents 4 binary bits**. **The first 12 characters correspond to 48 bits.** 2001:db8:deca:abce:: would have the /64 prefix, 2001:db8:: would have the /32 prefix, and 2001: would have the /16 prefix.
--------
**BR2# show ip route**
<... output omitted ...>

Gateway of last resort is 172.16.2.3 to network 0.0.0.0

      172.16.0.0/16 is variably subnetted, 4 subnets, 2 masks
D        172.16.1.0/30 [90/2195456] via 172.16.2.1, 00:00:22, Ethernet0/0
C        172.16.2.0/30 is directly connected, Ethernet0/0
L        172.16.2.2/32 is directly connected, Ethernet0/0
D        172.16.3.0/30 [90/2195456] via 172.16.2.1, 00:00:22, Ethernet0/0
D     192.168.0.0/24 [90/409600] via 172.16.2.1, 00:00:22, Ethernet0/0
D     192.168.1.0/24 [90/2323456] via 172.16.2.1, 00:00:22, Ethernet0/1
      192.168.2.0/24 is variably subnetted, 2 subnets, 2 masks
C        192.168.2.0/24 is directly connected, Loopback0
L        192.168.2.1/32 is directly connected, Loopback0
D*EX  0.0.0.0/0 [170/7289856] via 172.16.2.3, 00:00:22, Ethernet0/0

Refer to the exhibit. **Router BR2 receives a packet with the destination IPv4 address of 172.16.5.20**. Based on the routing table, what would the router do with the packet?

* **Forward it out of interface Ethernet0/0. (Ans)**

* Forward it out of interface Ethernet0/1.

* Forward it out of interface Loopback0.

* It will discard the packet.
--------
Refer to the exhibit. It represents the Cisco Enterprise Architecture model. **In this model, where is the firewall located?**

* between the edge router and the core switch

* between the edge router and the distribution switch

* between the internet and the core switch

* **between the internet and the edge router (Ans)**
--------
What are two reasons for **choosing Transport Layer Security (TLS) over IP Security (IPsec)** encryption? (Choose two.)

* IPsec encrypts the IP packet, resulting in lesser application-level security.

* IPsec is less efficient than TLS, and in general not supported on mobile devices.

* **IPsec requires dedicated software installed on client hosts. (Ans)**

* **TLS can be used for encrypting traffic to public websites. (Ans)**

* TLS decryption can be easily accelerated in hardware.
--------
*******

In this lab, you will secure administrative access to Cisco IOS devices.

The devices have basic addressing configurations in place. You will use end devices as sources of remote access connections.

The following is pre-configured in the lab:

On SW2:

Telnet access parameters

On R1:

Telnet is enabled on remote access lines

remote access lines are configured for password-only login, with the password Cisco111

**access list SSHACCESS**

You will not be able to access the console of the R1 router directly. However, you will be able to access it from other devices in the topology, as instructed.

Perform the following task:

Using Telnet to access R1, configure SSH with the following parameters:

key size of 2048 bits

**domain name example.com**

login authentication must be performed against the locally stored user information

create an entry in the local database for one user, using the username **AdminPC2, maximum privilege level, and password Cisco123**

Examine the access list configuration on R1:

From PC2, access the R1 router using SSH. Apply the configured access list so that it limits remote access to R1 to only SSH connections from PC2.

########

From PC2, use SSH to access R1. Use AdminPC2 as the username and Cisco123 as the password. **What is the IPv4 address of the loopback interface?**

* 10.10.2.1

* **10.10.3.1**

* 10.10.4.1

* 10.10.5.1

	Answer
	The correct answer is 10.10.3.1. If you issue the **show ip interface brief** command, you will see that there are two interfaces configured. Ethernet0/0 has the IPv4 address 10.10.1.1 and the **loopback0 interface has the IPv4 address 10.10.3.1.**

###########

In the lab network, which SSHACCESS access list implementation would correctly limit remote access to only SSH connections from PC2?

* inbound direction on the Ethernet0/0 interface on R1

* inbound direction on the Ethernet0/2 interface on SW1

* **inbound direction on the vty lines on R1**

* outbound direction on the Ethernet0/1 interface on SW2

* outbound direction on the vty lines on R1

	Answer
	The correct answer is inbound direction on the vty lines on R1. The other proposed implementations would also limit other traffic.

###########

Examine the configuration on SW2. Based on the information in the configuration, use Telnet from PC1 to access the SW2 switch. Which message is displayed upon successful access?

* **Access for authorized users only. Proceed with caution. (Ans)**

* Only authorized access to this device is allowed!

* Unauthorized access prohibited.

* You must have permissions to access this device! If you are not authorized, do not proceed!

*******
--------
How are NETCONF messages encoded?

* by using CSS

* by using JSON

* by using SQL

* **by using XML**

	Answer
	The correct answer is by using XML. Not all devices support NETCONF; the ones that do support it, advertise their capabilities via the interface. NETCONF does not use CSS, JSON, or SQL for encoding messages.
--------
Which APIs are used for communication between a software-defined networking (SDN) application and a controller?

* Eastbound APIs

* **Northbound APIs**

* Southbound APIs

* Westbound APIs

	Answer
	The correct answer is Northbound APIs. Northbound APIs or northbound interfaces are responsible for the communication between the SDN controller and the services that run over the network. Northbound APIs enable your applications to manage and control the network. Therefore, rather than adjusting and tweaking your network repeatedly to get a service or application running correctly, you can set up a framework that allows the application to demand the network setup that it needs.
--------
Refer to the exhibit. Which two options are common IPsec or SSL VPN implementations? (Choose two.)

* **option 1**

* option 2

* option 3

* option 4

* **option 5**

	Answer
	The correct answers are option 1 and option 5. An IPsec Tunnel VPN is typically established between two network devices, connecting two or more remote networks. An SSL VPN is typically established between a client and a network device. DMVPN and IPsec VTI VPN are typically established between network devices.
--------
Which two statements about the **Dynamic Multipoint Virtual Private Network (DMVPN)** are true? (Choose two.)

* **DMVPN creates hub-to-spoke tunnels.**

* **DMVPN creates spoke-to-spoke tunnels.**

* DMVPN is used for connection between an enterprise and a provider.

* DMVPN is used for connection between enterprises.

* DMVPN is used within a branch network.

	Answer
	The correct answers are DMVPN creates hub-to-spoke tunnels and DMVPN creates spoke-to-spoke tunnels. After building the hub-and-spoke VPNs, the spokes can establish direct spoke-to-spoke tunnels, based on the information they obtain from the hub.
--------
Which three protocols use **UDP**? (Choose three.)

* **DHCP**

* FTP

* HTTPS

* **SNMP**

* **TFTP**

	Answer
	The correct answers are DHCP, SNMP, and TFTP. DHCP is a network management protocol used on UDP/IP networks whereby a DHCP server dynamically assigns an IP address and other network configuration parameters to each device on a network. TFTP is used to transfer configuration files, Cisco IOS images, and other files between systems. SNMP is an application layer protocol that facilitates the exchange of management information between network devices. FTP is a connection-oriented service that uses TCP to transfer files between systems. HTTPS uses TCP for distributed, collaborative hypermedia information systems.
--------
Which **IPv6 network prefix is only intended for local links and cannot be routed**?

* ::ffff/80

* 2001::/3

* fc00::/7

* **fe80::/10 (Ans)**
--------
What are two characteristics of an **anycast IPv6 address**? (Choose two.)

* It can be assigned to a host (end-user devices).

* **It can be assigned to multiple nodes.**

* It can be recognized by a pre-defined prefix.

* It is used in an IPv6 packet as a source IPv6 address.

* **It is assigned from the unicast IPv6 address space.**

	Answer
	The correct answers are It can be assigned to multiple nodes and It is assigned from the unicast IPv6 address space. Anycast IPv6 addresses are syntactically indistinguishable from unicast IPv6 addresses, and they do not have a dedicated prefix assigned. Anycast IPv6 addresses cannot be used by hosts, and they must not be used as the source address of an IPv6 packet.
--------
Which fields does the **802.1Q header add to an Ethernet frame**?

* CRC

* EtherType

* preamble

* **VLAN ID (Ans)**
--------
When configuring a trunk port on a Cisco switch, which VLAN ranges can be used to specify the allowed VLANs?

* **extended and standard**

* extended

* standard

* standard and reserved

	Answer
	The correct answer is extended and standard. A trunk port is a member of all VLANs by default, including extended-range VLANs, but membership can be limited by configuring the allowed-VLAN list.
--------
Which of the following network devices defines a **broadcast domain and a collision domain on every one of its ports**?

* bridge

* hub

* **router**

* switch

	Answer
	The correct answer is router. Switches and bridges create separate collision domains on their ports, but do not limit the broadcast domain to only one port. The broadcast domain on a switch includes all the ports in one VLAN. The hub extends both the collision and broadcast domains to all its ports.
--------
Which three device types can **benefit from Power over Ethernet (PoE) connectivity**? (Choose three.)

* access switches

* computers

* **IP cameras (Ans)**

* **VoIP phones (Ans)**

* **wireless access points (Ans)**
--------
What are the two main **WLAN deployment types**? (Choose two.)

* **centralized (Ans)**

* router-based

* **standalone (Ans)**

* Wi-Fi Direct

* Zero Touch Provisioning (ZTP)
--------
Which **802.11 frame is a control frame**?

* association request

* association response

* **acknowledgment (Ans)**

* beacon
--------
Which **cloud service model offers customers the most control over their cloud-hosted services?**

* Function as a Service (FaaS)

* **Infrastructure as a Service (IaaS) (Ans)**

* Platform as a Service (PaaS)

* Software as a Service (SaaS)

	Answer
	The correct answer is **Infrastructure as a Service (IaaS)**. IaaS is a cloud service model where a customer rents or purchases computing, storage, and network resources. The customer is responsible for resource specification and operating system management. In FaaS, PaaS, and SaaS, the customer does not have control over machine resources or the operating system.
--------
Which three layers does the **hierarchical three-tier model include**? (Choose three.)

* **access (Ans)**

* **core (Ans)**

* data link

* **distribution (Ans)**

* network
--------
Which command is used to set **192.168.1.1 as the default gateway** on a Layer 2 switch?

* **Switch(config)# ip default-gateway 192.168.1.1 (Ans)**

* Switch(config)# ip default-network 192.168.1.1

* Switch(config)# ip route 0.0.0.0 0.0.0.0 192.168.1.1

* Switch(config)# ip route 0.0.0.0 0.0.0.0 DHCP 1
--------
*********

The network switches must be configured to separate workstations and servers into different VLANs as displayed in the topology. To ensure inter-VLAN connectivity, router R1 is already pre-configured.

Ensure that the devices in one VLAN can communicate with each other. Perform the following tasks:

Configure IPv4 addressing on workstations and servers so that they belong to the appropriate subnet.

Configure the default gateway IPv4 address on workstations and servers.

Configure VLANs and trunking.

Do not change the default configuration on the Ethernet0/3 interface on SW2.

When configuring devices and verifying device configurations, use the information provided in the documentation, that is in the topology figure and Job Aids.

*********

When you examine the MAC address table on SW2, which VLAN does MAC aa-aa-aa-aa-22-22 belong to?

* 1

* **65**

* 80

* 1001

* 1005

	Answer
	The correct answer is 65. The MAC address aa-aa-aa-aa-22-22 belongs to PC2 and as such is a member of VLAN 65. VLAN 80 contains both server nodes. VLAN 1001 is not present in this lab topology and VLAN 1005 is a reserved FDDI/Token Ring VLAN.

#########

On SW2, verify the administrative and operational switching modes on interface Ethernet0/3. Which statement correctly describes the administrative mode and operational mode values?

* Administrative mode is access and operational mode is access.

* Administrative mode is dynamic-auto and operational mode is access.

* Administrative mode is dynamic-desirable and operational mode is access.

* **Administrative mode is dynamic-desirable and operational mode is trunk.**

* Administrative mode is trunk and operational mode is trunk.

	Answer
	The correct answer is Administrative mode is dynamic-desirable and operational mode is trunk. Administrative mode displays what you have configured on the interface. Operational mode displays the actual status of the interface. When manually configuring access or trunking, administrative and operational mode have identical values. When you configure Dynamic Trunking Protocol (DTP) to negotiate switching status, administrative and operational mode differ. Cisco recommends disabling DTP on a switch."

##########

Examine the topology and the configuration. On PC2, when you use the ping command to check connectivity to Server 1, what is the order of the devices that packets traverse?

* PC2 > SW1 > SW2 > R1 > SW2 > Server1

* PC2 > SW2 > R1 > SW1 > Server1

* PC2 > SW2 > SW1 > R1 > Server1

* **PC2 > SW2 > SW1 > R1 > SW1 > Server1 (Ans)**

#########

Which interfaces on SW1 are trunk interfaces?

* E0/0 and E0/1

* **E0/0 and E0/3**

* E0/1 and E0/2

* E0/1 and E0/3

	Answer
	The correct answer is E0/0 and E0/3. SW1 has four interfaces. The interfaces E0/0 and E0/3 are connected to a router and another switch, respectively. As such, those two interfaces are set up as trunk interfaces in order to carry multiple VLANs. The interfaces E0/1 and E0/2 are connected to end nodes, and are configured as access interfaces.
--------
Which Windows Command Prompt command do you use to view the IP address of a host?

* ip address

* ifconfig

* **ipconfig (Ans)**

* show ip address
--------
Which three statements about **IPv4 addresses** are true? (Choose three.)

* **8.0.0.0 is a public address.**

* **10.8.0.0 is a private address.**

* **127.0.0.1 is a reserved address.**

* 172.30.0.0 is a public address.

* 192.170.0.0 is a private address.

	Answer
	The correct answers are 8.0.0.0 is a public address, 10.8.0.0 is a private address, and 127.0.0.1 is a reserved address. 192.170.0.0 is a public IPv4 address, and 172.30.0.0 is a private IPv4 address.
--------
You are tasked with installing and configuring a new PoE-supported IP camera with a power consumption of 20 W. After connecting it to a PoE-enabled switch, the camera does not turn on. What is the likely cause of the problem?

* The cable connecting the switch and the camera is too long.

* The camera requires additional configuration to work with PoE.

* **The switch does not support the PoE Plus standard.**

* The switch requires additional configuration to enable PoE on the interface.

	Answer
	The correct answer is The switch does not support the PoE Plus standard. Normal PoE can only provide up to 15.4 W of power, while PoE Plus provides up to 30 W. Devices that support PoE do not need to be configured to use it, as they will power on when connected to the Ethernet. PoE is enabled on all ports. Supplied PoE power decreases with range, but the drop is minimal.
--------
Which two symptoms are characteristic of a duplex mismatch? (Choose two.)

* The full-duplex side of the link will experience increased collision rates.

* **The half-duplex side of the link will experience increased collision rates.**

* TCP data transfer will perform better than UDP data transfer.

* The connection will not be operational.

* **The full-duplex side of the link will have a large number of CRC errors.**

	Answer
	The correct answers are The half-duplex side of the link will experience increased collision rates and The full-duplex side of the link will have a large number of CRC errors. The full-duplex side of the link does not detect any collisions, since Carrier Sense Multiple Access with Collision Detection (CSMA/CD) is disabled on the full-duplex side of the link. The connections with a duplex mismatch are typically operational, but they operate poorly. When used to send a larger amount of data, the TCP data transfer would provoke collisions and trigger TCP retransmissions, which slows down the transfer.
--------
When the **store-and-forward switching method is in use, which part of the Ethernet frame is used to perform error checking using cyclic redundancy check (CRC)?**

* **All frame fields, except the FCS field in the trailer.**

* The destination MAC address in the header, and the FCS field in the trailer.

* The frame check sequence (FCS) field in the trailer.

* The source MAC address in the header, and the FCS field in the trailer.

	Answer
	The correct answer is All frame fields, except the FCS field in the trailer. A cyclic redundancy check is used to generate a CRC value for the FCS field. The FCS field value is computed as a function of the contents of the destination address, source address, type, and data and padding fields of the Ethernet frame, in other words, on all Ethernet frame fields except the FCS field.
--------
After receiving an Ethernet frame, a switch examines the destination MAC address, and forwards the frame out of all ports except the incoming port. In which communication types can this behavior occur?

* in broadcast and multicast communication

* in broadcast communication

* **in broadcast, multicast, and unicast communication**

* in unicast communication

	Answer
	The correct answer is in broadcast, multicast, and unicast communication. An Ethernet switch forwards a frame out of all ports except the incoming port when the intended recipients are all devices in a network, like in broadcast communication. It also forwards a frame out of all ports except the incoming port when communication is sent to a specific group of hosts, which is the case in multicast communications. In unicast communication, the switch will forward the frame out of all ports except the incoming port only when it does not have the destination MAC address in its MAC table.
--------
Which command would you use to configure a **floating static route?**

* ip route static 192.168.13.0 255.255.255.0 100

* **ip route 192.168.13.0 255.255.255.0 172.17.10.1 100**

* ip route 192.168.13.0 255.255.255.0 172.17.10.1

* ip route 192.168.13.0 255.255.255.0 172.17.10.1 metric 100

	Answer
	The correct answer is ip route 192.168.13.0 255.255.255.0 172.17.10.1 100. It is the only option with the correct syntax. The ip route static 192.168.13.0 255.255.255.0 100 command is missing the gateway IPv4 address or interface to that network. The ip route 192.168.13.0 255.255.255.0 172.17.10.1 command has the default administrative distance of 1 set, and is therefore not classified as a floating static route. In the ip route 192.168.13.0 255.255.255.0 172.17.10.1 metric 100 command, the keyword "metric" is redundant.
--------
For an administrator to be able to access the Layer 2 switch S1 from the internet, which IP connectivity parameters do you have to configure on the S1 switch?

* **default gateway to 192.168.3.254**

* default route via 192.168.3.254

* IPv4 address in the 209.168.200.224/27 subnet

* static route to 209.168.200.254/27

	Answer
	The correct answer is default gateway to 192.168.3.254. For **Switch S1 to be able to replay and respond as the administrator manages it, it must have a default gateway set.** On a Layer 2 switch, you cannot configure routes, since IP routing is not enabled. For the switch virtual interface to work, the VLAN must be associated and active on at least one physical port.
--------
When a router is calculating the network portion of an IPv4 address, which bitwise operation is performed on the IPv4 address and the subnet mask?

* **AND**

* NAND

* OR

* XOR

	Answer
	The correct answer is AND. In order to extract the network part of an IPv4 address, the ANDing logical operation is performed with the IPv4 address and the subnet mask as operands. When the binary digit 1 is ANDed with another digit, the value of the other digit is preserved. ANDing with 0 always results in a 0. Therefore, 1s in the subnet mask will preserve the value found in the IPv4 address. The logical operations NAND, OR, and XOR would not preserve the values found in the IPv4 address.
--------
Two computers are connected to a Cisco Catalyst Layer 2 switch. PC1 is assigned the address 10.250.20.20/26 and PC2 is assigned the address 10.250.20.50/26. When a user on PC1 issues the ping 10.250.20.63 command, will PC2 respond to it?

* No, because 10.250.20.63 is not in the subnet that PC1 belongs to.

* No, because 10.250.20.63 is not the IP of PC2.

* **Yes, the PC2 will respond to the 10.250.20.63 broadcast if both ports are operationally in access mode and the same VLAN**

* Yes, if the ip routing command is configured on the switch.

	Answer
	The correct answer is Yes, the PC2 will respond to the 10.250.20.63 broadcast if both ports are operationally in access mode and the same VLAN. The IPv4 address 10.250.20.63 is the broadcast address of the 10.250.20.0/26 subnet. A switch forward broadcast communication to all ports in a VLAN. If both ports that connect PC1 and PC2 belong to the same VLAN, then PC2 as well as other devices in the same subnet will receive the ICMP request from PC1 and respond to it.
--------
Refer to the exhibit. In an 802.1X implementation, what are the roles of the devices shown?

* A: authenticator, B: supplicant, C: authentication server

* A: client device, B: supplicant, C: authentication server

* **A: supplicant, B: authenticator, C: authentication server**

* A: supplicant, B: client device, C: authentication server

	Answer
	The correct answer is A: supplicant, B: authenticator, C: authentication server. A supplicant is a workstation with 802.1X-compliant client software. An authenticator acts as a proxy between the supplicant and an authentication server. An authentication server authenticates supplicants connecting to a switch port.
--------
What are two differences between the RADIUS and TACACS+ protocols? (Choose two.)

* **RADIUS combines authentication and authorization, while TACACS+ implements two separate processes.**

* RADIUS encrypts the entire payload, while TACACS+ encrypts only the password.

* RADIUS is a TCP-based protocol, while TACACS+ is a UDP-based protocol.

* **RADIUS is a UDP based protocol. TACACS+ is a TCP based protocol.**

* RADIUS supports bidirectional authentication, while TACACS+ supports only unidirectional authentication.

	Answer
	The correct answers are RADIUS combines authentication and authorization, while TACACS+ implements two separate processes and RADIUS is a UDP based protocol. TACACS+ is a TCP based protocol. RADIUS is an open standard that combines authentication and authorization services into a single process. TACACS+ is a Cisco proprietary security mechanism that can be used only for authorization and accounting while using another method of authentication. TACACS+ uses the Transmission Control Protocol (TCP) for all three services.
--------
How **many switch ports are designated ports on a root bridge?**

* **all of them (Ans)**

* none of them

* one

* two
--------
What is the purpose of the blocking state of ports in STP (Spanning Tree Protocol)?

* To prevent MITM (man-in-the-middle) attacks.

* To prevent retransmission of routing protocol updates.

* **To prevent path loops. (Ans)**

* To prevent unauthorized usage of unused ports.

--------
*********

During this activity, you will use the Cisco Discovery Protocol (CDP) and the Link Layer Discovery Protocol (LLDP) to map the connectivity within an unfamiliar network. There are four devices in the topology. You have access to the console ports of SW1, SW2, and R1. However, you do not know how they are connected. Using the CDP and LLDP commands, you will determine the actual topology.

IPv4 addressing is configured on all devices.

The SW2 neighbor discovery protocol is pre-configured. Do not change the existing configuration parameters on SW2.

CDP is already configured on R2. You will not have direct access to the R2 router. You can gain information about R2 configuration using neighbor discovery protocols on neighboring devices.

In this task you will discover the topology using Link Layer Discovery Protocol (LLDP) and the Cisco Discovery Protocol (CDP). Router R2 is already pre-configured. Perform the following tasks:

Examine the configurations of the SW1 and SW2 switches. Answer the first question.

Configure switch SW1 and router R1 so that Layer 2 connectivity information is provided among all devices in the topology, that is: SW1, SW2, R1, and R2.

*********

Examine the configurations of the switches SW1 and SW2. SW2 cannot obtain Layer 2 information from SW1 using CDP. Why?

* because CDP is disabled on the interface connecting to SW1

* **because CDP is globally disabled on SW2**

* because the interface connecting to SW1 is down

* because the interface connecting to SW1 is in the wrong VLAN

* because STP is blocking the interface connecting to SW1

	Answer
	The correct answer is because CDP is globally disabled on SW2. The Cisco Discovery Protocol works as long it is globally enabled and not disabled on specific interfaces connecting two devices, and the two devices have L1 and L2 connectivity.


What is the IP address of the R2 interface connecting to R1?

* 10.10.1.3

* 192.168.3.1

* **192.168.3.2 (Ans)**

* 192.168.3.3

Answer
The correct answer is 192.168.3.2. By issuing the **show cdp neighbors detail** command on R1, you are able to get the IPv4 address of R2’s interface connecting to R1.

##########

What are the ports that interconnect switches SW1 and SW2?

* **SW1 Ethernet0/0 and SW2 Ethernet0/0**

* SW1 Ethernet0/0 and SW2 Ethernet0/1

* SW1 Ethernet0/1 and SW2 Ethernet0/0

* SW1 Ethernet0/1 and SW2 Ethernet0/1

	Answer
	The correct answer is SW1 Ethernet0/0 and SW2 Ethernet0/0. By issuing the show lldp neighbors command, you can learn that SW1 and SW2 are connected by using Ethernet0/0 ports on both.

###########

In the topology you discovered in this exercise, can R1 obtain information about SW1 using CDP?

* **No, because R1 and SW1 are not directly connected.**

* No, because STP is blocking the connection between R1 and SW1.

* Yes, because R1 and SW1 are directly connected.

* Yes, because R1 and SW1 both have CDP enabled.

	Answer
	The correct answer is No, because R1 and SW1 are not directly connected. By examining the topology using CDP, you can determine that SW1 and R1 are not directly connected. SW2 is used to interconnect the two devices and CDP information is not propagated over devices.

#########

On SW4, which port is the STP root port for VLAN 20?

* Eth1/0

* Po14

* Po24

* **Po34**

	Answer
	The correct answer is Po34. SW3 is the root bridge for VLAN 20. SW4 is connected to SW3 via aggregated links represented by interfaces Po14, Po24, and Po34. After verifying the STP status for VLAN 20, you can see that the Po34 interface has the shortest path, hence the lowest cost and is elected as the root port.

##########

On SW2, when you see the summary information for aggregated link. What is the status code or flags of the port channel Po23?

* down (D)

* **Layer2 - In use (SU)**

* stand-alone (I)

* suspended (s)

	Answer
	The correct answer is Layer2 - In use (SU). When you use the show etherchannel summary command, the SU Status code signifies that the aggregated channel is Layer 2 channel and that it is active.

###########

Issue the ping command from PC1 to PC2. What is the path that packets traverse?

* **SW1 > SW3 > SW2**

* SW1 > SW3 > SW4 > SW2

* SW1 > SW4 > SW2

* SW1 > SW4 > SW3 > SW2

	Answer
	The correct answer is SW1 > SW3 > SW2. This is the resulting path of VLAN 10 after STP calculations are performed, taking aggregated links into consideration.

--------
*********

In this task you will configure link aggregation and examine its effects on STP topology. The network devices are pre-configured with basic connectivity parameters and Rapid Per VLAN Spanning Tree Protocol Plus (Rapid PVSTP+) to prevent traffic loops. The topology consists of three segments: workstations, servers, and connecting segment. All devices have their basic configurations in place, including hostnames and IP addresses.

Carefully examine the device configurations. There are some mistakes in the interface configuration on network devices. First, find the mistakes and correct them. Then, perform the following configuration tasks, and answer the questions.

Create EtherChannel links between the switches using the Link Aggregation Control Protocol (LACP).

Configure the switches so SW3 is the root switch for VLAN 20 and SW1 is the root switch for VLAN 10.

Ensure there is full connectivity within each VLAN (that is, you can successfully issue the ping command between PC1 and PC2, between SRV1 and SRV2, and between switches).

*********

Refer to the exhibit. The figure represents the topology resulting from STP calculations after configuring the Layer 2 EtherChannel. Which VLAN does the topology in the exhibit represent?

* VLAN 1

* VLAN 10

* **VLAN 20**

* VLAN 99

	Answer
	The correct answer is VLAN 20. When you use the show spanning-tree command on a switch, the output displays STP information for each VLAN, including the STP root bridge election results and port designations.
--------
In order to allow SNMP traffic to flow throughout the network, which two communication scenarios must be allowed? (Choose two.)

* TCP to port 161

* TCP to port 162

* UDP and TCP to port 161

* UDP and TCP to port 162

* **UDP to port 161**

* **UDP to port 162**

	Answer
	The correct answers are UDP to port 161 and UDP to port 162. SNMP uses the UDP transport mechanism to retrieve and send management information. The SNMP manager polls the SNMP agents and queries the MIB via SNMP agents on UDP port 161. The SNMP agent can also send triggered messages called traps to the SNMP manager, on UDP port 162.
--------
Which **three SNMP messages are sent from an SNMP agent to an SNMP manager**? (Choose three.)

* GetRequest

* GetNextRequest

* **InformRequest**

* **Response**

* SetRequest

* **Trap**

	Answer
	The correct answers are InformRequest, Response, and Trap. GetRequest, GetNextRequest and SetRequest are SNMP messages that an SNMP manager sends to an SNMP agent.
--------
A client issues a DNS request to its local DNS server. The local DNS server does not have the information required. Which entity will finally send a DNS response to the client?

* the authoritative DNS server for the top-level domain

* the authoritative top-level domain and subdomain DNS servers

* **the client's local DNS server**

* the Internet Service Provider's DNS server

	Answer
	The correct answer is the client's local DNS server. When the local DNS server cannot find the queried domain in its database, which indicates that the local server is not authoritative for this domain, it will query the authoritative root DNS server for the top-level (root) domain. The root DNS server directs the query to the DNS server for the first subdomain of the queried domain name. The query directing process continues until the local server reaches the authoritative subdomain DNS server. The authoritative subdomain DNS server resolves the initially queried domain name and replies to the local DNS server. This is how the local DNS server gets the resolved IP address. It is then the local DNS who sends the response to the client.
--------
Which command would you use to **verify the number of excluded addresses on a router configured as a DHCP server**?

* show ip dhcp bindings

* show ip dhcp conflict

* show ip dhcp database

* **show ip dhcp pool (Ans)**
--------
Routers communicate First Hop Redundancy Protocol (FHRP) information between each other through hello messages. What is this mechanism called?

* EtherChannel

* **keepalive (Ans)**

* link-state

* VLAN tagging
--------
When using **Hot Standby Router Protocol (HSRP) for gateway redundancy**, which address is used for the gateway on hosts?

* active

* active and standby

* standby

* **virtual**

	Answer
	The correct answer is virtual. HSRP provides gateway redundancy by sharing IP and MAC addresses between redundant gateways. The protocol consists of virtual IP and MAC addresses that the routers belonging to the same HSRP group share between each other.
--------
Where does a router that runs **OSPFv2**, and that has neighbor adjacencies established, **store link-state advertisements** (LSAs)?

* **LSDB**

* Neighbors table

* Routing table

* SPF tree

	Answer
	The correct answer is LSDB. An LSA is a type of packet containing information about adjacent routers and networks that it is connected to. A router stores LSAs in the link-state database (LSDB), which is then used for the calculation of optimal paths through the network.
--------
Which **algorithm is used to calculate the optimal path** to a given destination from data stored in a link-state database (LSDB)?

* Rivest, Shamir, and Adleman (RSA)

* Secure Hash Algorithm (SHA)

* **Shortest Path First (SPF)**

* Quicksort

	Answer
	The correct answer is Shortest Path First (SPF). SPF is a widely used algorithm in computer science for finding the optimal path through nodes in a network or, in this case, a network of routers. The RSA and SHA algorithms are used for secure data transmission. RSA is used for encryption and SHA is a hash function that ensures transmitted data integrity. Quicksort is an algorithm used for sorting an array of data.
--------
What is a way of mitigating social engineering attacks?

* Avoiding making copies of files on external memory devices.

* Avoiding using personal data to create a password.

* Assigning administration privileges only to people with technical knowledge.

* **Training users about correct security behaviors. (Ans)**
--------
Which two attack categories does the smurf attack belong to? (Choose two.)

* **amplification**

* brute-force

* man-in-the-middle

* exfiltration

* **reflection**

	Answer
	The correct answers are amplification and reflection. A smurf attack can be classified as a reflection attack because it is launched from a single source spoofing one or multiple IP addresses, triggering replies to the spoofed sources. By sending a small amount of request traffic, an attacker can cause much larger response traffic, making it an amplification attack.
--------
You have restarted a router, which has the default booting procedure. During the reboot, the following messages appear on the console:

%Error opening tftp://255.255.255.255/network-confg (Timed out)
%Error opening tftp://255.255.255.255/cisconet.cfg (Timed out)
What can you conclude based on the messages?

* The router will attempt to load the configuration from the NVRAM.

* The router configuration will be loaded from the TFTP server.

* The TFTP server URL is incorrect.

* **The configuration file is not found on the TFTP server.**

	Answer
	The correct answer is The configuration file is not found on the TFTP server. By default, the router first attempts to load the startup configuration from the NVRAM. If the startup configuration file does not exist in NVRAM, the router searches for a TFTP server. If the router detects that it has an active link, it sends a broadcast searching for a configuration file across the active link. No specific TFTP URL is used. If the router does not find the configuration source, it will display the error console messages.
--------
What does the term **per-hop behavior (PHB)** signify?

* a set of node requirements for compliance with the DiffServ model

* a set of packet markings applied to different classes of traffic

* **a set of techniques for traffic shaping (Ans)**

* a set of traffic classes defined in the network
--------
Which three types of booting are supported on servers? (Choose three.)

* **booting from internal storage (Ans)**

* **booting from LAN (Ans)**

* **booting from SAN (Ans)**

* booting from WAN

* booting from wireless
--------
On a router that does not have a default route in the routing table, you issue the following two commands:

Router(config)# ip route 0.0.0.0 0.0.0.0 10.10.10.10 20
Router(config)# ip route 0.0.0.0 0.0.0.0 10.20.250.2 10
What is the result of executing the commands?

* Both routes are installed in the routing table as default routes.

* The route pointing to the IPv4 address 10.10.10.10 is installed as the default route.

* **The route pointing to the IPv4 address 10.20.250.2 is installed as the default route.**

* There are no changes to the routing table.

	Answer
	The correct answer is The route pointing to the IPv4 address 10.20.250.2 is installed as the default route. The ip route command can specify the administrative distance in its arguments. When two routes are configured to the same destination network, the one with the lower administrative distance will be installed in the routing table.
--------
What is the network ID of the IPv6 address 2001:db8:deca:abce:45eb:27ff:feba:fa38/48?

* 2001::

* 2001:db8::

* **2001:db8:deca::**

* 2001:db8:deca:abce::

	Answer
	The correct answer is 2001:db8:deca::. Each hexadecimal character represents 4 binary bits. The first 12 characters correspond to 48 bits. 2001:db8:deca:abce:: would have the /64 prefix, 2001:db8:: would have the /32 prefix, and 2001: would have the /16 prefix.
--------
Which statement is true about using the Device Provisioning Protocol (DPP) to provision wireless devices?

* DPP is a replacement of RADIUS with enhanced security.

* DPP is a replacement of WPA2 with enhanced security.

* DPP is used to provision an 802.1X-based clientless service.

* **DPP is used with IoT devices to make the provisioning process easier. (Ans)**
--------
In a wireless IEEE **802.11 implementation**, what is the most secure option to protect user traffic?

* WEP

* WPA

* WPA2

* **WPA3**

	Answer
	The correct answer is WPA3. Wi-Fi Protected Access 3 (WPA3) is a replacement of WPA2 and is the next generation of wireless security standards that provides more resiliency to network attacks.
--------

############

In this lab, you will secure administrative access to Cisco IOS devices.

The devices have basic addressing configurations in place. You will use end devices as sources of remote access connections.

The following is pre-configured in the lab:

On SW2:

Telnet access parameters

On R1:

Telnet is enabled on remote access lines

remote access lines are configured for password-only login, with the password Cisco111

access list SSHACCESS

You will not be able to access the console of the R1 router directly. However, you will be able to access it from other devices in the topology, as instructed.

Perform the following task:

Using Telnet to access R1, configure SSH with the following parameters:

key size of 2048 bits

domain name example.com

login authentication must be performed against the locally stored user information

create an entry in the local database for one user, using the username AdminPC2, maximum privilege level, and password Cisco123

Examine the access list configuration on R1:

From PC2, access the R1 router using SSH. Apply the configured access list so that it limits remote access to R1 to only SSH connections from PC2.

Note
The devices in the topology may take 2 to 3 minutes to boot up and become accessible.

You are using a US English keyboard layout. This cannot be changed once the lab has initialized.
Change Keyboard Layout

 Visit Device Help for info about changing the OS keyboard layout and screen resolution after lab initialization.

You may navigate away from this page once you begin initializing the lab.
You will be notified once the devices are ready.

From PC2, use SSH to access R1. Use AdminPC2 as the username and Cisco123 as the password. What is the IPv4 address of the loopback interface?

* 10.10.2.1

* **10.10.3.1 (Ans)**

* 10.10.4.1

* 10.10.5.1

In the lab network, which SSHACCESS access list implementation would correctly limit remote access to only SSH connections from PC2?

* inbound direction on the Ethernet0/0 interface on R1

* inbound direction on the Ethernet0/2 interface on SW1

* **inbound direction on the vty lines on R1**

* outbound direction on the Ethernet0/1 interface on SW2

* outbound direction on the vty lines on R1

	Answer
	The correct answer is inbound direction on the vty lines on R1. The other proposed implementations would also limit other traffic.

Examine the configuration on SW2. Based on the information in the configuration, use Telnet from PC1 to access the SW2 switch. Which message is displayed upon successful access?

* **Access for authorized users only. Proceed with caution.**

* Only authorized access to this device is allowed!

* Unauthorized access prohibited.

* You must have permissions to access this device! If you are not authorized, do not proceed!

	Answer
	The correct answer is Access for authorized users only. Proceed with caution. The banner that is displayed when accessing is called the login banner. Another banner that you will see when connecting to SW2 is the message of the day (MOTD) banner. The MOTD banner is displayed to all terminals that are connected and is useful for sending messages that affect all users (such as impending system shutdowns).

In the Cisco Software-Defined Access solution, which three network elements are used to build the underlay network? (Choose three.)

* Cisco DNA Center

* Cisco Identity Services Engine

* **Cisco routers (Ans)**

* **Cisco switches (Ans)**

* **Cisco Wireless LAN Controllers (Ans)**
############

--------
Refer to the exhibit. The service provider is implementing **Multiprotocol Label Switching Virtual Private Network (MPLS VPN)** service. Which two options indicate the specific VPN type that is implemented and how the service provider appears from the perspective of the customer? (Choose two.)

* The service provider is implementing MPLS L2VPN.

* **The service provider is implementing MPLS L3VPN.**

* The service provider is implementing MPLS VPLS.

* **The service provider network can be represented as a router from the customer perspective.**

* The service provider network can be represented as a switch from the customer perspective.

	Answer
	The correct answers are The service provider is implementing MPLS L3VPN. and The service provider network can be represented as a router from the customer perspective.
--------
Which two statements about the **Dynamic Multipoint Virtual Private Network (DMVPN)** are true? (Choose two.)

* **DMVPN creates hub-to-spoke tunnels.**

* **DMVPN creates spoke-to-spoke tunnels.**

* DMVPN is used for connection between an enterprise and a provider.

* DMVPN is used for connection between enterprises.

* DMVPN is used within a branch network.

	Answer
	The correct answers are DMVPN creates hub-to-spoke tunnels and DMVPN creates spoke-to-spoke tunnels. After building the hub-and-spoke VPNs, the spokes can establish direct spoke-to-spoke tunnels, based on the information they obtain from the hub.
--------
Which three protocols use UDP? (Choose three.)

* **DHCP**

* FTP

* HTTPS

* **SNMP**

* **TFTP**

	Answer
	The correct answers are DHCP, SNMP, and TFTP. DHCP is a network management protocol used on UDP/IP networks whereby a DHCP server dynamically assigns an IP address and other network configuration parameters to each device on a network. TFTP is used to transfer configuration files, Cisco IOS images, and other files between systems. SNMP is an application layer protocol that facilitates the exchange of management information between network devices. FTP is a connection-oriented service that uses TCP to transfer files between systems. HTTPS uses TCP for distributed, collaborative hypermedia information systems.
--------
Which **IPv6 network prefix is only intended for local links and cannot be routed**?

* ::ffff/80

* 2001::/3

* fc00::/7

* **fe80::/10 (Ans)**
--------
What are two characteristics of an **anycast IPv6 address**? (Choose two.)

* It can be assigned to a host (end-user devices).

* **It can be assigned to multiple nodes.**

* It can be recognized by a pre-defined prefix.

* It is used in an IPv6 packet as a source IPv6 address.

* **It is assigned from the unicast IPv6 address space.**

	Answer
	The correct answers are It can be assigned to multiple nodes and It is assigned from the unicast IPv6 address space. Anycast IPv6 addresses are syntactically indistinguishable from unicast IPv6 addresses, and they do not have a dedicated prefix assigned. Anycast IPv6 addresses cannot be used by hosts, and they must not be used as the source address of an IPv6 packet.
--------
Which three characteristics apply to the 802.1Q protocol? (Choose three.)

* **It carries untagged frames.**

* **It modifies the 802.3 frame header.**

* It includes an 8-bit field for TTL (Time to Live).

* It is a messaging protocol that carries a VLAN configuration.

* **It uses an internal tagging mechanism.**

	Answer
	The correct answers are It carries untagged frames, It modifies the 802.3 frame, and It uses an internal tagging mechanism. The 802.1Q protocol does not include an 8-bit field for TTL, and it is not a messaging protocol that carries a VLAN configuration.
--------
Which three device types can benefit from Power over Ethernet (PoE) connectivity? (Choose three.)

* access switches

* computers

* **IP cameras (Ans)**

* **VoIP phones (Ans)**

* **wireless access points (Ans)**
--------
Which of the following **network devices defines a broadcast domain and a collision domain on every one of its ports**?

* bridge

* hub

* **router**

* switch

	Answer
	The correct answer is router. Switches and bridges create separate collision domains on their ports, but do not limit the broadcast domain to only one port. The broadcast domain on a switch includes all the ports in one VLAN. The hub extends both the collision and broadcast domains to all its ports.
--------
What is the benefit of Mobility Express wireless access points (APs)?

* multiple SSIDs

* multiple VLANs

* Quality of Service (QoS)

* **reduced initial cost (Ans)**
--------
What is the name typically used to describe virtualization software?

* container

* distributed resource scheduler (DRS)

* **hypervisor (Ans)**

* HyperFlex

* snapshot manager
--------
Which cloud service model offers customers the most control over their cloud-hosted services?

* Function as a Service (FaaS)

* **Infrastructure as a Service (IaaS)**

* Platform as a Service (PaaS)

* Software as a Service (SaaS)

	Answer
	The correct answer is Infrastructure as a Service (IaaS). IaaS is a cloud service model where a customer rents or purchases computing, storage, and network resources. The customer is responsible for resource specification and operating system management. In FaaS, PaaS, and SaaS, the customer does not have control over machine resources or the operating system.
--------
Which command is used to set 192.168.1.1 as the default gateway on a Layer 2 switch?

* **Switch(config)# ip default-gateway 192.168.1.1 (Ans)**

* Switch(config)# ip default-network 192.168.1.1

* Switch(config)# ip route 0.0.0.0 0.0.0.0 192.168.1.1

* Switch(config)# ip route 0.0.0.0 0.0.0.0 DHCP 1
--------
Refer to the exhibit. PC1 does not have a default gateway configured. The R1 router has a proxy ARP feature enabled on all its Ethernet interfaces. When PC1 sends a frame to the File Server, what is the destination MAC address in the outgoing frame?

* **aa:aa:aa:11:11:11**

* aa:aa:aa:22:22:22

* bb:bb:bb:11:11:11

* bb:bb:bb:22:22:22

	Answer
	The correct answer is aa:aa:aa:11:11:11. When the proxy ARP feature is enabled, the local router will send its MAC address in the response to an ARP request transmitted by the host. When the host without the default gateway configuration sends the ARP request, it includes the packet's destination IPv4 address.
--------

#############
In this task you will use variable length subnet masking (VLSM) to determine the addressing scheme for the network represented by the topology.

The topology consists of four segments: segment A, segment B, segment C, and segment D.

You are assigned the 172.16.31.0/24 address space.

The first subnet from this address space is already determined using VLSM. The first subnet is 172.16.31.0/29 and is assigned to segment A.

All addressing in segment A is pre-configured on all devices. Examine the configurations of devices in segment A.

There are two addressing mistakes in the pre-configuration. Find the two mistakes, note them down, and correct them. If correcting requires you to change IPv4 addressing, use the first available IPv4 address.

Perform the following tasks:

From the assigned address space, allocate the second available VLSM segment to segment B so that it can accommodate five end devices. Note that the first available segment was already used for segment A (172.16.31.0/29).

On R2, configure the Ethernet0/1 interface with the last available IPv4 address in the chosen segment.

On PC1, configure the Ethernet0/0 interface with the first available IPv4 address in the chosen segment.

On PC1, configure the default gateway.

Continue with VLSM subnetting and allocate the next available VLSM segment to segment C. Choose the subnet size so that it exactly meets addressing requirements as represented by the topology.

On R1, configure Ethernet0/2 interface with the first available IPv4 address from the chosen VLSM segment.

On R4, configure Ethernet0/0 interface on R4 with the last available IPv4 address from the chosen VLSM segment.

Note
The routers in the topology may take 2 to 3 minutes to boot up and become accessible.

You are using a US English keyboard layout. This cannot be changed once the lab has initialized.
Change Keyboard Layout

 Visit Device Help for info about changing the OS keyboard layout and screen resolution after lab initialization.

You may navigate away from this page once you begin initializing the lab.
You will be notified once the devices are ready.

Examine the configurations of the devices in segment A. Which two address configuration mistakes were made? (Choose two.)

* **The IPv4 address was incorrect on R1.**

* The IPv4 address was incorrect on R2.

* The IPv4 address was incorrect on R3.

* The subnet mask was incorrect on R1.

* **The subnet mask was incorrect on R3.**

	Answer
	The correct answers are The IPv4 address was incorrect on R1 and The subnet mask was incorrect on R3. The R1 router had an IP address of 172.16.31.9 set, which is not part of the first VLSM network (172.16.31.0/29). The subnet mask on R3 was 255.255.255.240, which sets a bigger network (14 hosts) than is necessary.

On PC1, which address did you configure as the default gateway?

* 172.16.31.7

* 172.16.31.8

* **172.16.31.14 (Ans)**

* 172.16.31.15

#############

--------
Which three IPv4 addresses are private? (Choose three.)

* **10.255.255.254 (Ans)**

* **172.31.255.254 (Ans)**

* 172.32.255.254

* **192.168.1.100 (Ans)**

* 192.169.1.100
--------
Which three statements about IPv4 addresses are true? (Choose three.)

* **8.0.0.0 is a public address.**

* **10.8.0.0 is a private address.**

* **127.0.0.1 is a reserved address.**

* 172.30.0.0 is a public address.

* 192.170.0.0 is a private address.

	Answer
	The correct answers are **8.0.0.0 is a public address, 10.8.0.0 is a private address, and 127.0.0.1 is a reserved address**. 192.170.0.0 is a public IPv4 address, and 172.30.0.0 is a private IPv4 address.
--------
You are tasked with installing and configuring a new PoE-supported IP camera with a power consumption of 20 W. After connecting it to a PoE-enabled switch, the camera does not turn on. What is the likely cause of the problem?

* The cable connecting the switch and the camera is too long.

* The camera requires additional configuration to work with PoE.

* **The switch does not support the PoE Plus standard. (Ans)**

* The switch requires additional configuration to enable PoE on the interface.
--------
Which two symptoms are characteristic of a duplex mismatch? (Choose two.)

* The full-duplex side of the link will experience increased collision rates.

* **The half-duplex side of the link will experience increased collision rates. (Ans)**

* TCP data transfer will perform better than UDP data transfer.

* The connection will not be operational.

* **The full-duplex side of the link will have a large number of CRC errors. (Ans)**
--------
When the **store-and-forward switching method is in use**, which part of the Ethernet frame is used to perform error checking using cyclic redundancy check (CRC)?

* **All frame fields, except the FCS field in the trailer.**

* The destination MAC address in the header, and the FCS field in the trailer.

* The frame check sequence (FCS) field in the trailer.

* The source MAC address in the header, and the FCS field in the trailer.

--------
On Cisco routers, routing for IPv6 is not enabled by default. Which command should you use **to enable IPv6 routing**?

* ipv6 enable

* ipv6 local policy route-map

* ipv6 route <IPv6 address>

* **ipv6 unicast-routing (Ans)**
--------
On a Cisco router, which command should you use to display the **IPv6 routing table**?

* show ipv6 neighbors

* show ipv6 protocols

* **show ipv6 route (Ans)**

* show ipv6 router
--------
How many bits does the subnet mask consist of?

* 16

* 24

* **32 (Ans)**

* 48
--------
When a router is calculating the network portion of an IPv4 address, which bitwise operation is performed on the IPv4 address and the subnet mask?

* **AND**

* NAND

* OR

* XOR

	Answer
	The correct answer is **AND**. In order to extract the network part of an IPv4 address, the ANDing logical operation is performed with the IPv4 address and the subnet mask as operands. When the binary digit 1 is ANDed with another digit, the value of the other digit is preserved. ANDing with 0 always results in a 0. Therefore, 1s in the subnet mask will preserve the value found in the IPv4 address. The logical operations NAND, OR, and XOR would not preserve the values found in the IPv4 address.
--------
Refer to the exhibit. In an 802.1X implementation, what are the roles of the devices shown?
	A is laptop/desktop
	B is Switch
	C is Server

* A: authenticator, B: supplicant, C: authentication server

* A: client device, B: supplicant, C: authentication server

* **A: supplicant, B: authenticator, C: authentication server**

* A: supplicant, B: client device, C: authentication server

	Answer
	The correct answer is **A: supplicant, B: authenticator, C: authentication server.** A supplicant is a workstation with 802.1X-compliant client software. An authenticator acts as a proxy between the supplicant and an authentication server. An authentication server authenticates supplicants connecting to a switch port.
--------
In an enterprise environment, which guideline should be **implemented to manage passwords securely, and why**?

* A centralized password repository should be avoided, because it is a single point of failure.

* A local password repository should be used, because it is more secure, and there is no need to transmit passwords using a AAA protocol.

* **Access to passwords should be logged along with the user information, in order to have visibility of password usage. (Ans)**

* Passwords should NOT be used, because digital certificates are more secure and scale better.
--------
In Cisco PVST+, how many root ports per VLAN are allowed on a device?

* **1 (Ans)**

* 8

* 24

* 32
--------
How many switch ports are designated ports on a root bridge?

* **all of them**

* none of them

* one

* two

	Answer
	The correct answer is **all of them**. For root bridges, all switch ports are designated ports. Non-root bridges have only one designated switch port.
--------

###############

In this task you will configure link aggregation and examine its effects on STP topology. The network devices are pre-configured with basic connectivity parameters and Rapid Per VLAN Spanning Tree Protocol Plus (Rapid PVSTP+) to prevent traffic loops. The topology consists of three segments: workstations, servers, and connecting segment. All devices have their basic configurations in place, including hostnames and IP addresses.

Carefully examine the device configurations. There are some mistakes in the interface configuration on network devices. First, find the mistakes and correct them. Then, perform the following configuration tasks, and answer the questions.

Create EtherChannel links between the switches using the Link Aggregation Control Protocol (LACP).

Configure the switches so SW3 is the root switch for VLAN 20 and SW1 is the root switch for VLAN 10.

Ensure there is full connectivity within each VLAN (that is, you can successfully issue the ping command between PC1 and PC2, between SRV1 and SRV2, and between switches).

On SW4, which port is the STP root port for VLAN 20?

* Eth1/0

* Po14

* Po24

* **Po34**

	Answer
	The correct answer is **Po34**. SW3 is the root bridge for VLAN 20. SW4 is connected to SW3 via aggregated links represented by interfaces Po14, Po24, and Po34. After verifying the STP status for VLAN 20, you can see that the Po34 interface has the shortest path, hence the lowest cost and is elected as the root port.

On SW2, when you see the summary information for aggregated link. What is the status code or flags of the port channel Po23? Need to find the answer

* down (D)

* **Layer2 - In use (SU)**

* stand-alone (I)

* suspended (s)

Issue the ping command from PC1 to PC2. What is the path that packets traverse? Need to find the answer

* **SW1 > SW3 > SW2**

* SW1 > SW3 > SW4 > SW2

* SW1 > SW4 > SW2

* SW1 > SW4 > SW3 > SW2

Refer to the exhibit. The figure represents the topology resulting from STP calculations after configuring the Layer 2 EtherChannel. Which VLAN does the topology in the exhibit represent?

* VLAN 1

* VLAN 10

* **VLAN 20**

* VLAN 99

	Answer
	The correct answer is **VLAN 20**. When you use the show spanning-tree command on a switch, the output displays STP information for each VLAN, including the STP root bridge election results and port designations.

###########

--------

###########
The lab is prepared with the devices that are represented in the topology diagram. All devices have their basic configurations in place, including host names and IPv4 addresses. The SRV2 server is a DNS server for both departments. The domain names of the devices are equal to their host names. Note that static routing is implemented between the routers to ensure connectivity between the network segments.

Perform the following tasks:

On R1, the IP standard access list 10 is already configured. Implement the IP standard access list 10 on the R1 Ethernet0/3 interface by applying it in the outbound direction.

On PC1, change the IP address on Ethernet 0/0 to 10.10.1.11/24.

On R1 Ethernet 0/1, configure an access list to deny Telnet and permit ping from SRV1 to SRV2. Apply the access list to the Ethernet 0/1 interface.

You want to deny Telnet and permit ping from SRV1 to SRV2. The access list 101 will be used and you have already prepared two access list given below. The access list will be applied in the inbound direction on the R1 Ethernet 0/1 interface. Which statement describes the correct configuration?

	access-list 101 deny tcp host 10.10.2.20 host 203.0.113.30 eq telnet
	access-list 101 permit icmp host 10.10.2.20 host 203.0.113.30

* The deny any any statement should be added at the end of the access list.

* **The order of the two prepared statements is not important. (Ans)**

* The prepared permit statement must be placed before the deny statement.

* The prepared deny statement must be placed before the permit statement.

Which Cisco IOS command displays the sequence numbers of the statements in the access list?

* show ip access-group

* **show ip access-lists (Ans)**

* show running-config

* show running-config all
###############

--------
The console of a device you are administering displays the following syslog message:

%LINK-**3**-UPDOWN: Interface FastEthernet0/0, changed state to down
What is the severity level of the displayed syslog message?

* **Error**

* Log alert

* Log audit

* System daemon

* Warning

	Answer
	The correct answer is **Error**. The general format of syslog messages that the syslog process on Cisco IOS Software generates by default is: seq no:time stamp: %facility-severity-MNEMONIC:description. The "LINK" word of the message indicates which facility is the source of the message. The syslog RFC defines these sources by a numeric value. Cisco facilities are a free-form method of identifying the source message type such as SYS, IP, LDP, L2, MEM, FILESYS, DOT11, LINEPROTO, and so on. Facility indication is followed by a value representing severity. The value 3 corresponds to the severity level called Error, which indicates an error condition.
--------
A client issues a DNS request to its local DNS server. The local DNS server does not have the information required. Which entity will finally send a DNS response to the client?

* the authoritative DNS server for the top-level domain

* the authoritative top-level domain and subdomain DNS servers

* **the client's local DNS server**

* the Internet Service Provider's DNS server

	Answer
	The correct answer is **the client's local DNS server**. When the local DNS server cannot find the queried domain in its database, which indicates that the local server is not authoritative for this domain, it will query the authoritative root DNS server for the top-level (root) domain. The root DNS server directs the query to the DNS server for the first subdomain of the queried domain name. The query directing process continues until the local server reaches the authoritative subdomain DNS server. The authoritative subdomain DNS server resolves the initially queried domain name and replies to the local DNS server. This is how the local DNS server gets the resolved IP address. It is then the local DNS who sends the response to the client.
--------
Which two Microsoft Windows commands will display the DNS server address configured on the host? (Choose two.) Need to find the answer

* ipconfig

* **ipconfig /all**

* net config

* netstat -f

* **nslookup**
--------
Refer to the exhibit. The administrator has configured Hot Standby Router Protocol (HSRP) to provide default gateway redundancy. Which statement correctly describes the behavior of the network?

* PC1 will be able to reach remote networks if either R1 or R2 fails.

* **PC1 will be able to reach remote networks while R1 is operational.**

* PC1 will not be able to reach remote networks if either R1 or R2 fails.

* PC1 will not be able to reach remote networks if R2 fails.

	Answer
	The correct answer is **PC1 will be able to reach remote networks while R1 is operational**. Because of the explicit default gateway configuration, the ARP table of PC1 has the default gateway IPv4 mapped to the R1 MAC address, and not to the virtual IP address of the HSRP group. When R1 fails, the PC1 ARP table will not be updated, and PC1 will not be able to reach R2, which would take over the role of the default gateway.
--------
For which network entity is the OSPF designated router/backup designated router (DR/BDR) selection performed?

* **for each multi-access segment**

* for each OSPF router ID

* for the entire OSPF area

* per transmission state of the link
--------
Where does a router that runs OSPFv2, and that has neighbor adjacencies established, store link-state advertisements (LSAs)? Need to find the answer

* **LSDB**

* Neighbors table

* Routing table

* SPF tree
--------
What is a way of mitigating social engineering attacks?

* Avoiding making copies of files on external memory devices.

* Avoiding using personal data to create a password.

* Assigning administration privileges only to people with technical knowledge.

* **Training users about correct security behaviors. (Ans)**
--------
Which two attack categories does the smurf attack belong to? (Choose two.) Need to find the answer

* **amplification**

* brute-force

* man-in-the-middle

* exfiltration

* **reflection**
--------
After the Cisco IOS **Software image is loaded and started**, from which three components can the device load its configuration? (Choose three.)

* DHCP server

* DNS server

* RAM

* **NVRAM**

* **SCP server**

* **TFTP server**

	Answer
	The correct answers are **NVRAM, SCP server, and TFTP server**. If there is an existing saved configuration file (startup-config) in NVRAM, it is executed. If the startup configuration file does not exist in NVRAM, the router may search for a network file server (TFTP, SCP, and so on). RAM stores the current configuration after it is loaded. A DHCP server can provide the URL of the configuration file, where the file can then be loaded from. DNS servers are not used for file transfers.
--------
You have restarted a router, which has the default booting procedure. During the reboot, the following messages appear on the console:

%Error opening tftp://255.255.255.255/network-confg (Timed out)
%Error opening tftp://255.255.255.255/cisconet.cfg (Timed out)
What can you conclude based on the messages? Need to find the answer

* The router will attempt to load the configuration from the NVRAM.

* The router configuration will be loaded from the TFTP server.

* The TFTP server URL is incorrect.

* **The configuration file is not found on the TFTP server.**

--------
Lab Sample 8 Begins:
--------------------

Consult the topology diagram and address table to understand the network connectivity and addressing. Not all systems are initially configured with IPv6 addresses. OSPFv3 is configured between routers.

Perform the following tasks:

Configure SRV1 (Ethernet0/0) with the IPv6 address that is the first available after the address assigned to SW3. Make sure that the ping from SRV1 to the R3 Ethernet0/0 is successful.

Configure PC1 and PC2 to auto-configure both their IPv6 addresses and their default gateways. The ping from PC1 to PC2 should be successful.

Configure the SW1 and SW2 IPv6 addresses and default gateways as listed in the Job Aids.

Configure the routers with link-local addresses so that each interface on a router has the same link-local address.

For R1, use fe80::1.

For R2, use fe80::2.

For R3, use fe80::3.

Which command is used to assign IPv6 addresses to PC1 and PC2?

* ipv6 address autoconfig

* **ipv6 address autoconfig default**

* ipv6 address dhcp

* ipv6 address 2001:db8:0:1::/64 eui-64 on PC1 and ipv6 address 2001:db8:0:2::/64 eui-64 on PC2

	Answer
	The correct answer is **ipv6 address autoconfig default**. The ipv6 address autoconfig command enables autoconfiguration for IPv6 address assignment only, but the default route is not injected into the routing table. The ipv6 address dhcp command requires a DHCP server to be installed. The ipv6 address 2001:db8:0:1::/64 eui-64 and ipv6 address 2001:db8:0:2::/64 eui-64 commands manually configure the IPv6 address prefix, where the host portion of the IPv6 address is calculated from the EUI-64 method.

Which IPv6 address is assigned to the SRV1 server?

* 2001:db8:0:3::1/128

* 2001:db8:0:3::30/64

* 2001:db8:0:3::30/128

* **2001:db8:0:3::31/64**

	Answer
	The correct answer is 2001:DB8:0:3::31/64. This is the first available IPv6 address after the IPv6 address assigned to SW3 VLAN 1 (2001:dbB8:0:3::30/64). The IPv6 subnet mask should be the same as assigned to SW3 VLAN1 (/64).

Use the show ipv6 route command, examine the routing table on the R1 router. What is the next-hop IPv6 address to the 2001:db8:0:2::/64 network?

* 2001:db8:0:2::2

* **fe80::2**

* fe80::3

* fe80::a8bb:ccff:fe00:6d00

	Answer
	The correct answer is **fe80::2.** The next-hop IPv6 address is a link-local IPv6 address of R2 Ethernet0/2. You have manually configured link-local IPv6 addresses on all R2 router interfaces to fe80::2.

Use the shutdown command, disable the R2 Ethernet0/2 interface. What is the next-hop IPv6 address to the 2001:DB8:0:2::/64 network when examining the IPv6 routing table on the R1 router?

* 2001:db8:0:2::2

* fe80::2

* **fe80::3**

* fe80::a8bb:ccff:fe00:6d00

	Answer
	The correct answer is **fe80::3**. Since you have disabled the link between R1 and R2, the routing protocol calculates a new path from R1 router to the 2001:db8:0:2::/64 network. The next-hop IPv6 address is a link-local IPv6 address of R3 Ethernet0/1. You have manually configured link-local IPv6 addresses on all R3 router interfaces to fe80::3.

What is the IPv6 default gateway address for the SW2 switch?

* 2001:db8:0:1::1

* **2001:db8:0:2::2**

* 2001:db8:0:2::20

* 2001:db8:0:2:a8bb:ccff:fe00:6e00

	Answer
	The correct answer is 2001:db8:0:2::2. The IPv6 default gateway for the SW2 switch is the IPv6 address configured on R2 Ethernet0/0. The IPv6 default gateway and SW2 VLAN1 IPv6 address should have the same IPv6 prefix (2001:DB8:0:2::/64).

Refer to the network diagram for the lab. What are two physical topologies of the router interconnections? (Choose two.)

* bus

* extended star

* **full mesh (Ans)**

* partial mesh

* **ring (Ans)**

* star 

Lab Sample 8 Ends:
------------------

--------
Which three of the following application characteristic values are determined in the service level specification phase when designing the quality of service (QoS) policy of a network? (Choose three.)

* generated data flows

* **required bandwidth**

* required responsiveness

* response criticality

* **tolerable jitter**

* **tolerable packet loss**

	Answer
	The correct answers are **required bandwidth, tolerable jitter, and tolerable packet loss**. When you specify the service levels for a class of traffic, you define specific values for delay and jitter, packet loss tolerance, required bandwidth, and time sensitivity. After the implementation of the QoS policy, the performance of your network can then be measured and evaluated against the specified service levels. You should identify the data flows generated by the application prior to determining service levels, in the first phase of policy design. Required responsiveness and response criticality are performed within the business audit phase, which precedes service-level specification.
--------
When a **network handles Voice over IP (VoIP) packets differently than HTTP packets**, which network feature is implemented?

* fault tolerance

* **quality of service**

* scalability

* security

	Answer
	The correct answer is quality of service. Quality of service (QoS) includes tools, mechanisms, and architectures that allow you to control how and when network resources are used by applications. QoS is especially important for prioritizing traffic when the network is congested. Scalability ensures that a network can easily accommodate more users and data transmission requirements, while security indicates how well the network is defended from potential threats. Fault tolerance indicates how resilient the network is in case of failure.
--------
Which statement is true regarding **subnet 192.168.1.64/26**?


* The broadcast address of this subnet is 192.168.1.95.


* The subnet supports 126 host addresses.


* The valid subnet mask for this subnet is 255.255.255.224. 


* **There are 6 bits available for addressing hosts.**

--------
Which network capability ensures that an endpoint, such as an IP phone, connects to the company network in a secure and automatic way?

* **802.1x**

* ACL

* DHCP

* VLAN

	Answer
	The correct answer is **802.1x**. VLANs segment the network, and ACLs limit traffic flows, but both must be manually configured on edge interfaces if additional mechanisms are not in place. DHCP provides network parameters based on VLAN membership, but doesn’t ensure any security.


--------
What are the three tasks of an **Intrusion Prevention System (IPS)**? (Choose three.)


* **blocking suspicious activity**


* inspecting suspicious activity


* **logging suspicious activity**


* **reporting suspicious activity**


* tracing suspicious activity

	Answer
	The correct answers are blocking suspicious activity, logging suspicious activity, and reporting suspicious activity. Inspecting and tracing suspicious activity falls out of the scope of an IPS system and is achieved separately.


--------

The devices in the topology are pre-configured with IP addressing and can communicate with each other. You need to configure and verify the time-related configuration which will allow devices to synchronize time in a pre-determined way.

Perform the following tasks:

Examine the current NTP and time zone configuration on the devices.

Configure R1 as the NTP master with stratum = 1.

Configure R2 and SW to synchronize time directly with R1.


After configuring R2 and SW to synchronize their clocks directly to R1, what are the stratum levels of R2 and SW?


* The R2 stratum level is 1 and the SW stratum level is 1.


* **The R2 stratum level is 2 and the SW stratum level is 2.**


* The R2 stratum level is 2 and the SW stratum level is 3.


* The R2 stratum level is 3 and the SW stratum level is 3.

	Answer
	The correct answer is The R2 stratum level is 2 and the SW stratum level is 2. Because both R2 and SW are synchronizing time directly with R1, they both have the same stratum value. Because R1 has a stratum value of 1, R2 and SW increment their values by one (to 2).


What is the maximum stratum level that you can configure on a Cisco device?


* 12


* **15**


* 21


* 24

On the SW switch, display the established NTP associations. What is the value displayed in the address column?


* ***~198.51.100.2 (Ans)**


* *198.51.100.2


* ~198.51.100.2


* 198.51.100.2

	Answer
	The correct answer is *~198.51.100.2. An asterisk (*)* next to a configured peer represents that the device is synced to this peer and using it as the master clock. A tilde (~) next to a configured peer represents that this is a configured master server.

--------
What are **two valid IPv6 address scopes for a unique local IPv6 address**? (Choose two.)


* global


* interface-local


* link-local


* **organization-local**


* **site-local**

	Answer
	The correct answers are organization-local and site-local. Unique local IPv6 addresses are equivalents of private IPv4 addresses. They can be considered globally unique, because the probability of duplication is extremely low. Unique local IPv6 addresses are routable inside of a limited area, such as a site. Also, unique local IPv6 addresses may be routed between a limited set of sites (within an organization), but are not expected to be routable on the global internet.


--------
When a particular VLAN is deleted, what happens to interfaces that were assigned to the deleted VLAN?


* They are reassigned to VLAN 1 automatically.


* They are put into err-disabled mode.


* **They become inactive.**


* The interface configuration is erased.

	Answer
	The correct answer is They become inactive. When a port is assigned to a non-existent VLAN or a VLAN that gets deleted, the port becomes inactive and is unable to communicate with the rest of the network. VLAN 1 is a factory default VLAN that is automatically assigned to an access port, unless its configured otherwise. Removing a VLAN does not change interface configuration.


--------
On a Cisco switch, which two commands would you use to identify ports that are configured as trunks? (Choose two.)


* **show interfaces status**


* show interfaces summary


* **show interfaces trunk**


* show ip interface brief


* show vlan brief

	Answer
	The correct answers are show interfaces status and show interfaces trunk. The show interfaces summary, show ip interface brief, and show vlan brief commands do not display information about switch ports configured as trunks.


--------
What is the purpose of the Cisco Wireless LAN Controller (WLC)?


* ensuring that firewall rules are enforced on wireless networks


* **managing multiple wireless access points (APs)**


* providing a wireless signal to end points


* routing traffic between wireless networks


--------
When an enterprise has to comply with strict data security regulations, which cloud deployment model should they use for their services?


* community


* hybrid


* **private**


* public


--------

The network switches must be configured to separate workstations and servers into different VLANs as displayed in the topology. To ensure inter-VLAN connectivity, router R1 is already pre-configured.

Ensure that the devices in one VLAN can communicate with each other. Perform the following tasks:

Configure IPv4 addressing on workstations and servers so that they belong to the appropriate subnet.

Configure the default gateway IPv4 address on workstations and servers.

Configure VLANs and trunking.

Do not change the default configuration on the Ethernet0/3 interface on SW2.

When configuring devices and verifying device configurations, use the information provided in the documentation, that is in the topology figure and Job Aids.


When you examine the MAC address table on SW2, which VLAN does MAC aa-aa-aa-aa-22-22 belong to?


* 1


* **65**


* 80


* 1001


* 1005

	Answer
	The correct answer is 65. The MAC address aa-aa-aa-aa-22-22 belongs to PC2 and as such is a member of VLAN 65. VLAN 80 contains both server nodes. VLAN 1001 is not present in this lab topology and VLAN 1005 is a reserved FDDI/Token Ring VLAN.


On SW2, verify the administrative and operational switching modes on interface Ethernet0/3. Which statement correctly describes the administrative mode and operational mode values?


* Administrative mode is access and operational mode is access.


* Administrative mode is dynamic-auto and operational mode is access.


* Administrative mode is dynamic-desirable and operational mode is access.


* **Administrative mode is dynamic-desirable and operational mode is trunk.**


* Administrative mode is trunk and operational mode is trunk.

	Answer
	The correct answer is **Administrative mode is dynamic-desirable and operational mode is trunk.** Administrative mode displays what you have configured on the interface. Operational mode displays the actual status of the interface. When manually configuring access or trunking, administrative and operational mode have identical values. When you configure Dynamic Trunking Protocol (DTP) to negotiate switching status, administrative and operational mode differ. Cisco recommends disabling DTP on a switch."

Examine the topology and the configuration. On PC2, when you use the ping command to check connectivity to Server 1, what is the order of the devices that packets traverse?


* PC2 > SW1 > SW2 > R1 > SW2 > Server1


* PC2 > SW2 > R1 > SW1 > Server1


* PC2 > SW2 > SW1 > R1 > Server1


* **PC2 > SW2 > SW1 > R1 > SW1 > Server1**

Which interfaces on SW1 are trunk interfaces?


* E0/0 and E0/1


* **E0/0 and E0/3**


* E0/1 and E0/2


* E0/1 and E0/3

	Answer
	The correct answer is E0/0 and E0/3. SW1 has four interfaces. The interfaces E0/0 and E0/3 are connected to a router and another switch, respectively. As such, those two interfaces are set up as trunk interfaces in order to carry multiple VLANs. The interfaces E0/1 and E0/2 are connected to end nodes, and are configured as access interfaces.


Which three statements about IPv4 addresses are true? (Choose three.)


* **8.0.0.0 is a public address.**


* **10.8.0.0 is a private address.**


* **127.0.0.1 is a reserved address.**


* 172.30.0.0 is a public address. -> is a private range


* 192.170.0.0 is a private address. -> is a public range

	Answer
	The correct answers are 8.0.0.0 is a public address, 10.8.0.0 is a private address, and 127.0.0.1 is a reserved address. 192.170.0.0 is a public IPv4 address, and 172.30.0.0 is a private IPv4 address.


--------
What is the maximum cable length of an unshielded twisted-pair (UTP) cable that still guarantees full connectivity?


* 80 m


* **100 m**


* 120 m


* 150 m

	Answer
	The correct answer is 100 m. Maximum UTP cable length is limited due to physical limitations of copper wires, where signal strength degrades with distance.

--------
When creating and maintaining the MAC address table, which two activities does a switch perform? (Choose two.)


* It adds the destination MAC address in the frame and the incoming port number.


* It adds the destination MAC address in the frame and the outgoing port number.


* **It adds the source MAC address in the frame and the incoming port number.**


* It resets the aging timer of all the entries related to the incoming port.


* **It resets the aging time of the MAC table entry for the source MAC address.**

	Answer
	The correct answers are It adds the source MAC address in the frame and the incoming port number and It resets the aging time of the MAC table entry for the source MAC address. A switch uses the destination MAC address to decide whether to forward or flood a frame. The destination MAC address is not stored in the MAC address table. The aging timer is reset for the source MAC address entry each time the switch receives a frame from that source MAC address.


--------
When configuring an IPv4 static route pointing to the **next-hop IPv4**, which command should you use?


* **ip route 172.16.1.0 255.255.255.0 172.16.2.1**


* ip route 172.16.1.0 net-mask 255.255.255.0 next-hop 172.16.2.1


* ip route 172.16.1.0/24 172.16.2.1


* ip route static 172.16.1.0 net-mask 255.255.255.0 next-hop 172.16.2.1

	Answer
	The correct answer is ip route 172.16.1.0 255.255.255.0 172.16.2.1. When configuring a static route, you must specify an IPv4 destination network (172.16.1.0 255.255.255.0), then use the IPv4 address of the next-hop router (172.16.2.1).


--------
When an access port is enabled with the PortFast feature, which two STP states are bypassed? (Choose two.)


* administratively down


* blocking


* forwarding


* **learning**


* **listening**


--------
If a port is still a designated or root port at the end of the learning state, which state will it enter?


* blocking


* disabled


* **forwarding**


* learning


* listening

	Answer
	The correct answer is forwarding. This port sends and receives all data frames on the bridged port. A blocked port only listens to BPDUs (Bridge Protocol Data Units), and it does not forward any frames. Disabled ports do not participate in frame forwarding. A port changes to a learning state after a listening state. After a blocking state, the designated port moves to a listening state.


--------
In this task you will configure link aggregation and examine its effects on STP topology. The network devices are pre-configured with basic connectivity parameters and Rapid Per VLAN Spanning Tree Protocol Plus (Rapid PVSTP+) to prevent traffic loops. The topology consists of three segments: workstations, servers, and connecting segment. All devices have their basic configurations in place, including hostnames and IP addresses.

Carefully examine the device configurations. There are some mistakes in the interface configuration on network devices. First, find the mistakes and correct them. Then, perform the following configuration tasks, and answer the questions.

Create EtherChannel links between the switches using the Link Aggregation Control Protocol (LACP).

Configure the switches so SW3 is the root switch for VLAN 20 and SW1 is the root switch for VLAN 10.

Ensure there is full connectivity within each VLAN (that is, you can successfully issue the ping command between PC1 and PC2, between SRV1 and SRV2, and between switches).


On SW2, when you see the summary information for aggregated link. What is the status code or flags of the port channel Po23? Need to find the answer


* down (D)


* **Layer2 - In use (SU)**


* stand-alone (I)


* suspended (s)

Issue the ping command from PC1 to PC2. What is the path that packets traverse?


* **SW1 > SW3 > SW2**


* SW1 > SW3 > SW4 > SW2


* SW1 > SW4 > SW2


* SW1 > SW4 > SW3 > SW2



Refer to the exhibit. The figure represents the topology resulting from STP calculations after configuring the Layer 2 EtherChannel. Which VLAN does the topology in the exhibit represent?


* VLAN 1


* VLAN 10


* **VLAN 20**


* VLAN 99



--------

The lab is prepared with the devices that are represented in the topology diagram. All devices have their basic configurations in place, including hostnames and IP addresses. Static routing is configured on all devices.

Perform the following tasks:

On R1, configure port forwarding so that Telnet connections to SRV1 are possible from outside networks. For the public IPv4 address, use the IPv4 address of the Ethernet 0/3 interface. For the publicly accessible port, use 2323.

Ensure that traffic from the 10.10.2.0/24 subnet is dynamically translated, using the following pool of public addresses: 209.165.202.128/27.

Ensure that traffic from the 10.10.1.0/24 subnet is translated to the IPv4 address of the Ethernet 0/3 interface on R1.

Which command should you use to access SRV1 from SRV2 using Telnet?


* telnet 10.10.2.20 23


* telnet 10.10.2.20 2323


* telnet 198.51.100.2 23


* **telnet 198.51.100.2 2323**

When you use Telnet to connect from SRV2 to the IP 198.51.100.2 and port 2323, what message should you get?


* % Connection refused by remote host


* Password required, but none set


* **Welcome!**


* Please log in!



On PC1, issue the ping command to verify connectivity to SRV2. What is the result that you see?


* .....


* **U.U.U**


* !.!.!


* !!!!!

Examine the routing table on R2. What does the subnet 209.165.202.128/27 in the static entry refer to?


* **SRV1 to R1 public segment**


* R1 to R2 public segment


* R2 to SRV2 public segment


* SRV1 to R1 private segment




--------
Which part of the Open Shortest Path First (OSPF) process is omitted **if two routers are connected with a point-to-point link?**


* **Designated router/Border designated router (DR/BDR) election**


* exchange of hello packets


* exchange of link-state database (LSDB) summary


* Shortest Path First (SPF) calculation

**Designated router/Border designated router (DR/BDR) election**

	The correct answer is Designated router/Border designated router (DR/BDR) election. Since there can be only two routers on a point-to-point connection, there is no need for a DR/BDR election. DR/BDR elections happen in point-to-multipoint topologies. OSPF exchange of hello packets, exchange of LSDB summaries, and SPF calculation are necessary procedures in an OSPF operation. These procedures are always performed, regardless of the link connection type.

--------
What is a way of mitigating social engineering attacks?


* Avoiding making copies of files on external memory devices.


* Avoiding using personal data to create a password.


* Assigning administration privileges only to people with technical knowledge.


* **Training users about correct security behaviors.**


--------
Which two statements describe examples of social engineering attacks? (Choose two.)


* Cracking a user password using personal data related to the victim.


* Defacing a website and explaining the political ideology behind the attack.


* Delivering a DoS attack from a server trusted by all company users.


* **Sending an email from a seemingly legitimate address with writing that adopts typical sender language.**


* **Sending an infected USB with a magazine.**

	**Ans:**
	Sending an email from a seemingly legitimate address with writing that adopts typical sender language.
	Sending an infected USB with a magazine.

--------
This lab tests your knowledge about basic security configuration of the device management plane. IP addressing on all devices is already configured.

The SW2 switch in the topology has already been configured. You will have no direct access to this device, however, you can access it remotely from other devices in the topology.

SW2 already has a local database of user credentials. The Device Access table provides detailed information.

In the task, you will configure the SW1 switch and the R1 router.

On SW1, perform the following tasks:

Restrict access to the privileged EXEC mode. Configure the protected password CiscoSW1! using the default encryption type. Configure the unprotected password Cisco123! and ensure it is obfuscated in the configuration file (that is, it does not show in the plain text).

Define two users in the local database, using the following credentials:

username

password

privilege level

1

TECH

CiscoTech1!

default

2

ADMIN

CiscoAdm1!

15

On R1, perform the following tasks:

Restrict access to the privileged EXEC mode. Configure the protected password CiscoR1! using the default encryption type.

Configure the unprotected password Cisco123! and ensure it is obfuscated in the configuration file.

Protect the access to the console by requiring a password to access the console. Set the console password to Cisco333!.


From PC1, connect to SW1 using Telnet with the password Cisco111!. Which password did you use to access the privileged EXEC mode on SW1?


* Cisco111!


* Cisco123!


* CiscoAdm1!


* **CiscoSW1!**


* CiscoTech1!

On R1, at the command prompt, issue the exit command as many times as necessary until you get the "Press RETURN to get started" prompt. Which password do you have to type to access the USER exec mode?


* Cisco123!


* Cisco333!


* CiscoR1!


* **password is not required**

Which number represents the default encryption type of the protected password used to restrict access to the privileged EXEC mode?


* **4**
* 5
* 8
* 9

Examine the Device Access table in the Job Aid. There are four users configured on SW2. The SW2 switch console line access is set to privilege level 5. Presuming command privileges are set to default, which username should you use to be able to change the SW2 configuration?


* admin
* monitor
* operator
* **superadmin**

From PC1, connect to SW2 using Telnet and verify the console line configuration. How long can a user be inactive while still connected to the console of SW2?


* **60 minutes and 7 seconds**
* 60 minutes within 7 days
* 67 minutes
* 67 seconds

From PC2, connect to SW2 using Telnet. Examine the running configuration. Which time zone is set?


* CET
* **LJUB**
* MDT
* PST

--------


--------
Cisco routers and switches use IOS (Internetwork Operating System) commands to display information about the device's status, interfaces, and configuration. The "show" commands are some of the most commonly used for troubleshooting and monitoring the network. Below is a list of some fundamental "show" commands and their explanations:

1. `show version`
   - Displays information about the device's hardware and software, including the IOS version, system uptime, and device model.

2. `show running-config`
   - Displays the current running configuration of the device, which is stored in RAM.

3. `show startup-config`
   - Shows the saved configuration that is stored in NVRAM and will be used to boot the device.

4. `show interfaces`
   - Provides detailed information about all the interfaces on the device, including IP addresses, status, packet statistics, and errors.

5. `show ip interface brief`
   - Offers a summary of the interfaces, showing their IP addresses, status, and protocol states.

6. `show protocols`
   - Displays the status of configured Layer 3 protocols, such as IP, on the device.

7. `show ip route`
   - Shows the device's IP routing table, including connected, static, and dynamically learned routes.

8. `show arp`
   - Displays the Address Resolution Protocol (ARP) table, which maps IP addresses to MAC addresses.

9. `show mac address-table`
   - Shows the MAC address table (also known as the CAM table) on a switch, which maps MAC addresses to switch ports.

10. `show vlan`
    - Displays VLAN (Virtual LAN) information, including VLAN IDs and associated ports on a switch.

11. `show cdp neighbors`
    - Lists information about neighboring Cisco devices discovered using Cisco Discovery Protocol (CDP).

12. `show cdp neighbors detail`
    - Provides detailed information about each CDP neighbor, including IP addresses and device capabilities.

13. `show lldp neighbors`
    - Similar to the CDP commands, but for devices using the Link Layer Discovery Protocol (LLDP), which is vendor-neutral.

14. `show ip ospf neighbor`
    - Lists OSPF neighbor relationships and states if the device is using the OSPF routing protocol.

15. `show ip eigrp neighbors`
    - Displays EIGRP neighbor relationships if the device is using EIGRP as its routing protocol.

16. `show ip bgp`
    - Shows the BGP table with all the BGP routes if the device is configured for BGP.

17. `show access-lists`
    - Displays all access lists configured on the device and their hit counts.

18. `show users`
    - Lists users currently logged into the device and their connection method.

19. `show flash:`
    - Shows the contents of the device's flash memory, including the IOS image(s) and other files.

20. `show logging`
    - Displays the device's logging information, such as syslog messages and severity levels.

21. `show processes`
    - Provides information about the active processes running on the device and their CPU usage.

22. `show memory`
    - Displays memory usage statistics for the device.

23. `show tech-support`
    - Generates a detailed report with a wide range of information about the device's state, which can be used for troubleshooting or provided to Cisco technical support.

This is not an exhaustive list, as Cisco devices have a vast number of "show" commands, each providing different types of information. The specific "show" commands available can vary depending on the IOS version and the device model.


On Cisco switches, the `show interfaces` command is very versatile and can be used to display a range of details about the switch's interfaces. Here are some of the most common uses of the `show interfaces` command and related commands to check interface status and statistics:

1. `show interfaces`
   - This command displays detailed information about all interfaces on the switch, including status (up/down), protocol state, MAC address, speed, duplex mode, and various statistics such as input/output packets and errors.

2. `show interfaces status`
   - Provides a quick summary of the interface status, including the VLAN assignment, duplex mode, speed, type, and whether the port is in an error-disabled state.

3. `show interfaces description`
   - Displays the description for each interface (if configured) along with the interface status and protocol state, which is useful for quickly identifying the purpose of each interface.

4. `show interfaces switchport`
   - Shows detailed information about a specific interface's switchport settings, including access or trunk mode, VLAN membership, and voice VLAN information.

5. `show interfaces trunk`
   - Lists all trunk interfaces on the switch and shows their encapsulation (dot1q or ISL), native VLAN, and allowed VLANs on the trunk.

6. `show interfaces [interface-id]`
   - Displays detailed information for a specific interface, where `[interface-id]` is the identifier of the interface (e.g., `GigabitEthernet1/0/1`). This command provides in-depth statistics and status for a single interface.

7. `show interfaces counters`
   - Provides detailed traffic statistics for all interfaces, such as the total number of packets and bytes transmitted and received, including errors.

8. `show interfaces counters errors`
   - Displays error counters for all interfaces, which can help in identifying problematic interfaces with high error rates.

9. `show interfaces [interface-id] switchport`
   - Shows the switchport information for a specific interface, including VLAN assignments and trunking details.

10. `show interfaces [interface-id] status`
    - Shows the link status, speed, duplex mode, and VLAN assignment for a single specified interface.

11. `show interfaces vlan [vlan-id]`
    - Displays information about a specific VLAN interface, including IP address, status, and protocol state.

12. `show interfaces summary`
    - Provides a summary of the interface statuses, including the number of interfaces that are administratively down, down, up, or trunking.

* The `show interfaces` commands are invaluable for network troubleshooting and monitoring. They allow network administrators to assess the status, performance, and configuration of switch ports and to quickly identify and resolve issues with network connectivity or performance.

* To show the interface administrative mode and operational mode: `show inter eth0/3 switchport`

--------
Which three types of booting are supported on servers? (Choose three.)

* **booting from internal storage**
* **booting from LAN**
* **booting from SAN**
* booting from WAN
* booting from wireless
--------
Which two characteristics apply to small office/home office (SOHO) routers? (Choose two.)

* They are more expensive than enterprise routers.
* They are more reliable than enterprise routers.
* **They have a web-based administration interface.**
* **They have integrated security functionality.**
* They perform intensive routing tasks.

    * They have a web-based administration interface.
    * They have integrated security functionality.
	-
	SOHO routers usually route between a small number of subnets, thereby freeing resources to perform other networking tasks. SOHO routers integrate functionalities provided by other networking devices, such as switches, firewalls and DNS servers. Enterprise-grade routers are designed for very high reliability and are more reliable than SOHO routers.
--------
Which two parameters can be used for metric calculations? (Choose two.)

* IP Address
* **Hop count**
* Link Up/Downtime
* **Bandwidth**
* Default Route
* Local Routes

    * Hop count
    * Bandwidth
	-
	The metric calculation is a critical component of any routing protocol. The routing protocol uses multiple factors to calculate the metric for a path, such as Hop Count, Bandwidth, Delay, and Cost.
--------
What is the network ID of the IPv6 address 2001:db8:deca:abce:45eb:27ff:feba:fa38/48?

* 2001::
* 2001:db8::
* **2001:db8:deca::**
* 2001:db8:deca:abce::

* **2001:db8:deca::**
	-
	Each hexadecimal character represents 4 binary bits. The first 12 characters correspond to 48 bits. 2001:db8:deca:abce:: would have the /64 prefix, 2001:db8:: would have the /32 prefix, and 2001: would have the /16 prefix.
	
	**Note:**
		IPv6 addresses are 128 bits long, and are written as eight sections of 16 bits each, using hexadecimal representation. The sections range from 0 to FFFF, and are separated by colons. Leading zeros in each section might be omitted.
		As per the question - the subnet value is /48. Each section consist of 16 bits. So 16*8 = 48. The answer is `2001:db8:deca::`
--------
In a wireless IEEE 802.11 implementation, what is the most secure option to protect user traffic?

* WEP
* WPA
* WPA2
* **WPA3**

	WPA3
	-
	Wi-Fi Protected Access 3 (WPA3) is a replacement of WPA2 and is the next generation of wireless security standards that provides more resiliency to network attacks.
--------
Which three elements are parts of an HTTP status line? (Choose three.)

* **protocol version**
* requested method
* **status code**
* **status message**
* target URL

	* **protocol version**
	* **status code**
	* **status message**
--------
Which task makes configuring network devices more efficient and reduces errors?

* compliance checks
* data collection and telemetry
* **device provisioning**
* device software management

	device provisioning
	-
	The correct answer is device provisioning. Device provisioning configures network devices more efficiently, faster, and with fewer errors because human interaction with each network device is decreased. Device software management controls the download and deployment of software updates. Data collection and telemetry collects data from network devices and telemetry on network behavior. Compliance checks audit large groups of network devices for configuration errors and automatically make the appropriate corrections with built-in regression tests.

--------
Which three Wi-Fi standards support the 5 GHz spectrum? (Choose three.)
* **802.11a**
* **802.11ac**
* 802.11b
* 802.11g
* **802.11n**

	* 802.11a
	* 802.11ac
	* 802.11n
--------
When an access point (AP) is operating in local mode, on which network device is wireless client traffic switched?
* on a network switch
* **on a wireless access controller (WLC)**
* on the egress AP
* on the ingress AP

	on a wireless access controller (WLC)
	-
	In local mode, the AP sends all the client traffic to the WLC. The network switch would switch the traffic between two stand-alone APs. The egress and ingress points have no influence on the switching decision.
--------
What is the broadcast address of segment B?
* 172.16.31.7
* 172.16.31.8
* **172.16.31.15**
* 172.16.31.16

	172.16.31.15
--------
How many end devices can be addressed in segment D prefix/27?
The correct answer is 30. Segment D has a network prefix of /27, which means that there are 32 possible addresses to be assigned, one of which is reserved for the network address and one for the broadcast address. That leaves 30 IPv4 addresses that can be assigned to end devices.
* 6
* 14
* **30**
* 62

	30
	-
	Segment D has a network prefix of /27, which means that there are 32 possible addresses to be assigned, one of which is reserved for the network address and one for the broadcast address. That leaves 30 IPv4 addresses that can be assigned to end devices.
--------
On R4, issue the ping command sourced from the address allocated to the interface E0/0 and test connectivity to the internet test address. What is the resulting output?
* Ping is not successful because an ACL is blocking traffic.
* Ping is not successful because IP routing is not enabled on R4.
* Ping is partially successful (30%).
* **Ping is successful (80-100%).**

	Ping is successful (80-100%)
	.-
	The correct answer is Ping is successful (80-100%). If everything was correctly configured in the lab, then the ping to the internet test address should be successful.
--------
A device running a Windows OS has the IP address 169.254.254.254. Which of the following statements is true?
* **The address is automatically configured by the device itself.**
* The device is reachable via the internet.
* The IP address is used to communicate with the default gateway.
* The IP address is a loopback address.

	The address is automatically configured by the device itself.
	-
	The address space 169.254.0.0/16 is reserved for link-local IPv4 addresses. An end-device that supports IPv4 link-local addresses self-assigns an IPv4 address from the 169.254.0.0/16 range, when the address is not specified otherwise. The link-local IPv4 address can be used only for local network connectivity and will not be routed.
--------
Which three statements about IPv4 addresses are true? (Choose three.)
* **8.0.0.0 is a public address.**
* **10.8.0.0 is a private address.**
* **127.0.0.1 is a reserved address.**
* 172.30.0.0 is a public address.
* 192.170.0.0 is a private address.

	* 8.0.0.0 is a public address.
	* 10.8.0.0 is a private address.
	* 127.0.0.1 is a reserved address.
	-
	192.170.0.0 is a public IPv4 address, and 172.30.0.0 is a private IPv4 address.
--------
What is the default aging timer value on Cisco switches?
* 180 seconds
* 240 seconds
* **300 seconds**
* 360 seconds

	**300 seconds**
--------
After receiving an Ethernet frame, a switch examines the destination MAC address, and forwards the frame out of all ports except the incoming port. In which communication types can this behavior occur?
* in broadcast and multicast communication
* in broadcast communication
* **in broadcast, multicast, and unicast communication**
* in unicast communication

	in broadcast, multicast, and unicast communication
	-
	An Ethernet switch forwards a frame out of all ports except the incoming port when the intended recipients are all devices in a network, like in broadcast communication. It also forwards a frame out of all ports except the incoming port when communication is sent to a specific group of hosts, which is the case in multicast communications. In unicast communication, the switch will forward the frame out of all ports except the incoming port only when it does not have the destination MAC address in its MAC table.
--------
Which is the correct subnet mask for a host route?
* 0.0.0.0
* 255.254.0.0
* 255.255.255.254
* **255.255.255.255**

	255.255.255.255
	-
	The host route is a static route for a single host. A single host is specified by the subnet mask of 255.255.255.255. The host route has all the bits in the network mask set to 1, for IPv4 this can be 192.168.1.1/32, and for IPv6 it could be ::1/128.
--------
For an administrator to be able to access the Layer 2 switch S1 from the internet, which IP connectivity parameters do you have to configure on the S1 switch?
* **default gateway to 192.168.3.254**
* default route via 192.168.3.254
* IPv4 address in the 209.168.200.224/27 subnet
* static route to 209.168.200.254/27

	default gateway to 192.168.3.254 which is the edge router in this situation
	-
	For Switch S1 to be able to replay and respond as the administrator manages it, it must have a default gateway set. On a Layer 2 switch, you cannot configure routes, since IP routing is not enabled. For the switch virtual interface to work, the VLAN must be associated and active on at least one physical port.

--------
How many bits does the subnet mask consist of?
* 16
* 24
* **32**
* 48

	32
	-
	The subnet mask consists of 32 bits, just as the address does. It uses ones and zeros to indicate which bits of the address are network and subnet bits, and which bits are host bits.
--------
What are two differences between the RADIUS and TACACS+ protocols? (Choose two.)
* **RADIUS combines authentication and authorization, while TACACS+ implements two separate processes.**
* RADIUS encrypts the entire payload, while TACACS+ encrypts only the password.
* RADIUS is a TCP-based protocol, while TACACS+ is a UDP-based protocol.
* **RADIUS is a UDP based protocol. TACACS+ is a TCP based protocol.**
* RADIUS supports bidirectional authentication, while TACACS+ supports only unidirectional authentication.

	* RADIUS combines authentication and authorization, while TACACS+ implements two separate processes.
	* RADIUS is a UDP based protocol. TACACS+ is a TCP based protocol.
	-
	RADIUS is an open standard that combines authentication and authorization services into a single process. TACACS+ is a Cisco proprietary security mechanism that can be used only for authorization and accounting while using another method of authentication. TACACS+ uses the Transmission Control Protocol (TCP) for all three services.
--------
Refer to the exhibit. In an 802.1X implementation, what are the roles of the devices shown?
* A: authenticator, B: supplicant, C: authentication server
* A: client device, B: supplicant, C: authentication server
* **A: supplicant, B: authenticator, C: authentication server**
* A: supplicant, B: client device, C: authentication server

	A: supplicant, B: authenticator, C: authentication server
	-
	A supplicant is a workstation with 802.1X-compliant client software. An authenticator acts as a proxy between the supplicant and an authentication server. An authentication server authenticates supplicants connecting to a switch port.
--------
Which feature of PVST+ is not available in RSTP?
* fast convergence on topology changes
* per-port STP
* **per-VLAN STP instance**
* edge ports

	per-VLAN STP instance
	-
	PVST+ is used on VLANs, while RSTP is used in LANs. Convergence is the state of a set of routers that have the same topological information about the internetwork where they are connected. Per-port STP is available in both PVST+ and RSTP, and PVST+ PortFast corresponds with the RSTP edge port concept.
--------
If a port is still a designated or root port at the end of the learning state, which state will it enter?
* blocking
* disabled
* **forwarding**
* learning
* listening

	forwarding
	-
	This port sends and receives all data frames on the bridged port. A blocked port only listens to BPDUs (Bridge Protocol Data Units), and it does not forward any frames. Disabled ports do not participate in frame forwarding. A port changes to a learning state after a listening state. After a blocking state, the designated port moves to a listening state.
--------
Examine the configurations of the switches SW1 and SW2. SW2 cannot obtain Layer 2 information from SW1 using CDP. Why?
* because CDP is disabled on the interface connecting to SW1
* **because CDP is globally disabled on SW2**
* because the interface connecting to SW1 is down
* because the interface connecting to SW1 is in the wrong VLAN
* because STP is blocking the interface connecting to SW1

	because CDP is globally disabled on SW2
	-
	The Cisco Discovery Protocol works as long it is globally enabled and not disabled on specific interfaces connecting two devices, and the two devices have L1 and L2 connectivity.
--------
What is the IP address of the R2 interface connecting to R1?
* 10.10.1.3
* 192.168.3.1
* **192.168.3.2**
* 192.168.3.3

	192.168.3.2
	-
	By issuing the show cdp neighbors detail command on R1, you are able to get the IPv4 address of R2's interface connecting to R1.
--------
What are the ports that interconnect switches SW1 and SW2?
* **SW1 Ethernet0/0 and SW2 Ethernet0/0**
* SW1 Ethernet0/0 and SW2 Ethernet0/1
* SW1 Ethernet0/1 and SW2 Ethernet0/0
* SW1 Ethernet0/1 and SW2 Ethernet0/1

	SW1 Ethernet0/0 and SW2 Ethernet0/0
	-
--------
In the topology you discovered in this exercise, can R1 obtain information about SW1 using CDP?
* **No, because R1 and SW1 are not directly connected.**
* No, because STP is blocking the connection between R1 and SW1.
* Yes, because R1 and SW1 are directly connected.
* Yes, because R1 and SW1 both have CDP enabled.

	No, because R1 and SW1 are not directly connected.
	-
--------
How many static routing entries did you have to add to the IPv4 routing table on R3?
* **1**
* 2
* 3
* 6

	1	
--------
Trace the path that IPv4 packets take from PC1 to SRV1. What is the hop sequence that the packets follow?
* **PC1 > R1 > R2 > R3 > SRV1**
* PC1 > R1 > R2 > R3 > SW3 > SRV1
* PC1 > R1 > R3 > SW2 > SRV1
* PC1 > SW1 > R1 > R2 > R3 > SRV1

	PC1 > R1 > R2 > R3 > SRV1
	-
	SW1 and SW3 do not participate in Layer 3 processing of either ICMP or UDP messages that are generated by the traceroute tool. Therefore, switches do not respond with ICMP replies. If the static routing was correctly configured as instructed, the traceroute traffic should flow from PC1 through R1 to R2, and terminate at SRV1.
--------
On R3, shut down the interface toward R2. On PC1, issue the ping command toward the IPv4 address of SRV1. What is the result?
* an "unreachable network" error is returned
* ping is only partly successful (20-30%)
* ping is successful (80-100%)
* **ping is unsuccessful (0%)**

	ping is unsuccessful (0%)
	-
	If static routing was correctly configured and connection between R2 and R3 disabled, the ping is unsuccessful, because no traffic can pass between R2 and R3. The unreachable network error is returned if no route (default or otherwise) exists on PC1 to the network of SRV1.
--------
Trace the path that IPv4 packets take from PC1 to SRV1. What is the hop sequence that the packets follow?
* **PC1 > R1 > R2 > R3 > SRV1**
* PC1 > R1 > R2 > R3 > SW3 > SRV1
* PC1 > R1 > R3 > SW2 > SRV1
* PC1 > SW1 > R1 > R2 > R3 > SRV1

	PC1 > R1 > R2 > R3 > SRV1
--------
Refer to the exhibit. You must ensure full connectivity in the network. When configuring trunking on SW3, which configuration would you use?

	SW3(config)# interface range GigabitEthernet0/1-2 SW3(config-if-range)# switchport mode trunk
	SW3(config-if-range)# switchport trunk allowed vlan 10,20,30 SW3(config-if-range)# switchport trunk native vlan 39 SW3(config-if-range)# end
	SW3# configure terminal
	SW3(config)# vlan 10,20,30
	SW3(config-vlan)# end
--------
In order to allow SNMP traffic to flow throughout the network, which two communication scenarios must be allowed? (Choose two.)
* TCP to port 161
* TCP to port 162
* UDP and TCP to port 161
* UDP and TCP to port 162
* **UDP to port 161**
* **UDP to port 162**

	* UDP to port 161
	* UDP to port 162
	-
	SNMP uses the UDP transport mechanism to retrieve and send management information. The SNMP manager polls the SNMP agents and queries the MIB via SNMP agents on UDP port 161. The SNMP agent can also send triggered messages called traps to the SNMP manager, on UDP port 162.
--------
Which three SNMP messages are sent from an SNMP agent to an SNMP manager? (Choose three.)
* GetRequest
* GetNextRequest
* **InformRequest**
* **Response**
* SetRequest
* **Trap**

	* InformRequest
	* Response
	* Trap
	-
	GetRequest, GetNextRequest and SetRequest are SNMP messages that an SNMP manager sends to an SNMP agent.
--------
Which command would you use to verify the number of excluded addresses on a router configured as a DHCP server?
* show ip dhcp bindings
* show ip dhcp conflict
* show ip dhcp database
* **show ip dhcp pool**

	show ip dhcp pool
	-
	To display a list of all IPv4 address-to-MAC bindings, you can use the show ip dhcp binding command. The show ip dhcp database command displays information about the DHCP server database agent, and the show ip dhcp conflict command displays the address conflicts found by a DHCP server when addresses are offered to the client.
--------
A client issues a DNS request to its local DNS server. The local DNS server does not have the information required. Which entity will send a DNS response to the client?
* the authoritative DNS server for the top-level domain
* the authoritative top-level domain and subdomain DNS servers
* **the client's local DNS server**
* the Internet Service Provider's DNS server

	the client's local DNS server
	-
	When the local DNS server cannot find the queried domain in its database, which indicates that the local server is not authoritative for this domain, it will query the authoritative root DNS server for the top-level (root) domain. The root DNS server directs the query to the DNS server for the first subdomain of the queried domain name. The query directing process continues until the local server reaches the authoritative subdomain DNS server. The authoritative subdomain DNS server resolves the initially queried domain name and replies to the local DNS server. This is how the local DNS server gets the resolved IP address. It is then the local DNS who sends the response to the client.
--------
Routers communicate First Hop Redundancy Protocol (FHRP) information between each other through hello messages. What is this mechanism called?
* EtherChannel
* **keepalive**
* link-state
* VLAN tagging

	keepalive
	-
	EtherChannel is a technology that enables link aggregation. A link-state router uses the link-state information to create a topology map and to select the best path to all destination networks in the topology. Switches use a process called VLAN tagging, in which the sending switch adds another header to the frame before sending it over the trunk.
--------
Two routers, A and B, are part of the Hot Standby Router Protocol (HSRP) standby group. There was no priority configured, and router A with the highest IP address for this HSRP group. Which statement is correct?
* Router A will be in the ACTIVE state and router B will be in the ACTIVE state.
* **Router A will be in the ACTIVE state and router B will be in the STANDBY state.**
* Router A will be in the LISTEN state and router B will be in the STANDBY state
* Router A will be in the STANDBY state and router B will be in the STANDBY state.

	Router A will be in the ACTIVE state and router B will be in the STANDBY state.
	-
	In normal operation, one router is always active and the other on standby, waiting to take over if the active router fails.
--------
Which command would you use to configure a router ID on a Cisco router?
* R1 (config-router)# ip router-id ip-address
* **R1 (config-router)# router-id ip-address**
* R1 (config)# ip router-id ip-address
* R1 (config)# router-id ip-address

	R1 (config-router)# router-id ip-address
	-
	For the network device administrator to configure a router ID on a router, the router-id ip-address command is used. The ip router-id ip-address, ip router-id ip-address, and router-id ip-address commands do not configure router IDs.
--------
When determining the OSPF router ID, what is the last action that the router will perform?
* Choosing the highest IPv4 address on a loopback interface.
* **Choosing the highest IPv4 address on an active interface.**
* Choosing the lowest IPv4 address on a loopback interface.
* Choosing the lowest IPv4 address on an active interface.

	Choosing the highest IPv4 address on an active interface.
	-
	The router will set the OSPF router ID to the manually configured value. If the OSPF router ID is not configured, then the router will use the highest IPv4 address on a loopback interface for the OSPF router ID. When neither the manual nor loopback-based router ID is determined, the last action the router performs is to use the highest IPv4 address of an active interface.
--------
Which two statements describe examples of social engineering attacks? (Choose two.)
* Cracking a user password using personal data related to the victim.
* Defacing a website and explaining the political ideology behind the attack.
* Delivering a DoS attack from a server trusted by all company users.
* **Sending an email from a seemingly legitimate address with writing that adopts typical sender language.**
* **Sending an infected USB with a magazine.**

	* Sending an email from a seemingly legitimate address with writing that adopts typical sender language.
	* Sending an infected USB with a magazine.
	-
	Social engineering is the process of manipulating people in order to capitalize on expected behaviors. Social engineering often involves utilizing social skills, relationships, or understanding of cultural norms to manipulate people inside a network to provide the information that is needed to access the network. Sending a USB with the right magazine or sending an email from a known address are methods of manipulating people. DoS attacks, password cracking, and website defacing are not based on manipulation, even if the information is related to specific users.
--------
What is a way of mitigating social engineering attacks?
* Avoiding making copies of files on external memory devices.
* Avoiding using personal data to create a password.
* Assigning administration privileges only to people with technical knowledge.
* **Training users about correct security behaviors.**

	Training users about correct security behaviors.
	-
	Social engineering attacks are based on manipulating people. The usual goal of these attacks is to trick a user into launching malware or sharing certain information. The most important aspect of mitigating social engineering attacks is to make users aware of the existence of such attacks and advise them regarding appropriate behavior in case of anomalous requests.
--------
%Error opening tftp://255.255.255.255/network-confg (Timed out)
%Error opening tftp://255.255.255.255/cisconet.cfg (Timed out)

What can you conclude based on the messages?

* The router will attempt to load the configuration from the NVRAM.
* The router configuration will be loaded from the TFTP server.
* The TFTP server URL is incorrect.
* **The configuration file is not found on the TFTP server.**

	The configuration file is not found on the TFTP server.
	-
	By default, the router first attempts to load the startup configuration from the NVRAM. If the startup configuration file does not exist in NVRAM, the router searches for a TFTP server. If the router detects that it has an active link, it sends a broadcast searching for a configuration file across the active link. No specific TFTP URL is used. If the router does not find the configuration source, it will display the error console messages.
--------
After the Cisco IOS Software image is loaded and started, from which three components can the device load its configuration? (Choose three.)
* DHCP server
* DNS server
* RAM
* **NVRAM**
* **SCP server**
* **TFTP server**

	* NVRAM
	* SCP server
	* TFTP server
	-
	If there is an existing saved configuration file (startup-config) in NVRAM, it is executed. If the startup configuration file does not exist in NVRAM, the router may search for a network file server (TFTP, SCP, and so on). RAM stores the current configuration after it is loaded. A DHCP server can provide the URL of the configuration file, where the file can then be loaded from. DNS servers are not used for file transfers.
--------
On R1, at the command prompt, issue the exit command as many times as necessary until you get the "Press RETURN to get started" prompt. Which password do you have to type to access the USER exec mode?
* Cisco123!
* Cisco333!
* CiscoR1!
* **password is not required**

--------
Which number represents the default encryption type of the protected password used to restrict access to the privileged EXEC mode?
* **4**
* 5
* 8
* 9

	**4 Ans**
--------
Examine the Device Access table in the Job Aid. There are four users configured on SW2. The SW2 switch console line access is set to privilege level 5. Presuming command privileges are set to default, which username should you use to be able to change the SW2 configuration?
* admin
* monitor
* operator
* **superadmin**

	superadmin
	-
	By default, Cisco IOS configuration commands require the maximum privilege level, which is 15. This is the privilege level of the user superadmin.
--------
From PC1, connect to SW2 using Telnet and verify the console line configuration. How long can a user be inactive while still connected to the console of SW2?
* **60 minutes and 7 seconds**
* 60 minutes within 7 days
* 67 minutes
* 67 seconds

	60 minutes and 7 seconds
--------
From PC2, connect to SW2 using Telnet. Examine the running configuration. Which time zone is set?
* CET
* **LJUB**
* MDT
* PST

	LJUB
	-
	When you issue the show running-config command, the outup displays the clock timezone LJUB 8 0. You can obtain the same information using the show clock command.
--------
What are two field names corresponding to the IPv4 header field and the IPv6 header field that contain Differentiated Services Code Point (DSCP) markings? (Choose two.)
* flow control
* flow label
* IP precedence
* offset
* **traffic class**
* **type of service (ToS)**

	* traffic class
	* type of service (ToS)
	-
	In the original RFC definitions of the ToS field, IP precedence was a 3-bit sub-field. The initial definition of the ToS field has been changed to include the flow control field. The offset field is the IPv4 header field used when packets are fragmented. The flow label IPv6 header field can be used to label a set of packets belonging to the same flow and does not contain DSCP markings.
--------
When a network handles Voice over IP (VoIP) packets differently than HTTP packets, which network feature is implemented?
* fault tolerance
* **quality of service**
* scalability
* security

	quality of service
	-
	Quality of service (QoS) includes tools, mechanisms, and architectures that allow you to control how and when network resources are used by applications. QoS is especially important for prioritizing traffic when the network is congested. Scalability ensures that a network can easily accommodate more users and data transmission requirements, while security indicates how well the network is defended from potential threats. Fault tolerance indicates how resilient the network is in case of failure.
--------
Which statement regarding a small office/home office (SOHO) of a remote worker is correct?
* **It is a LAN that includes both wireless and wired network devices.**
* It must be permanently connected to the main office.
* It must follow the three-tier architecture model.
* It typically uses dark fiber to connect to the main office.

	It is a LAN that includes both wireless and wired network devices.
	-
	The SOHO connectivity to other enterprise network segments can be established when required. To connect to other segments, SOHO networks usually use public internet, which they access via broadband connection. Since SOHO networks are typically small and consist of only a small number of devices, such as a computer and a printer, they do not need to follow the three-tier architecture model to ensure network operation.
--------
What is the role of a router?
* to connect departmental devices
* **to connect network segments**
* to provide wireless network access
* to secure the edge network

	**to connect network segments**
--------
What is the administrative distance of OSPF?
* 90
* **110**
* 170
* 200

	110
	-
	Internal EIGRP routes have the administrative distance value of 90, external EIGRP routes have 170 and internal BGP routes have an administrative distance of 200.
--------
What are two characteristics of a pre-shared key wireless implementation? (Choose two.)
* Access control is centralized.
* An authentication server is required.
* **Encryption uses an optional Advanced Encryption Standard (AES).**
* **Encryption uses the Temporal Key Integrity Protocol (TKIP).**
* The authentication key is rotated automatically.

	* Encryption uses an optional Advanced Encryption Standard (AES).
	* Encryption uses the Temporal Key Integrity Protocol (TKIP).
	-
	TKIP uses a suite of algorithms surrounding Wired Equivalent Privacy (WEP) and Wi-Fi Protected Access (WPA) to enhance its security. AES allows for longer keys and is used for most WLAN security solutions. TKIP and AES are both used in the Personal mode of wireless protected access.
--------
A company needs to implement a secure VPN solution using IPsec. Which protocol and encryption algorithm should be used to guarantee VPN confidentiality?
* AH protocol with the AES encryption algorithm
* AH protocol with the SHA-2 encryption algorithm
* both ESP and AH protocols with the RSA encryption algorithm
* **ESP protocol with the 3DES encryption algorithm**
* ESP protocol with the Diffie-Hellman Group 7 encryption algorithm

	ESP protocol with the 3DES encryption algorithm
	-
	Of the two IPsec tunnel protocols, only the Encapsulating Security Payload (ESP) supports confidentiality. 3DES and AES are symmetric encryption algorithms, and both can be used in IPsec VPNs. SHA-2 is a hash function, RSA is a public-key cryptosystem, and Diffie-Hellman is a key exchange algorithm.
--------
Perform the following tasks:
Examine the current NTP and time zone configuration on the devices.
Configure R1 as the NTP master with stratum = 1.
Configure R2 and SW to synchronize time directly with R1.

After configuring R2 and SW to synchronize their clocks directly to R1, what are the stratum levels of R2 and SW?
* The R2 stratum level is 1 and the SW stratum level is 1.
* **The R2 stratum level is 2 and the SW stratum level is 2.**
* The R2 stratum level is 2 and the SW stratum level is 3.
* The R2 stratum level is 3 and the SW stratum level is 3.

	The R2 stratum level is 2 and the SW stratum level is 2.

What is the maximum stratum level that you can configure on a Cisco device?
	**15 Ans **

On the SW switch, display the established NTP associations. What is the value displayed in the address column?
* *~198.51.100.2
* *198.51.100.2
* ~198.51.100.2
* 198.51.100.2

	*~198.51.100.2
	-
	An asterisk (*) next to a configured peer represents that the device is synced to this peer and using it as the master clock. A tilde (~) next to a configured peer represents that this is a configured master server.
--------
Which three characteristics differentiate Ansible from other automation tools? (Choose three.)
* It is agent-based.
* **It is agentless.**
* **It is written in Python.**
* It is written in Ruby.
* **It uses YAML definitions.**

	* It is agentless.
	* It is written in Python.
	* It uses YAML definitions.
	-
	Ansible is an agentless automation tool, so it does not require any application to be installed in the target system. Ansible is written in Python and uses YAML files to define the configuration, as well as the automation steps.
--------
Which three statements are correct about the JSON data format? (Choose three.)
* Empty values cannot be used in the JSON data format.
* JSON arrays separate elements using a semicolon.
* **JSON can be used when data is sent from a server to a web page.**
* **JSON does not support comments.**
* **JSON is a hierarchical data format.**

	* JSON can be used when data is sent from a server to a web page.
	* JSON does not support comments.
	* JSON is a hierarchical data format.
	-
	Arrays use a curly bracket notation with comma-separated elements (example: {"firstName":"John", "lastName":"Doe"}, {"firstName":"Anna", "lastName":"Smith"}). Empty values can be used in the JSON data format by using the word "null."
	Previous
--------
Which two statements about the Dynamic Multipoint Virtual Private Network (DMVPN) are true? (Choose two.)
* **DMVPN creates hub-to-spoke tunnels.**
* **DMVPN creates spoke-to-spoke tunnels.**
* DMVPN is used for connection between an enterprise and a provider.
* DMVPN is used for connection between enterprises.
* DMVPN is used within a branch network.

	* DMVPN creates hub-to-spoke tunnels.
	* DMVPN creates spoke-to-spoke tunnels.
	-
	After building the hub-and-spoke VPNs, the spokes can establish direct spoke-to-spoke tunnels, based on the information they obtain from the hub.
--------
In which situation would you choose to use UDP instead of TCP for IP applications?
* when ensuring accurate file transfers even in the face of network issues
* when ensuring packet headers are not changed during transmission from source to destination
* **when speed of delivery is more important than error correction in IP packet transmissions**
* when you require that the recipient of the packets verify that the packets are delivered

	when speed of delivery is more important than error correction in IP packet transmissions
	-
	Both UDP and TCP can provide integrity verification via checksum calculation. However, the usage of the checksum field is mandatory only in the TCP. TCP, unlike UDP, provides features that guarantee the delivery of the packets, by using sequence numbering, acknowledgments, and retransmissions.
--------
Which flag is set in the first TCP packet sent by a device initiating a communication?
* ACK
* FIN
* PSH
* RST
* **SYN**

	SYN
	-
	The correct answer is SYN. ACK is the acknowledgment flag, used to confirm the reception of the sent bytes. The FIN flag identifies the last packet received from the sender. The RST flag is used to reset the connection, and the PSH flag is used when buffered data must be sent to the receiving application without waiting.
--------
A device has been assigned an IPv6 address through the Stateless Address Autoconfiguration (SLAAC) process. Which three statements about SLAAC are correct? (Choose three.)
* **It generates link-local addresses.**
* **It generates global unicast IPv6 addresses.**
* It must be used in combination with a DHCPv6 server.
* **It relies on ICMPv6 router advertisements.**
* It requires a device to use the EUI-64 format in the process.
* It relies on a DHCPv6 server for duplicate address detection (DAD).

	* It generates link-local addresses.
	* It generates global unicast IPv6 addresses.
	* It relies on ICMPv6 router advertisements.
	-
	SLAAC is an autoconfiguration mechanism that automatically configures the IPv6 address of a device. The device picks its own address based on the network prefix being advertised by the router on their connected interface. As defined in RFC 4862, the autoconfiguration process includes generating a link-local address, generating global addresses through SLAAC, and the duplicate address detection procedure to verify the uniqueness of the addresses on a link. Some devices may choose to use EUI-64 or a randomized value for the interface ID.
--------
An enterprise wants to provide a global service that would be provided from an enterprise resource nearest to the user. For which three reasons does the enterprise choose to assign anycast IPv6 addresses to the relevant devices? (Choose three.)
* Because all the devices configured with the IPv6 anycast address would be aware of the user session.
* **Because IPv6 anycast addresses are globally routable.**
* Because routing of IPv6 anycast addresses is more secure than routing other IPv6 address types.
* **Because routing tables will point to the nearest resource configured with the IPv6 anycast address.**
* **Because using IPv6 anycast addresses provides automatic failover.**

	* Because IPv6 anycast addresses are globally routable.
	* Because routing tables will point to the nearest resource configured with the IPv6 anycast address.
	* Because using IPv6 anycast addresses provides automatic failover.
	-
	The nearest resource provides a service to the user; other resources, which are equally capable of providing the service, are not involved. Routing information exchange is no more or less secure for anycast IPv6 addresses than it is for other IPv6 address types.
--------
Which two commands display the type of trunking encapsulation of an interface? (Choose two.)
* **show interfaces Ethernet0/0 switchport**
* show interfaces status
* show interfaces summary
* **show interfaces trunk**
* show ip interfaces brief

	* show interfaces Ethernet0/0 switchport
	* show interfaces trunk
	-
	The show interfaces status, show ip interfaces brief, and show interfaces summary commands do not display the type of trunking encapsulation of an interface.
--------
On a Cisco switch, which two commands display the VLANs allowed on trunk interfaces? (Choose two.)
* show interfaces
* show interfaces stats
* show interfaces summary
* **show interfaces switchport**
* **show interfaces trunk**

	* show interfaces switchport
	* show interfaces trunk
	-
	The show interfaces summary command displays a summary of statistics for all interfaces that are configured on a switch. The show interfaces stats command displays the input and output packets by switching the path for the interface.
--------
Which component is used to generate a signal for single-mode fiber connections?
* cathode
* **laser transmitter**
* LED diode
* oscillator

	**laser transmitter**
--------
What is the purpose of a Layer 3 switch?
* **to route traffic between company VLANs**
* to route traffic between the company network and the internet
* to route traffic between multiple geographical locations
* to route traffic between different protocol networks

	to route traffic between company VLANs
	-
	Routers route traffic between the company network and the internet, as well as between different geographical networks. Multiprotocol routers provide routing between different networks with different protocols.
--------
Which wired network device is an equivalent of a wireless access point (AP)?
* firewall
* hub
* router
* **switch**

	switch
	-
	A wireless AP also provides connectivity to end devices over multiple VLANs. Firewalls secure network traffic, routers connect multiple network segments, and hubs are not VLAN-aware.
--------
Which 802.11 frame is a control frame?
* association request
* association response
* **acknowledgment**
* beacon

	acknowledgment
	-
	Association request, response, and beacon frames are 802.11 management frames.
--------
Which two of the following protocols does the distribution layer use to provide default gateway redundancy? (Choose two.)
* Device Control Protocol (DCP)
* Distributed Network Protocol (DNP3)
* Dynamic Source Routing Protocol (DSR)
* **First Hop Redundancy Protocol (FHRP)**
* **Hot Standby Router Protocol (HSRP)**

	* First Hop Redundancy Protocol (FHRP)
	* Hot Standby Router Protocol (HSRP)
	-
	FHRP and HSRP are designated to allow two or more routers to take the role of the default gateway in the network. DCP is designed for integration, monitoring and controlling of devices in the network. DSR is a routing protocol for wireless mesh networks. DNP3 is a set of open source protocols, developed for communication mainly in equipment used by utilities such as electric and water companies.
--------
What are two examples of full hypervisors? (Choose two.)
* Docker
* DOSBox
* Kubernetes
* **type-1**
* **type-2**

	* type-1
	* type-2
	-
	The type-1 hypervisor is also called the bare metal hypervisor, and is installed directly on hardware. The type-2 hypervisor is installed inside an OS, such as Linux or Windows. Docker and Kubernetes are container software packages that don't include any virtualization. DOSBox is an emulator program which emulates an IBM PC running the DOS operational system.
--------
Which command is used to verify a default gateway configuration on a Layer 2 switch?
* show interface description
* show interface stats
* show ip default-gateway network
* show management
* **show running-config**

	show running-config
	-
	The show interface stats command displays interface statistics. The show management command displays the management applications.
--------
Which command is used to set 192.168.1.1 as the default gateway on a Layer 2 switch?
* **Switch(config)# ip default-gateway 192.168.1.1**
* Switch(config)# ip default-network 192.168.1.1
* Switch(config)# ip route 0.0.0.0 0.0.0.0 192.168.1.1
* Switch(config)# ip route 0.0.0.0 0.0.0.0 DHCP 1

	Switch(config)# ip default-gateway 192.168.1.1
	-
	This command sets a default gateway for devices that do not support IP routing. The ip default-network command sets a classful default route. The ip route 0.0.0.0 0.0.0.0 192.168.1.1 command sets the default route via the forwarding router IP address. The DHCP keyword instructs the switch to get the forwarding router IP address from the DHCP.
--------
From the assigned address space, allocate the second available VLSM segment to segment B so that it can accommodate five end devices. Note that the first available segment was already used for segment A (172.16.31.0/29).
On R2, configure the Ethernet0/1 interface with the last available IPv4 address in the chosen segment.
On PC1, configure the Ethernet0/0 interface with the first available IPv4 address in the chosen segment.
On PC1, configure the default gateway.
Continue with VLSM subnetting and allocate the next available VLSM segment to segment C. Choose the subnet size so that it exactly meets addressing requirements as represented by the topology.
On R1, configure Ethernet0/2 interface with the first available IPv4 address from the chosen VLSM segment.
On R4, configure Ethernet0/0 interface on R4 with the last available IPv4 address from the chosen VLSM segment.

On PC1, which address did you configure as the default gateway?
* 172.16.31.7
* 172.16.31.8
* **172.16.31.14**
* 172.16.31.15

	172.16.31.14
	-
	172.16.31.7 is the broadcast address of the segment A network. 172.16.31.8 is the IPv4 address of the segment B network and 172.16.31.15 is the broadcast address of that network.

What is the broadcast address of segment B?
* 172.16.31.7
* 172.16.31.8
* **172.16.31.15**
* 172.16.31.16

	172.16.31.15
	-
	172.16.31.7 is the broadcast address of the segment A network, 172.16.31.8 is the IPv4 address of the segment B network, and 172.16.31.16 is the IPv4 address of the segment C network.

How many end devices can be addressed in segment D?
* 6
* 14
* **30**
* 62

	30
	-
	Segment D has a network prefix of /27, which means that there are 32 possible addresses to be assigned, one of which is reserved for the network address and one for the broadcast address. That leaves 30 IPv4 addresses that can be assigned to end devices.

On R4, issue the ping command sourced from the address allocated to the interface E0/0 and test connectivity to the internet test address. What is the resulting output?
* Ping is not successful because an ACL is blocking traffic.
* Ping is not successful because IP routing is not enabled on R4.
* Ping is partially successful (30%).
* **Ping is successful (80-100%).**

	Ping is successful (80-100%).
	-
	If everything was correctly configured in the lab, then the ping to the internet test address should be successful.
--------
Which Windows Command Prompt command do you use to view the IP address of a host?
* ip address
* ifconfig
* **ipconfig**
* show ip address

	ipconfig
	-
	The Windows Command Prompt tool uses the ipconfig command to display network interface settings. The ifconfig and ip address commands are used in Linux systems. Show commands are used on Cisco IOS devices.
--------
Which three IPv4 addresses are private? (Choose three.)
* **10.255.255.254**
* **172.31.255.254**
* 172.32.255.254
* **192.168.1.100**
* 192.169.1.100

	* 10.255.255.254
	* 172.31.255.254
	* 192.168.1.100
	-
	These ranges of IP addresses are private: 10.0.0.0 to 10.255.255.255, 172.16.0.0 to 172.31.255.255, and 192.168.0.0 to 192.168.255.255. Addresses in these ranges are not routed on the internet backbone.
--------
When creating and maintaining the MAC address table, which two activities does a switch perform? (Choose two.)
* It adds the destination MAC address in the frame and the incoming port number.
* It adds the destination MAC address in the frame and the outgoing port number.
* **It adds the source MAC address in the frame and the incoming port number.**
* It resets the aging timer of all the entries related to the incoming port.
* **It resets the aging time of the MAC table entry for the source MAC address.**

	* It adds the source MAC address in the frame and the incoming port number.
	* It resets the aging time of the MAC table entry for the source MAC address.
	-
	A switch uses the destination MAC address to decide whether to forward or flood a frame. The destination MAC address is not stored in the MAC address table. The aging timer is reset for the source MAC address entry each time the switch receives a frame from that source MAC address.
--------
Which command would you use to configure a floating static route?
* ip route static 192.168.13.0 255.255.255.0 100
* **ip route 192.168.13.0 255.255.255.0 172.17.10.1 100**
* ip route 192.168.13.0 255.255.255.0 172.17.10.1
* ip route 192.168.13.0 255.255.255.0 172.17.10.1 metric 100

	ip route 192.168.13.0 255.255.255.0 172.17.10.1 100
--------
Refer to the exhibit. Which of the routes is a floating static route?

BR2# show ip route
<... output omitted ...>

Gateway of last resort is 172.16.2.1 to network 0.0.0.0

D*EX  0.0.0.0/0 [170/307200] via 172.16.2.1, 00:03:01, Ethernet0/0
      10.0.0.0/8 is variably subnetted, 8 subnets, 4 masks
D        10.8.0.0/13 [90/435200] via 172.16.2.1, 00:02:58, Ethernet0/0
D        10.64.0.0/14 is a summary, 00:03:04, Null0
C        10.64.0.0/16 is directly connected, Loopback0
L        10.64.0.1/32 is directly connected, Loopback0
      172.16.0.0/16 is variably subnetted, 3 subnets, 2 masks
D        172.16.1.0/30 [90/307200] via 172.16.2.1, 00:03:01, Ethernet0/0
C        172.16.2.0/30 is directly connected, Ethernet0/0
L        172.16.2.2/32 is directly connected, Ethernet0/0
S     192.168.16.0/24 [90/0] via 172.16.2.1
S     192.168.33.0/24 [1/0] via 172.16.2.1
      209.165.200.0/27 is subnetted, 1 subnets
D        209.165.200.224 [90/307200] via 172.16.2.1, 00:03:01, Ethernet0/0


* route to network 10.8.0.0/13
* route to network 172.16.1.0/30
* **route to network 192.168 16.0/24**
* route to network 192.168.33.0/24

	route to network 192.168 16.0/24
	-
	A floating static route is a static route with an administrative distance greater than the default value of 1. In the example we have two static routes, the route to network 192.16.33.0/24 has the default administrative distance, and is therefore not floating static. The other two options are routes sourced from elsewhere, in this case from the EIGRP routing protocol, as indicated by the "D" protocol code.
--------
When a router is calculating the network portion of an IPv4 address, which bitwise operation is performed on the IPv4 address and the subnet mask?
* **AND**
* NAND
* OR
* XOR

	AND
	-
	In order to extract the network part of an IPv4 address, the ANDing logical operation is performed with the IPv4 address and the subnet mask as operands. When the binary digit 1 is ANDed with another digit, the value of the other digit is preserved. ANDing with 0 always results in a 0. Therefore, 1s in the subnet mask will preserve the value found in the IPv4 address. The logical operations NAND, OR, and XOR would not preserve the values found in the IPv4 address.
--------
Two computers are connected to a Cisco Catalyst Layer 2 switch. PC1 is assigned the address 10.250.20.20/26 and PC2 is assigned the address 10.250.20.50/26. When a user on PC1 issues the ping 10.250.20.63 command, will PC2 respond to it?
* No, because 10.250.20.63 is not in the subnet that PC1 belongs to.
* No, because 10.250.20.63 is not the IP of PC2.
* **Yes, the PC2 will respond to the 10.250.20.63 broadcast if both ports are operationally in access mode and the same VLAN.**
* Yes, if the ip routing command is configured on the switch.

	Yes, the PC2 will respond to the 10.250.20.63 broadcast if both ports are operationally in access mode and the same VLAN.
	-
	The IPv4 address 10.250.20.63 is the broadcast address of the 10.250.20.0/26 subnet. A switch forward broadcast communication to all ports in a VLAN. If both ports that connect PC1 and PC2 belong to the same VLAN, then PC2 as well as other devices in the same subnet will receive the ICMP request from PC1 and respond to it.
--------
Which statement regarding online and offline password attacks is true?
* **Offline attacks are more dangerous because there is no external authentication system.**
* Offline attacks are more dangerous because they target out-of-band management assets.
* Online attacks are more dangerous because distributed sources can deliver them.
* Online attacks are more dangerous because they can target resources connected on the network.

	Offline attacks are more dangerous because there is no external authentication system.
	-
	In an online attack, the password has the protection of the system in which it is stored, but there is no such protection in offline attacks. In an offline attack, the attacker captures the password hash or the encrypted form of the password. The attacker can then make countless attempts to crack the password without being noticed.
--------
Lab Work 7 begins:
------------------

During this activity, you will use the Cisco Discovery Protocol (CDP) and the Link Layer Discovery Protocol (LLDP) to map the connectivity within an unfamiliar network. There are four devices in the topology. You have access to the console ports of SW1, SW2, and R1. However, you do not know how they are connected. Using the CDP and LLDP commands, you will determine the actual topology.

Note
The routers in the topology may take 2 to 3 minutes to boot up and become accessible.

IPv4 addressing is configured on all devices.

The SW2 neighbor discovery protocol is pre-configured. Do not change the existing configuration parameters on SW2.

CDP is already configured on R2. You will not have direct access to the R2 router. You can gain information about R2 configuration using neighbor discovery protocols on neighboring devices.

In this task you will discover the topology using Link Layer Discovery Protocol (LLDP) and the Cisco Discovery Protocol (CDP). Router R2 is already pre-configured. Perform the following tasks:

Examine the configurations of the SW1 and SW2 switches. Answer the first question.

Configure switch SW1 and router R1 so that Layer 2 connectivity information is provided among all devices in the topology, that is: SW1, SW2, R1, and R2.
Examine the configurations of the switches SW1 and SW2. SW2 cannot obtain Layer 2 information from SW1 using CDP. Why?
* because CDP is disabled on the interface connecting to SW1
* **because CDP is globally disabled on SW2**
* because the interface connecting to SW1 is down
* because the interface connecting to SW1 is in the wrong VLAN
* because STP is blocking the interface connecting to SW1

	because CDP is globally disabled on SW2
	-
	The Cisco Discovery Protocol works as long it is globally enabled and not disabled on specific interfaces connecting two devices, and the two devices have L1 and L2 connectivity.

What is the IP address of the R2 interface connecting to R1?
* 10.10.1.3
* 192.168.3.1
* **192.168.3.2**
* 192.168.3.3

	192.168.3.2
	-
	By issuing the show cdp neighbors detail command on R1, you are able to get the IPv4 address of R2's interface connecting to R1.

What are the ports that interconnect switches SW1 and SW2?
* **SW1 Ethernet0/0 and SW2 Ethernet0/0**
* SW1 Ethernet0/0 and SW2 Ethernet0/1
* SW1 Ethernet0/1 and SW2 Ethernet0/0
* SW1 Ethernet0/1 and SW2 Ethernet0/1

	SW1 Ethernet0/0 and SW2 Ethernet0/0
	-
	Answer
	The correct answer is SW1 Ethernet0/0 and SW2 Ethernet0/0. By issuing the show lldp neighbors command, you can learn that SW1 and SW2 are connected by using Ethernet0/0 ports on both.

In the topology you discovered in this exercise, can R1 obtain information about SW1 using CDP?
* **No, because R1 and SW1 are not directly connected.**
* No, because STP is blocking the connection between R1 and SW1.
* Yes, because R1 and SW1 are directly connected.
* Yes, because R1 and SW1 both have CDP enabled.

	No, because R1 and SW1 are not directly connected.
	-
	By examining the topology using CDP, you can determine that SW1 and R1 are not directly connected. SW2 is used to interconnect the two devices and CDP information is not propagated over devices.

Lab Work 7 ends:
----------------
--------
Which two Microsoft Windows commands will display the DNS server address configured on the host? (Choose two.)
* ipconfig
* **ipconfig /all**
* net config
* netstat -f
* **nslookup**

	* ipconfig /all
	* nslookup
	-
	The letters "ns" are usually used to indicate the name server service in the network. The nslookup command is used for querying the configured DNS server to obtain domain name, IP address mapping, or other DNS records. The ipconfig command provides only basic information that does not include DNS server addresses. The net config command can be used to verify configuration or configure server and workstation services. The netstat -f command displays network statistics.
--------
When using Hot Standby Router Protocol (HSRP) for gateway redundancy, which address is used for the gateway on hosts?
* active
* active and standby
* standby
* **virtual**

	virtual
	-
	HSRP provides gateway redundancy by sharing IP and MAC addresses between redundant gateways. The protocol consists of virtual IP and MAC addresses that the routers belonging to the same HSRP group share between each other.
--------
Which Cisco command can you use to reset the OSPF neighbor adjacencies and DR/BDR election results?
* **clear ip ospf process**
* clear ip route
* ip ospf process default
* ip ospf shutdown

	clear ip ospf process
	-
	The ip ospf process default command is invalid. The ip ospf shutdown command is used in interface configuration mode to initiate a graceful shutdown of the OSPF protocol at the interface level. The clear ip route command deletes routes from the IPv4 routing table.
--------
Which two attack categories does the smurf attack belong to? (Choose two.)
* **amplification**
* brute-force
* man-in-the-middle
* exfiltration
* **reflection**

	* amplification
	* reflection
	-
	A smurf attack can be classified as a reflection attack because it is launched from a single source spoofing one or multiple IP addresses, triggering replies to the spoofed sources. By sending a small amount of request traffic, an attacker can cause much larger response traffic, making it an amplification attack.
--------
You have restarted a router, which has the default booting procedure. During the reboot, the following messages appear on the console:
%Error opening tftp://255.255.255.255/network-confg (Timed out) %Error opening tftp://255.255.255.255/cisconet.cfg (Timed out)
What can you conclude based on the messages?
* The router will attempt to load the configuration from the NVRAM.
* The router configuration will be loaded from the TFTP server.
* The TFTP server URL is incorrect.
* **The configuration file is not found on the TFTP server.**

	The configuration file is not found on the TFTP server.
	-
	By default, the router first attempts to load the startup configuration from the NVRAM. If the startup configuration file does not exist in NVRAM, the router searches for a TFTP server. If the router detects that it has an active link, it sends a broadcast searching for a configuration file across the active link. No specific TFTP URL is used. If the router does not find the configuration source, it will display the error console messages.
--------

Restrict access to the privileged EXEC mode. Configure the protected password CiscoR1! using the default encryption type.
Configure the unprotected password Cisco123! and ensure it is obfuscated in the configuration file.
Protect the access to the console by requiring a password to access the console. Set the console password to Cisco333!.

From PC1, connect to SW1 using Telnet with the password Cisco111!. Which password did you use to access the privileged EXEC mode on SW1?
* Cisco111!
* Cisco123!
* CiscoAdm1!
* **CiscoSW1!**
* CiscoTech1!

	CiscoSW1!
	-
	When remotely accessing a device, the default console access restrictions require that privileged EXEC mode access is protected. A configured enable secret always takes precedence over a configured enable password.

On R1, at the command prompt, issue the exit command as many times as necessary until you get the "Press RETURN to get started" prompt. Which password do you have to type to access the * USER exec mode?
* Cisco123!
* **Cisco333!**
* CiscoR1!
* password is not required

	Cisco333!

Which number represents the default encryption type of the protected password used to restrict access to the privileged EXEC mode?
* **4**
* 5
* 8
* 9

	4
	-
	The enable secret is always stored in a protected fashion in the configuration file. Cisco IOS Software on routers supports several encryption types. On production routers, you will most likely find encryption type 8 or type 9. Using the default encryption type 4, which represents the Secure Hashing Algorithm 2 (SHA-2) protection, is not recommended due to security risks. Use the show running-config command to reveal the encryption type used for enable secret.

Examine the Device Access table in the Job Aid. There are four users configured on SW2. The SW2 switch console line access is set to privilege level 5. Presuming command privileges are set to default, which username should you use to be able to change the SW2 configuration?
* admin
* monitor
* operator
* **superadmin**

	superadmin
	-
	By default, Cisco IOS configuration commands require the maximum privilege level, which is 15. This is the privilege level of the user superadmin.

From PC1, connect to SW2 using Telnet and verify the console line configuration. How long can a user be inactive while still connected to the console of SW2?
* **60 minutes and 7 seconds**
* 60 minutes within 7 days
* 67 minutes
* 67 seconds

	60 minutes and 7 seconds
	-
	The exec-timeout command specifies the minutes and seconds that define the timeout, after which an inactive user is automatically disconnected from the console. This prevents users from remaining connected to a console port when they leave a station. Using the exec-timeout 0 0 command disables the timeout; this should not be used in a production environment because it is not a secure practice.

From PC2, connect to SW2 using Telnet. Examine the running configuration. Which time zone is set?
* CET
* **LJUB**
* MDT
* PST

	**LJUB**
----------------
What does the term per-hop behavior (PHB) signify?
* a set of node requirements for compliance with the DiffServ model
* a set of packet markings applied to different classes of traffic
* **a set of techniques for traffic shaping**
* a set of traffic classes defined in the network

	a set of techniques for traffic shaping
	-
	The term PHB refers to how a node will treat traffic having the same Differentiated Services Code Point (DSCP) values. The DiffServ model itself does not specify how PHBs must be implemented. A variety of techniques may be used to implement the desired traffic conditioning and PHB.
--------
Which three of the following application characteristic values are determined in the service level specification phase when designing the quality of service (QoS) policy of a network? (Choose three.)
* generated data flows
* **required bandwidth**
* required responsiveness
* response criticality
* **tolerable jitter**
* **tolerable packet loss**

	* required bandwidth
	* tolerable jitter
	* tolerable packet loss
	-
	When you specify the service levels for a class of traffic, you define specific values for delay and jitter, packet loss tolerance, required bandwidth, and time sensitivity. After the implementation of the QoS policy, the performance of your network can then be measured and evaluated against the specified service levels. You should identify the data flows generated by the application prior to determining service levels, in the first phase of policy design. Required responsiveness and response criticality are performed within the business audit phase, which precedes service-level specification.
--------
From a network perspective, how is a server a different endpoint than a user workstation?
* A server requires lower latency.
* **A server requires more bandwidth.**
* A server requires Power over Ethernet (PoE) connectivity.
* A server requires stricter network access control.

	A server requires more bandwidth.
	-
	Since a server is a convergent point on the network that connects multiple devices, it consumes more bandwidth. Low latency is not a differentiator for a server, since it is also a requirement for IP phones, for instance. Servers cannot be powered through PoE, since their power requirements surpass PoE capabilities. Servers are deployed in secured environments (locked closets or server rooms), where network access control is not a focus, since other security measures are implemented.
--------
Which network topology layer does a wireless access point (WAP) belong to?
* **access**
* collapsed core
* core
* distribution

	access
	-
	Access points connect client devices such as laptops and cameras, which makes them a part of the access layer. The core, collapsed core, and distribution layers are not intended for connection of network devices of this type.
--------
On a router that does not have a default route in the routing table, you issue the following two commands:
Router(config)# ip route 0.0.0.0 0.0.0.0 10.10.10.10 20
Router(config)# ip route 0.0.0.0 0.0.0.0 10.20.250.2 10
* What is the result of executing the commands?
* Both routes are installed in the routing table as default routes.
* The route pointing to the IPv4 address 10.10.10.10 is installed as the default route.
* **The route pointing to the IPv4 address 10.20.250.2 is installed as the default route.**
* There are no changes to the routing table.

	The route pointing to the IPv4 address 10.20.250.2 is installed as the default route.
--------
Which three security services does the Counter Mode with Cipher Block Chaining Message Authentication Code Protocol (CCMP) provide? (Choose three.)
* **access control**
* **authentication**
* authorization
* **data confidentiality**
* data redundancy

	* access control
	* authentication
	* data confidentiality
	-
	CCMP is the standard encryption protocol for use with Wi-Fi Protected Access 2 (WPA2). CCMP does not provide authorization and data redundancy.
--------
What are two reasons for choosing Transport Layer Security (TLS) over IP Security (IPsec) encryption? (Choose two.)
* IPsec encrypts the IP packet, resulting in lesser application-level security.
* IPsec is less efficient than TLS, and in general not supported on mobile devices.
* **IPsec requires dedicated software installed on client hosts.**
* **TLS can be used for encrypting traffic to public websites.**
* TLS decryption can be easily accelerated in hardware.

	* IPsec requires dedicated software installed on client hosts
	* TLS can be used for encrypting traffic to public websites
	-
	IPsec can encrypt the entire IP packet, while TLS encrypts only the application level data, which makes IPsec a more flexible choice for a broader range of applications. However, IPsec requires a software client installed, as well as a specific configuration on the VPN server, which makes it a worse choice than TLS to encrypt traffic to resources external to the organization. TLS needs only the browser.

Need to continue - break point
--------
Lab Work 8 begins:
------------------
Configure router R1 so that the PC1 and PC2 hosts get DHCP information from router R2.
Ensure that both PC1 and PC2 hosts get their addresses via DHCP.

What is the default gateway that PC1 has received through DHCP?
* 10.10.1.1
* **10.10.1.53**
* 10.10.1.100
* 10.10.1.254

	10.10.1.53
	-
	In real networks, the gateway address is usually either the first or the last assignable IP address of the subnet.

What is the lease time for the assigned IP address on PC2?
* 1 second
* **1 minute**
* 1 hour
* 1 day

	1 minute
	-
	or 60 seconds.

What is the IPv4 address of the DNS server assigned by DHCP to PC1?
* 10.10.1.1
* 198.51.100.1
* 203.0.113.1
* **203.0.113.30**

	203.0.113.30
	-
	The DNS server resides on SRV2, which has an IP address of 203.0.113.30.

Lab Work 8 ends:
----------------
--------
Which APIs are used for communication between a software-defined networking (SDN) application and a controller?
* Eastbound APIs
* **Northbound APIs**
* Southbound APIs
* Westbound APIs

	Northbound APIs
	-
	Northbound APIs or northbound interfaces are responsible for the communication between the SDN controller and the services that run over the network. Northbound APIs enable your applications to manage and control the network. Therefore, rather than adjusting and tweaking your network repeatedly to get a service or application running correctly, you can set up a framework that allows the application to demand the network setup that it needs.
--------
What is the latest and one of the most popular network configuration protocols?
* BGP
* LDP
* **NETCONF**
* SNMP

	**NETCONF**
--------
Refer to the exhibit. The service provider is implementing Multiprotocol Label Switching Virtual Private Network (MPLS VPN) service.

Which two options indicate the specific VPN type that is implemented and how the service provider appears from the perspective of the customer? (Choose two.)
* The service provider is implementing MPLS L2VPN.
* **The service provider is implementing MPLS L3VPN.**
* The service provider is implementing MPLS VPLS.
* **The service provider network can be represented as a router from the customer perspective.**
* The service provider network can be represented as a switch from the customer perspective.

	The service provider is implementing MPLS L3VPN.
	The service provider network can be represented as a router from the customer perspective.
--------
Which four of the following are valid link-local IPv6 addresses? (Choose four.)
* **fe80::1**
* ff80::1
* **fe90::1**
* **feb1::1**
* **fea3::1**
* fec3::1

	* fe80::1
	* fe90::1
	* feb1::1
	* fea3::1
	-
	All addresses encompassed by the fe80::/10 prefix are considered valid link-local IPv6 addresses. The ff00::/8 prefix is the prefix of multicast IPv6 addresses. Addresses starting with the hexadecimal digits fec3 do not belong to a link-local IPv6 address range.
--------
Refer to the exhibit. Switches SW1 and SW2 are directly connected, with ports configured in access mode and assigned to VLAN 1. They cannot communicate with each other. What are two possible reasons causing the issue? (Choose two.)
* Both devices have Dynamic Trunking Protocol (DTP) disabled, so they cannot negotiate the switchport mode.
* **One of the connecting switch ports is administratively shut down.**
* The assigned VLAN was deleted on one of the devices, so the port is inactive.
* **The assigned VLAN was shut down.**
* The connecting ports have different native VLANs set.

	* One of the connecting switch ports is administratively shut down.
	* The assigned VLAN was shut down.
	-
	If a port or the VLAN assigned to it are shut down, no traffic can flow through. Both ports were assigned to the default VLAN 1, which cannot be deleted, so this cannot be a reason for inactivity. The native VLAN determines which VLAN is allowed to remain untagged and is only set on trunk ports. Ports negotiate mode only when DTP mode is configured on at least one side. Static access ports do not send out DTP packets automatically.
	
	To shut down a VLAN in Cisco, you can try these steps:
	switch0(config)#interface vlan 2
	switch0(config-if)#shutdown
	switch0(config-if)#end
	switch0#show vlan brief
--------
Which three types of devices are typically connected to access switches in an enterprise network? (Choose three.)
* **desktops**
* firewalls
* **printers**
* **IP phones**
* routers

	* desktops
	* printers
	* IP phones
	-
	Access switches are used for connectivity of end-nodes. Firewalls and routers are connected to core or distribution switches.
--------
Why are the SSH and HTTPS protocols preferred for management traffic?
* Because more detailed logging is possible.
* **Because they encrypt the management traffic.**
* Because they provide single sign-on capabilities.
* Because they prevent unauthorized logins.

	Because they encrypt the management traffic.
	-
	HTTPS and SSH are secure versions of HTTP and Telnet. They encrypt login credentials, as well as subsequent management communication. Logging levels remain the same, no matter how we connect. Telnet and HTTP can also present login prompt, and prevent unauthorized logins. Single sign-on is not a function of encrypted communication.
--------
Refer to the exhibit. Which menu item should you select to configure Simple Network Management Protocol (SNMP) trap options in the wireless network?
* Controller
* **Management**
* Monitor
* Security

	Management
	-
	You use the Monitor menu option to view the information that the Cisco Wireless Controller (WLC) collects. Under the Controller menu option, you can configure the Cisco WLC parameters, such as dynamic interfaces, the internal DHCP server, Network Time Protocol (NTP), and others. Under the Security menu option, you can configure authentication, security policies, and other security features of a wireless network.
--------
When is an architecture design called a "collapsed core architecture"?
* **When the core and the distribution layer are merged into one layer.**
* When the core layer fails to provide fault tolerance.
* When the backbone and the access layer are merged into one layer.
* When the distribution and access layer are merged into the core layer.

	When the core and the distribution layer are merged into one layer.
	-
	In smaller networks, core and distribution layers are often combined in order to reduce cost. Collapsed core is the name for a network architecture and does not indicate the lack of a feature. The backbone layer is a synonym for the core layer. An access layer can only be combined with the distribution layer. In a collapsed core architecture, there are two distinctive layers and not only one.
--------
From the assigned address space, allocate the second available VLSM segment to segment B so that it can accommodate five end devices. Note that the first available segment was already used for segment A (172.16.31.0/29).
On R2, configure the Ethernet0/1 interface with the last available IPv4 address in the chosen segment.
On PC1, configure the Ethernet0/0 interface with the first available IPv4 address in the chosen segment.
On PC1, configure the default gateway.
Continue with VLSM subnetting and allocate the next available VLSM segment to segment C. Choose the subnet size so that it exactly meets addressing requirements as represented by the topology.
On R1, configure Ethernet0/2 interface with the first available IPv4 address from the chosen VLSM segment.
On R4, configure Ethernet0/0 interface on R4 with the last available IPv4 address from the chosen VLSM segment.

Examine the configurations of the devices in segment A. Which two address configuration mistakes were made? (Choose two.)
* **The IPv4 address was incorrect on R1.**
* The IPv4 address was incorrect on R2.
* The IPv4 address was incorrect on R3.
* The subnet mask was incorrect on R1.
* **The subnet mask was incorrect on R3.**

	* The IPv4 address was incorrect on R1.
	* The subnet mask was incorrect on R3.
	-
	The R1 router had an IP address of 172.16.31.9 set, which is not part of the first VLSM network (172.16.31.0/29). The subnet mask on R3 was 255.255.255.240, which sets a bigger network (14 hosts) than is necessary.
--------
What is the maximum cable length of an unshielded twisted-pair (UTP) cable that still guarantees full connectivity?
* 80 m
* **100 m**
* 120 m
* 150 m

	100 m
	-
	Maximum UTP cable length is limited due to physical limitations of copper wires, where signal strength degrades with distance.
--------
Which type of Cisco switch memory location stores the MAC address table?
* **content-addressable memory (CAM)**
* flash
* non-volatile random-access memory (NVRAM)
* read-only memory (ROM)

	content-addressable memory (CAM)
	-
	The MAC address table is stored in the CAM, which enables fast lookups. The flash memory typically stores the operating system files. NVRAM stores the startup configuration file. ROM contains the bootstrap code, the power-on self-test (POST) code and the operating system version with only basic functionalities.
--------
When using a AAA server along with an access switch, which two features benefit from centralized authentication? (Choose two.)
* IPsec VPN access
* **management access**
* **network access**
* network telemetry authentication
* spanning tree authentication

	* management access
	* network access
	-
	By having a switch communicating to an authentication server, it is possible to authenticate a user's network access using 802.1X or other methods. It is also possible to authenticate administrative management sessions, such as SSH or HTTPs remote sessions.
--------
In Cisco PVST+, how many root ports per VLAN are allowed on a device?
* **1**
* 8
* 24
* 32

	1
	-
	This port exists on non-root bridges. Only one root port is allowed per switch or per VLAN in Cisco PVST+. The root port forwards traffic toward the root bridge.
--------
Lab Work 7 begins:
------------------
On R1, configure port forwarding so that Telnet connections to SRV1 are possible from outside networks. For the public IPv4 address, use the IPv4 address of the Ethernet 0/3 interface. For the publicly accessible port, use 2323.
Ensure that traffic from the 10.10.2.0/24 subnet is dynamically translated, using the following pool of public addresses: 209.165.202.128/27.
Ensure that traffic from the 10.10.1.0/24 subnet is translated to the IPv4 address of the Ethernet 0/3 interface on R1.

Which command should you use to access SRV1 from SRV2 using Telnet?
* telnet 10.10.2.20 23
* telnet 10.10.2.20 2323
* telnet 198.51.100.2 23
* **telnet 198.51.100.2 2323**

	telnet 198.51.100.2 2323
	-
	The private address 10.10.2.20 is not reachable from SRV2. The public IP address 198.51.100.2 is configured on R1 Ethernet0/3. R1 Ethernet0/3 is reachable from SRV2, but you should not use Telnet to connect to R1. The port forwarding or static NAT translation on R1 translates IP 198.51.100.2 port 2323 into IP 10.10.2.20 and port 23.

When you use Telnet to connect from SRV2 to the IP 198.51.100.2 and port 2323, what message should you get?
* % Connection refused by remote host
* Password required, but none set
* **Welcome!**
* Please log in!

	**Welcome!**

On PC1, issue the ping command to verify connectivity to SRV2. What is the result that you see?
* .....
* **U.U.U**
* !.!.!
* !!!!!

	U.U.U
	-
	There is an access list configured on the SRV2 Ethernet0/0 interface that only permits ICMP packets from 209.165.202.128/27. Based on the R1 configuration, the PC1 IP is translated into R1 Ethernet0/3 (198.51.100.2), and this is why the ping is denied by the SRV2 Ethernet0/0 access list.

Examine the routing table on R2. What does the subnet 209.165.202.128/27 in the static entry refer to?
* **SRV1 to R1 public segment**
* R1 to R2 public segment
* R2 to SRV2 public segment
* SRV1 to R1 private segment

	SRV1 to R1 public segment
	-
	The traffic from the 10.10.2.0/24 subnet is dynamically translated into the pool of public addresses 209.165.202.128/27.
Lab Work 7 ends:
----------------
--------
Lab Work 6 begins:
------------------
Configure symmetric static routing with the following requirements:
All IPv4 traffic originating from PC1(10.10.1.0/24) or PC2(10.10.2.0/24), and destined to SRV1(10.10.3.0/24), must pass through router R2 before reaching router R3.
All IPv6 traffic originating from PC1 or PC2, and destined to SRV1, must pass through router R1 before reaching router R3.
Verify that there is connectivity from each network segment to every other network segment.

How many static routing entries did you have to add to the IPv4 routing table on R3?
* **1**
* 2
* 3
* 6

	1
	-
	On R3, you have to add a single IPv4 static route for the 10.10.1.0/24 network. The route point to the IPv4 address of R2(10.1.1.6), since all IPv4 traffic must pass through the R2 router.

Trace the path that IPv4 packets take from PC1 to SRV1. What is the hop sequence that the packets follow?
* **PC1 > R1 > R2 > R3 > SRV1**
* PC1 > R1 > R2 > R3 > SW3 > SRV1
* PC1 > R1 > R3 > SW2 > SRV1
* PC1 > SW1 > R1 > R2 > R3 > SRV1

	PC1 > R1 > R2 > R3 > SRV1
	-
	SW1 and SW3 do not participate in Layer 3 processing of either ICMP or UDP messages that are generated by the traceroute tool. If the static routing was correctly configured as instructed, traffic should flow from PC1 through R1, R2, and R3, and terminate at SRV1.

Trace the path that IPv6 packets take from PC1 to SRV1. What is the hop sequence that the packets follow?
* PC1 > SW1 > R1 > R2 > R3 > SRV1
* **PC1 > R1 > R3 > SRV1**
* PC1 > R1 > R3 > SW3 > SRV1
* PC1 > R1 > R2 > SRV1
* PC1 > SW1 > R1 > R2 > R3 > SW3 > SRV1

	PC1 > R1 > R3 > SRV1

On R3, shut down the interface toward R2. On PC1, issue the ping command toward the IPv4 address of SRV1. What is the result?

	**ping is unsuccessful (0%)**
	-
	If static routing was correctly configured and connection between R2 and R3 disabled, the ping is unsuccessful, because no traffic can pass between R2 and R3. The unreachable network error is returned if no route (default or otherwise) exists on PC1 to the network of SRV1.

Lab Work 6 ends:
----------------
--------
Which three operations can an SNMP manager process perform in a network? (Choose three.)
authenticate users accessing a device
* **configure a device**
* construct a management information base (MIB) on a device
* **retrieve data about the license of the device**
* **retrieve data about the environmental parameters of a device**

	* configure a device
	* retrieve data about the license of the device
	* retrieve data about the environmental parameters of a device
	-
	SNMP is not used to perform authentication of users accessing a device. The authentication performed by SNMP applies to the SNMP agent and SNMP manager processes. The MIB is an information storage location that organizes configuration and status data into a tree structure, and is pre-defined on a platform or a product.
--------
For which network entity is the OSPF designated router/backup designated router (DR/BDR) selection performed?
* **for each multi-access segment**
* for each OSPF router ID
* for the entire OSPF area
* per transmission state of the link

	for each multi-access segment
	-
	The DR/BDR election is not made per area, per OSPF version, or per transmission state of the link.
--------
Lab Work 5 begins:
------------------
Verify the configurations on SW1 and SW2 and answer questions 1, 2, and 3.
Correct the deliberately introduced configuration mistakes on switches SW1 and SW2 using the answers to questions 1, 2, and 3 as guidelines. After modifying the configurations, answer question 4.
On SW3, configure what is necessary to ensure full connectivity within VLAN 65 and VLAN 80. In other words, make sure that there is connectivity between the PC1 and PC2, and between Server1 and Server2. Answer questions 5 and 6.
VLAN
Name
65
Users1
13
Users2
80
Servers

Examine the initial switch configuration. Which VLAN does Server1 belong to?
* 13
* **60**
* 65
* 80

	60
	-
	Server1 is connected to SW1 Ethernet0/2. The initial SW1 configuration shows that the interface Ethernet0/2 belongs to VLAN 60. To ensure connectivity in VLAN 80, you need to change SW1 Ethernet0/2 from VLAN 60 to VLAN 80.

Examine the initial SW1 configuration. What is the name of VLAN 60?
* **5ervers**
* Servers
* Users1
* Users2

	5ervers
	-
	VLAN 60 is misconfigured on the SW1 switch and should be removed. The VLAN name has the digit 5 in place of the letter S.

What are the physical layer and data layer status codes of the Ethernet0/2 interface on the SW1 switch?
* The physical layer status code is administratively down and the data layer status code is administratively down.
* **The physical layer status code is administratively down and the data layer status code is down.**
* The physical layer status code is down and the data layer status code is down.
* The physical layer status code is up and the data layer status code is up.

	The physical layer status code is administratively down and the data layer status code is down.
	-
	The show ip interface brief command issued on the SW1 initially shows Ethernet0/2 as being administratively shutdown.

After you have resolved VLAN configuration issues on all switches, test connectivity from PC1 to Server1, Server2, PC2, and PC3on PC1 using the ping command. What are the results of the ping connectivity tests from PC1?
* The connectivity test is successful to PC2 and to PC3.
* **The connectivity test is successful to PC2 and unsuccessful to Server2.**
* The connectivity test is successful to PC3 and unsuccessful to Server2.
* The connectivity test is successful to Server2 and unsuccessful to PC2.

	The connectivity test is successful to PC2 and unsuccessful to Server2.
	-
	The ping tests are successful between devices in the same VLAN: VLAN 65 (connects PC1 and PC2), VLAN 80 (connects Server1 and Server2), and VLAN 13 (connects only PC3).

Examine the running configurations of switches. Notice that the SW1 and SW3 running configurations display VLAN information, like the one shown in the example output below. Why are there no VLANs listed in the SW2 running configuration?
* vlan 13 name Users2 ! vlan 65 name Users1 ! vlan 80 name Servers
* SW2 has no VLANs configured, but SW1 and SW3 have VLANs 13, 65, and 80 configured.
* **SW2 is configured as VTP mode Server or Client, but SW1 and SW3 are configured as VTP mode Transparent.**
* SW2 is configured as VTP mode Transparent, but SW1 and SW3 are configured as VTP mode Server or Client
* This is a Cisco IOS software bug and is easily resolved by reloading SW1.

	SW2 is configured as VTP mode Server or Client, but SW1 and SW3 are configured as VTP mode Transparent.
	-
	When a switch is configured with VTP mode Transparent, the VLAN configuration is stored in the startup and running configurations. However, when the VTP mode is Server or Client, the VLAN configuration is stored in the vlan.dat file, and not in the running and startup configurations.

After you have resolved VLAN connectivity, what is the expected result of the following ping command issued on Server2?
ping 255.255.255.255 repeat 2
* one response from Server1 (192.168.80.1) and one response from PC1 (192.168.65.1)
* **two responses from Server1 (192.168.80.1)**
* two responses from Server1 (192.168.80.1) and two responses from PC1 (192.168.65.1)
* two responses from an unknown host (255.255.255.255)

	two responses from Server1 (192.168.80.1)
	-
	The ping connectivity test to address 255.255.255.255 is broadcasted to all hosts in VLAN 80, where Server1 and Server2 are located. No other host from a different VLAN will respond to this ping connectivity test. The "repeat" keyword specifies the number of ping connectivity test probes and responses.
Lab Work 5 ends:
----------------
--------
To which Open Systems Interconnection (OSI) layer are router-specific functions mapped?
* Layer 1
* Layer 2
* **Layer 3**
* Layer 4

	Layer 3
	-
	Layer 3 is the network layer. OSI Layer 1 is the physical layer, Layer 2 is handled by network switches, and Layer 4 defines the transport protocols (TCP or UDP).
--------
HQ# show ip route 
<... output omitted ...> 
Gateway of last resort is not set 10.0.0.0/8 is variably subnetted, 3 subnets, 3 masks 
D 10.1.0.0/16 [90/409600] via 172.16.1.2, 00:03:52, Ethernet0/1 
D 10.1.1.0/24 [90/307200] via 172.16.1.2, 00:03:52, Ethernet0/1 
C 10.1.1.8/30 is directly connected, Serial0/0/0 
L 10.1.1.9/32 is directly connected, Serial0/0/0 
<... output omitted ...>

Refer to the exhibit. Which route will a packet with the destination IPv4 address of 10.1.1.12 match?
* 0.0.0.0/0
* 10.1.0.0/16
* **10.1.1.0/24**
* 10.1.1.8/30

	10.1.1.0/24
	-
	The 10.1.0.0/16 route and the destination IPv4 address 10.1.1.12 also match, but only in the first 16 bits. The route to 10.1.1.8/30 does not provide matching in all 30 bits. Since there is a route matching for the destination IPv4 address, the default route is not going to be used.
--------
Which language is used in the Cisco Network Services Orchestrator (NSO) to describe the network service intent?
* Python
* XML
* YAML
* **YANG**

	**YANG**
--------
How are NETCONF messages encoded?
* by using CSS
* by using JSON
* by using SQL
* **by using XML**

	by using XML
--------
A company wants to interconnect all its branches. To ensure minimum downtime, the company wants to use a WAN that provides high availability and high redundancy. Which WAN topology should the company use?
* **full mesh**
* hub-and-spoke
* partial mesh
* ring

	full mesh
	-
	In a full mesh topology, each node in the network can communicate directly with any other node. Also, full mesh topology has the largest number of redundant paths, which prevents downtime in case of a node or connection failure. Hub-and-spoke topology connects all spoke nodes to a central node, and spokes communicate between each other through a hub. The hub represents a single point of failure. In a ring topology, the number of redundant paths is lower than in a full mesh topology.
--------
Refer to the exhibit. The service provider is implementing Multiprotocol Label Switching Virtual Private Network (MPLS VPN) service. Which two options indicate the specific VPN type that is implemented and how the service provider appears from the perspective of the customer? (Choose two.)
* The service provider is implementing MPLS L2VPN.
* **The service provider is implementing MPLS L3VPN.**
* The service provider is implementing MPLS VPLS.
* **The service provider network can be represented as a router from the customer perspective.**
* The service provider network can be represented as a switch from the customer perspective.

	* The service provider is implementing MPLS L3VPN.
	* The service provider network can be represented as a router from the customer perspective.
--------
Which three protocols use UDP? (Choose three.)
* **DHCP** - Dynamic Host Configuration Protocol
* FTP - File Transfer Protocol
* HTTPS - HyperText Transfer Protocol Secure
* **SNMP** - Simple Network Management Protocol
* **TFTP** - Trivial File Transfer Protocol

	* DHCP
	* SNMP
	* TFTP
	-
	DHCP is a network management protocol used on UDP/IP networks whereby a DHCP server dynamically assigns an IP address and other network configuration parameters to each device on a network. TFTP is used to transfer configuration files, Cisco IOS images, and other files between systems. SNMP is an application layer protocol that facilitates the exchange of management information between network devices. FTP is a connection-oriented service that uses TCP to transfer files between systems. HTTPS uses TCP for distributed, collaborative hypermedia information systems.
--------
Which two of the following are characteristics of the **modified EUI-64 format when used to create an IPv6 address**? (Choose two.)
* **It creates an interface ID based on the MAC address of the interface.**
* **It ensures uniqueness of the interface ID.**
* It is used when an IPv6 address is assigned by the DHCPv6 server.
* It is used when an IPv6 address is manually configured.
* It creates an interface ID using a randomly generated number.

	* It creates an interface ID based on the MAC address of the interface.
	* It ensures uniqueness of the interface ID.
	-
	One way to guarantee that the interface ID is unique is to base it on the MAC address of the interface. The EUI-64 format is based on unique MAC addresses. Therefore, using the EUI-64 format, a device can automatically assign itself a unique 64-bit IPv6 interface ID without the need for manual configuration or DHCP. The interface ID can be created using a randomly generated number, but this is not the case when using the EUI-64 format.
--------
Which three statements describes characteristics of **solicited-node IPv6 addresses**? (Choose three.)
* There can be only one per device.
* **They are automatically created by the device.**
* They are created using the device's MAC address.
* **They are multicast addresses.**
* They are valid within an organization.
* **They have a recognizable prefix.**

	* They are automatically created by the device.
	* They are multicast addresses.
	* They have a recognizable prefix.
	-
	A solicited-node multicast IPv6 address is created using special mapping of the device's unicast address with the recognizable solicited-node multicast prefix of ff02:0:0:0:0:1:ff00::/104. A device can have multiple solicited-node multicast addresses, because the multicast addresses are automatically created for every unicast address on a device.
--------
Which two situations result in the default VLAN being assigned to a port? (Choose two.)
* The administrator issued the switchport access vlan DEFAULT command.
* **The administrator sets the interface back to defaults using the default interface command.**
* The non-default VLAN that is assigned to the port is administratively down.
* The non-default VLAN that was assigned to the port was deleted.
* **The administrator did not assign any VLAN to the interface**

	* The administrator sets the interface back to defaults using the default interface command.
	* The administrator did not assign any VLAN to the interface
	-
	VLAN 1 is the default VLAN. When a switch boots with the factory configuration, all the ports are placed in VLAN 1. Another way to ensure a port is in the default VLAN is to clear the interface configuration by issuing the default interface command. Shutting down or deleting a non-default VLAN that was previously assigned to a port does not modify interface configuration.
--------
When configuring a trunk port on a Cisco switch, which VLAN ranges can be used to specify the allowed VLANs?
* **extended and standard**
* extended
* standard
* standard and reserved

	extended and standard
	-
	A trunk port is a member of all VLANs by default, including extended-range VLANs, but membership can be limited by configuring the allowed-VLAN list.
--------
Which client software do you require in order to use the Cisco Wireless LAN Controller (WLC) GUI?
* Java client
* NETCONF client
* terminal emulator
* **web browser**

	**web browser**
--------
What can you use to **bundle multiple ports on the Cisco Wireless LAN Controller** (WLC) to provide **port redundancy and load-balancing**?
* Dynamic Trunking Protocol (DTP)
* Gateway Load Balancing Protocol (GLBP)
* **Link Aggregation Group (LAG) protocol**
* Virtual Router Redundancy Protocol (VRRP)

	**Link Aggregation Group (LAG) protocol**
	-
	Both VRRP and GLBP are used to provide default gateway redundancy, not link redundancy. DTP is used to negotiate a trunk between two DTP-capable devices without manual configuration.
--------
Which three layers does the hierarchical three-tier model include? (Choose three.)
* **access**
* **core**
* data link
* **distribution**
* network

	* access
	* core
	* distribution
	-
	The access layer provides a physical connection for devices to access the network. The distribution layer represents a communication point that routes and filters traffic. The core layer provides high-speed packet forwarding and redundancy, and is the aggregation point for the rest of the network. The data link and network layers are part of the OSI model.
--------
Lab Work 4 begins:
------------------
The devices are pre-configured with the basic connectivity requirements.

Your task is to configure additional Layer 2 security features on a Cisco network switch.

The logging-on switch is configured so only alerts and emergencies are sent to the console.

Carefully examine the pre-existing configuration of SW1 and answer questions 1, 2, and 3. Then perform the configuration tasks and answer questions 4 and 5.

Perform the following tasks:

Configure port security on SW1 on the port that is connected to PC1 to allow the MAC addresses of the first two devices that connect to the port. If any additional devices are connected to this port, the port must drop all packets, but it must not increment the security-violation count.

Configure port security on SW1 on the ports that are connected to PC2 and the Inventory server to allow a maximum of two MAC addresses. Configure the port so it remembers the MAC addresses of the first two devices that connect to the port. If any additional devices are connected to this port, the port must drop all packets and increment the security-violation count.

On SW1, what is the state of the port connecting to the Inventory server?
* connected
* disabled
* **err-disabled**
* shutdown

	err-disabled
	-
	You can check the status of the interface with the show interfaces Ethernet 0/3 command. The err-disabled interface is the result of Security Action Shutdown.

From PC2, ping Ethernet0/0 interface of the Border router. What is the cause for ping to fail?
* Another device with the same MAC is connected to the switch Ethernet0/2 interface.
* The switch interface Ethernet0/2 is administratively shutdown.
* **The maximum number of sticky MACs is already reached for switch interface Ethernet0/2.**
* The wrong static MAC is allowed on the switch interface Ethernet 0/2.

	The maximum number of sticky MACs is already reached for switch interface Ethernet0/2.
	-
	Verify the interface configuration with the show running-config interface Ethernet 0/2 command. You can see that the maximum number of MAC addresses allowed on the interface is two and that there are two static addresses configured. That is why a new MAC address will not be learned via the sticky MAC feature.

What is the Security Violation counter for the Ethernet 0/3 interface on SW1?
* 0
* **1**
* 2
* 16

	1
	-
	You can check the Security Violation counter with the show port-security command.

What is the port-security status of the Ethernet 0/1 interface on SW1?
* Administrative shutdown
* Secure-down
* Secure-shutdown
* **Secure-up**

	Secure-up
	-

Verify the line protocol status of the Ethernet0/3 port on SW1. How would you correct the issue?
* Clear the MAC address table.
* Reload the Inventory server.
* **Shut down and enable the interface on SW1.**
* Shut down and enable the interface on the Inventory server.

	Shut down and enable the interface on SW1.
	-
	To return the interface to working status, you must issue the shutdown command, followed by the no shutdown command. You can also issue the errdisable recovery command to recover err-disabled ports, depending on the cause.

Lab Work 4 ends:
----------------
--------
The **copper cabling used in your network is too close to electrical interferences.** Consequently, the interface statistics show an unusually large number of compromised frames. While you attempt to solve the issue, **which frame forwarding method should you implement on the Cisco switches in order to lower the number of compromised frames?**
* cut-through
* express forwarding
* process switching
* **store-and-forward**

	**store-and-forward**
--------
When configuring an IPv4 static route pointing to the next-hop IPv4, which command should you use?
* **ip route 172.16.1.0 255.255.255.0 172.16.2.1**
* ip route 172.16.1.0 net-mask 255.255.255.0 next-hop 172.16.2.1
* ip route 172.16.1.0/24 172.16.2.1
* ip route static 172.16.1.0 net-mask 255.255.255.0 next-hop 172.16.2.1

	ip route 172.16.1.0 255.255.255.0 172.16.2.1
	-
	When configuring a static route, you must specify an IPv4 destination network (172.16.1.0 255.255.255.0), then use the IPv4 address of the next-hop router (172.16.2.1).
--------
Refer to the exhibit. Which of the routes is a floating static route?

BR2# show ip route
<... output omitted ...>
Gateway of last resort is 172.16.2.1 to network 0.0.0.0
D*EX 0.0.0.0/0 [170/307200] via 172.16.2.1, 00:03:01, Ethernet0/0
10.0.0.0/8 is variably subnetted, 8 subnets, 4 masks
D 10.8.0.0/13 [90/435200] via 172.16.2.1, 00:02:58, Ethernet0/0
D 10.64.0.0/14 is a summary, 00:03:04, Null0
C 10.64.0.0/16 is directly connected, Loopback0
L 10.64.0.1/32 is directly connected, Loopback0
172.16.0.0/16 is variably subnetted, 3 subnets, 2 masks
D 172.16.1.0/30 [90/307200] via 172.16.2.1, 00:03:01, Ethernet0/0
C 172.16.2.0/30 is directly connected, Ethernet0/0
L 172.16.2.2/32 is directly connected, Ethernet0/0
S 192.168.16.0/24 [90/0] via 172.16.2.1
S 192.168.33.0/24 [1/0] via 172.16.2.1
209.165.200.0/27 is subnetted, 1 subnets
D 209.165.200.224 [90/307200] via 172.16.2.1, 00:03:01, Ethernet0/0

* route to network 10.8.0.0/13
* route to network 172.16.1.0/30
* **route to network 192.168 16.0/24**
* route to network 192.168.33.0/24

	route to network 192.168 16.0/24
	-
	A floating static route is a static route with an administrative distance greater than the default value of 1. In the example we have two static routes, the route to network 192.16.33.0/24 has the default administrative distance, and is therefore not floating static. The other two options are routes sourced from elsewhere, in this case from the EIGRP routing protocol, as indicated by the "D" protocol code.
--------
Which of the following is the correct binary representation of the third octet of the IPv4 address 172.20.**170**.50?
* 0001 1110
* 0110 0110
* **1010 1010**
* 1100 1011

	1010 1010
	-
	The decimal value of 170 converts to 1010 1010 in binary.
--------
How many switch ports are designated ports on a root bridge?
* **all of them**
* none of them
* one
* two

	all of them
	-
	For root bridges, all switch ports are designated ports. Non-root bridges have only one designated switch port.
--------
Which issue is eliminated when using PortFast?
* bandwidth throttling
* **DHCP timeout**
* duplex mismatch
* native VLAN mismatch

	DHCP timeout
	-
	When a device is connected to the switch, it sees the interface port as up and it immediately wants to get the IP from the DHCP. However, STP needs time to transition ports to the forwarding state. PortFast solves this issue by not setting STP on that port. STP and PortFast do not have a function for purposely throttling the bandwidth. Duplex mismatch may happen if the auto-negotiating feature is enabled on one device and not on the other. A native VLAN mismatch error happens when you have different native VLAN numbers on connected devices.
--------
Lab Work 3 begins:
------------------
Enable OSPF for routing information exchange on routers R1, R2, and R3. Use the following router IDs:
R1: 1.1.1.1
R2: 2.2.2.2
R3: 3.3.3.3
On R1, configure OSPF so that it advertises its default route to other OSPF-enabled routers.
Verify the routing tables on all routers. The routes to all networks should be visible on all routers to establish full connectivity.

Examine the OSPF configurations on routers in the multi-access segment, that is R1, R2, and R3. OSPF priority has been pre-configured on all routers. If all the routers would reboot at the same moment, which two routers would be elected as Designated Router (DR) and Backup Designated Router (BDR)?
* R1 is DR and R2 is BDR.
* **R1 is DR and R3 is BDR.**
* R2 is DR and R4 is BDR.
* R3 is DR and R1 is BDR.

	R1 is DR and R3 is BDR.
	-
	Upon examining the interface OSPF configurations, you will see that R1 is given the preferable priority, which ensures it would be elected as DR. The OSPF priority of R3 compared to R2 is preferred.

What are the OSPF hello and dead timer values on R2?
* **Hello is 10 seconds and dead is 40 seconds.**
* Hello is 20 seconds and dead is 40 seconds.
* Hello is 30 seconds and dead is 120 seconds.
* Hello is 60 seconds and dead is 120 seconds.

	Hello is 10 seconds and dead is 40 seconds.
	-
	The other options are incorrect.

In the routing table on R2, what is the protocol code for the default route?
* D
* D*EX
* **O*E2**
* O*IA
* S*

	O*E2
	-
	The "D" and "DEX" protocol codes indicate routes that were learned by the EIGRP routing process. "S" would indicate a static default route.

The R4 router is not participating in OSPF. What is causing the issue?
* OSPF is disabled on the R4 interface connecting to R1.
* **The OSPF area is configured incorrectly on R4.**
* The OSPF process ID is configured incorrectly on R4.
* The router ID is configured incorrectly on R4.

	The OSPF area is configured incorrectly on R4.
	-
	For OSPF to advertise routes, the area ID must be the same on all routers in a single-area OSPF domain. The router ID uniquely identifies the router; it must be unique on each router in the network, and the OSPF process ID do not need to be agreed upon by two interconnected routers.

Lab Work 3 ends:
----------------
--------
The console of a device you are administering displays the following syslog message:

%LINK-3-UPDOWN: Interface FastEthernet0/0, changed state to down

What is the severity level of the displayed syslog message?
* **Error**
* Log alert
* Log audit
* System daemon
* Warning

	Error
	-
	The general format of syslog messages that the syslog process on Cisco IOS Software generates by default is: seq no:time stamp: %facility-severity-MNEMONIC:description. The "LINK" word of the message indicates which facility is the source of the message. The syslog RFC defines these sources by a numeric value. Cisco facilities are a free-form method of identifying the source message type such as SYS, IP, LDP, L2, MEM, FILESYS, DOT11, LINEPROTO, and so on. Facility indication is followed by a value representing severity. The value 3 corresponds to the severity level called Error, which indicates an error condition.
--------
Which IPv6 command on a Cisco router can be used to provide the name-to-IP address resolution in case the DNS service in the network fails?
* `hostname TFTP-SERVER 2001:db8:a:a::69`
* `ipv6 host TFTP-SERVER interface Gi0/0`
* **`ipv6 host TFTP-SERVER 2001:db8:a:a::69 2001:db8:a:a::169`**
* `ipv6 hostname TFTP-SERVER 2001:db8:a:a::69`

	`ipv6 host TFTP-SERVER 2001:db8:a:a::69 2001:db8:a:a::169`
	-
	To define a static host name to address mapping in the host name cache, use the ipv6 host name [port] ipv6-address command in global configuration mode. The syntax of the command requires that you enter the host's name followed by one or more associated IPv6 addresses. Optionally, you can specify the port number. To remove the hostname-to-address mapping, use the no form of this command.
--------
Where does a router that runs OSPFv2, and that has neighbor adjacencies established, store link-state advertisements (LSAs)?
* **LSDB**
* Neighbors table
* Routing table
* SPF tree

	LSDB
	-
	An LSA is a type of packet containing information about adjacent routers and networks that it is connected to. A router stores LSAs in the link-state database (LSDB), which is then used for the calculation of optimal paths through the network.
--------
Which series of phases correctly represents a common attack methodology?
* **Initial Compromise > Escalation of Privileges > Reconnaissance of internal hosts > Lateral movement > Exfiltration**
* Lateral movement > Escalation of Privileges > Reconnaissance of internal hosts > Initial Compromise > Exfiltration
* Lateral movement > Reconnaissance of internal hosts > Escalation of Privileges > Initial Compromise > Exfiltration
* Reconnaissance of internal hosts > Escalation of Privileges > Initial Compromise > Lateral movement > Exfiltration

	Initial Compromise > Escalation of Privileges > Reconnaissance of internal hosts > Lateral movement > Exfiltration
	-
	Although a unique attack methodology does not exist, the commonly used attack proceeds in the following phases. Initial Compromise—compromising a low-security system to start analyzing the internal network; Escalation of Privileges—getting more options to scan the internal network; Internal Reconnaissance—scanning the internal network to detect an interesting system to compromise; Lateral Movement—compromising others' internal hosts; Exfiltration—data theft.
--------
Where in the network should you implement QoS packet classification?
* **at the input interface of a device at the LAN access edge of the network**
* at the input interface of a device at the WAN edge of the network
* at the output interface of a device at the LAN access edge of the network
* at the output interface of a device at the WAN edge of the network
 
	at the input interface of a device at the LAN access edge of the network
	-
	Classification should take place at the network edge, typically in the wiring closet, at trusted network endpoints, such as IP phones. It is recommended that classification occurs as close to the source of the traffic as possible. Congestion avoidance mechanisms, policing and shaping are commonly used at the WAN edge of the network.
--------
Choose the client technique for delivering electric power along with data to endpoint devices.
* Dynamic Host Configuration Protocol (DHCP)
* **Power over Ethernet (PoE)**
* Quality of Service (QoS)
* Secure Shell Host (SSH)

	Power over Ethernet (PoE)
	-
	Power over Ethernet (PoE) is a technique for delivering DC power to devices over copper Ethernet cabling, eliminating the need for separate power supplies and outlets.
--------
Which two conditions must be met on a router so that a route marked "C" shows up in the output of the show ip route command? (Choose two.)
* **A valid IP address is configured on the interface.**
* Routing adjacency is established between two routers.
* **The interface has Layer 1 and Layer 2 connectivity.**
* The ip route mark connected command is issued for the route.
* The same routing process ID must be set on both routers.

	* A valid IP address is configured on the interface.
	* The interface has Layer 1 and Layer 2 connectivity.
	-
	The interface must have a valid IP address configured and be in up/up state. Therefore, the shutdown command should not exist in the interface configuration. Route entries that are originated by routing protocols appear in the routing table marked with protocol codes other than "C."
--------
On a router that does not have a default route in the routing table, you issue the following two commands:
Router(config)# ip route 0.0.0.0 0.0.0.0 10.10.10.10 20 
Router(config)# ip route 0.0.0.0 0.0.0.0 10.20.250.2 10
What is the result of executing the commands?
* Both routes are installed in the routing table as default routes.
* The route pointing to the IPv4 address 10.10.10.10 is installed as the default route.
* **The route pointing to the IPv4 address 10.20.250.2 is installed as the default route.**
* There are no changes to the routing table.

	The route pointing to the IPv4 address 10.20.250.2 is installed as the default route.
	-
	The ip route command can specify the administrative distance in its arguments. When two routes are configured to the same destination network, the one with the lower administrative distance will be installed in the routing table.
--------
What are the three tasks of an Intrusion Prevention System (IPS)? (Choose three.)
* **blocking suspicious activity**
* inspecting suspicious activity
* **logging suspicious activity**
* **reporting suspicious activity**
* tracing suspicious activity

	* blocking suspicious activity
	* logging suspicious activity
	* reporting suspicious activity
	-
	Inspecting and tracing suspicious activity falls out of the scope of an IPS system and is achieved separately.
--------
The devices in the topology are pre-configured with IP addressing and can communicate with each other. You need to configure and verify the time-related configuration which will allow devices to synchronize time in a pre-determined way.

Perform the following tasks:
Examine the current NTP and time zone configuration on the devices.
Configure R1 as the NTP master with stratum = 1.
Configure R2 and SW to synchronize time directly with R1.

After configuring R2 and SW to synchronize their clocks directly to R1, what are the stratum levels of R2 and SW?
* The R2 stratum level is 1 and the SW stratum level is 1.
* **The R2 stratum level is 2 and the SW stratum level is 2.**
* The R2 stratum level is 2 and the SW stratum level is 3.
* The R2 stratum level is 3 and the SW stratum level is 3.

	The R2 stratum level is 2 and the SW stratum level is 2.
	-
	Because both R2 and SW are synchronizing time directly with R1, they both have the same stratum value. Because R1 has a stratum value of 1, R2 and SW increment their values by one (to 2).

What is the maximum stratum level that you can configure on a Cisco device?
* 12
* **15**
* 21
* 24

	15
	-
	Cisco IOS allows you to configure stratum levels from 1 to 15.

On the SW switch, display the established NTP associations. What is the value displayed in the address column?
* *~198.51.100.2
* *198.51.100.2
* ~198.51.100.2
* 198.51.100.2

	*~198.51.100.2
--------
Which task controls the download and deployment of software updates?
* compliance checks
* data collection and telemetry
* device provisioning
* **device software management**

	device software management
	-
	Controlling the download and deployment of software updates is a relatively simple task, but it can be time-consuming, and may be subject to human error. Many automated tools have been created to address this issue, but they can lag behind customer requirements. A simple network programmability solution for device software management is beneficial in many environments.
--------
What is the default VLAN of a port on a Cisco switch?
* VLAN 0
* **VLAN 1**
* VLAN 2
* VLAN 4

	VLAN 1
	-
	By default, all interfaces are in native VLAN 1. There is no VLAN 0. VLANs 2 and 4 can be configured but are never the default.
--------
Which statement about Service Set Identifiers (SSIDs) is true?
* An administrator can only create one SSID on the same access point.
* **An administrator can create several SSIDs on the same access point.**
* An SSID must be advertised by the Wi-Fi access point.
* An SSID is configured by default on an access point.

	An administrator can create several SSIDs on the same access point
	-
	An SSID is not configured by default. An administrator configures one or more SSIDs on an access point. The administrator can also decide to hide an SSID.
--------
Which devices does the core layer interconnect?
* access layer switches
* access points
* **distribution layer switches**
* end point devices

	distribution layer switches
	-
	A large LAN environment often has multiple distribution layer switches that the core layer switches interconnect together. Access layer switches enable endpoints and devices to connect to the network. End point devices include laptops and phones.
--------
What does a switch on an Ethernet network do if it receives a unicast frame with the destination MAC address that resides at the same switch port as the source frame?
* block the frame
* **drop the frame**
* flood the frame
* forward the frame

	drop the frame
	-
	When the destination MAC address of a received unicast frame resides at the same switch port as the source, the switch drops the frame, which is a behavior known as filtering. Flooding means that the switch sends the incoming frame to all active ports, except the port on which it received the frame.
--------
When using the modified EUI-64 format to create the interface ID of an IPv6 unicast address, which two portions of the Ethernet MAC are used unchanged? (Choose two.)
* Organizational Unique Identifier (OUI) octets
* **network interface card (NIC) specific octets**
* the universal/local bit
* **the unicast/multicast bit**
* the protocol type octet

	* network interface card (NIC) specific octets
	* the unicast/multicast bit
	-
	In an Ethernet MAC address structure, there is no specific type octet. The universal/local bit is the second-least significant bit in the MAC address. In the modified EUI-64 format, it is inverted. As this bit is part of the OUI octets, inverting it changes the value of the OUI octets as well.
--------
What are two differences between the RADIUS and TACACS+ protocols? (Choose two.)
* **RADIUS combines authentication and authorization, while TACACS+ implements two separate processes.**
* RADIUS encrypts the entire payload, while TACACS+ encrypts only the password.
* RADIUS is a TCP-based protocol, while TACACS+ is a UDP-based protocol.
* **RADIUS is a UDP based protocol. TACACS+ is a TCP based protocol.**
* RADIUS supports bidirectional authentication, while TACACS+ supports only unidirectional authentication

	* RADIUS combines authentication and authorization, while TACACS+ implements two separate processes
	* RADIUS is a UDP based protocol TACACS+ is a TCP based protocol
	-
	RADIUS is an open standard that combines authentication and authorization services into a single process. TACACS+ is a Cisco proprietary security mechanism that can be used only for authorization and accounting while using another method of authentication. TACACS+ uses the Transmission Control Protocol (TCP) for all three services.
--------
How can a RADIUS server enhance management security in wireless environments?
* By enforcing access control list (ACL) configurations.
* By preventing brute-force login attempts.
* By providing a stronger encryption.
* **By providing individualized login to specific network devices.**

	By providing individualized login to specific network devices
	-
	ACLs are not controlled by RADIUS servers, RADIUS does not prevent brute-force attacks, and encryption strength is not related to RADIUS server presence or absence.
--------
On a Cisco device, what is the default destination for syslog logging messages?
* **console line**
* logging buffer
* syslog server
* terminal lines

	**console line**
--------
Refer to the exhibit. The administrator has configured Hot Standby Router Protocol (HSRP) to provide default gateway redundancy. Which statement correctly describes the behavior of the network?
* PC1 will be able to reach remote networks if either R1 or R2 fails.
* **PC1 will be able to reach remote networks while R1 is operational.**
* PC1 will not be able to reach remote networks if either R1 or R2 fails.
* PC1 will not be able to reach remote networks if R2 fails.

	PC1 will be able to reach remote networks while R1 is operational
	-
	Because of the explicit default gateway configuration, the ARP table of PC1 has the default gateway IPv4 mapped to the R1 MAC address, and not to the virtual IP address of the HSRP group. When R1 fails, the PC1 ARP table will not be updated, and PC1 will not be able to reach R2, which would take over the role of the default gateway.
--------
HQ# show ip route
<... output omitted ...>
Gateway of last resort is 10.120.255.29 to network 0.0.0.0
O*IA 0.0.0.0/0 [110/11] via 10.120.255.29, 3d08h, FastEthernet2
10.0.0.0/8 is variably subnetted, 29 subnets, 3 masks
O N2 10.120.0.0/16 [110/20] via 10.120.251.29, 3d08h, FastEthernet4
C 10.120.70.0/24 is directly connected, Vlan1
<... output omitted ...>
L 10.120.251.30/32 is directly connected, FastEthernet4
O 10.120.251.32/30 [110/30] via 10.120.251.29, 3d08h, FastEthernet4
S 10.120.253.200/32 is directly connected, Dialer1
O 10.120.254.4/30 [110/31] via 10.120.255.29, 3d08h, FastEthernet2
O 10.120.254.8/30 [110/21] via 10.120.255.29, 3d08h, FastEthernet2
O 10.120.255.4/30 [110/20] via 10.120.255.29, 3d08h, FastEthernet2
O 10.120.255.8/30 [110/30] via 10.120.255.29, 3d08h, FastEthernet2
O 10.120.255.12/30 [110/20] via 10.120.255.29, 3d08h, FastEthernet2
O 10.120.255.20/30 [110/20] via 10.120.255.29, 3d08h, FastEthernet2
O 10.120.255.24/30 [110/20] via 10.120.255.29, 3d08h, FastEthernet2
C 10.120.255.28/30 is directly connected, FastEthernet2
L 10.120.255.30/32 is directly connected, FastEthernet2
O 10.120.255.32/30 [110/20] via 10.120.255.29, 3d08h, FastEthernet2
O 10.120.255.252/30 [110/11] via 10.120.255.29, 3d08h, FastEthernet2 172.24.0.0/16 is variably subnetted, 3 subnets, 3 masks
S 172.24.128.0/23 is directly connected, Dialer1
S 172.24.129.0/24 is directly connected, Dialer1
C 172.24.129.196/32 is directly connected, Dialer1

Refer to the exhibit. What is the administrative distance of the route to network 10.120.254.4/30?
* 1
* 21
* 90
* **110**

	**110**
--------
HQ# show ip route
<... output omitted ...>
Gateway of last resort is not set
10.0.0.0/8 is variably subnetted, 3 subnets, 3 masks
D 10.1.0.0/16 [90/409600] via 172.16.1.2, 00:03:52, Ethernet0/1
D 10.1.1.0/24 [90/307200] via 172.16.1.2, 00:03:52, Ethernet0/1
C 10.1.1.8/30 is directly connected, Serial0/0/0
L 10.1.1.9/32 is directly connected, Serial0/0/0
<... output omitted ...>

Refer to the exhibit. Which route will a packet with the destination IPv4 address of 10.1.1.12 match?
* 0.0.0.0/0
* 10.1.0.0/16
* **10.1.1.0/24**
* 10.1.1.8/30

	10.1.1.0/24
	-
	The 10.1.0.0/16 route and the destination IPv4 address 10.1.1.12 also match, but only in the first 16 bits. The route to 10.1.1.8/30 does not provide matching in all 30 bits. Since there is a route matching for the destination IPv4 address, the default route is not going to be used.
--------
Lab Work 2 begins:
------------------

In this lab, you will secure administrative access to Cisco IOS devices.

The devices have basic addressing configurations in place. You will use end devices as sources of remote access connections.

The following is pre-configured in the lab:

On SW2:

Telnet access parameters

On R1:

Telnet is enabled on remote access lines

remote access lines are configured for password-only login, with the password Cisco111

access list SSHACCESS

You will not be able to access the console of the R1 router directly. However, you will be able to access it from other devices in the topology, as instructed.

Perform the following task:

Using Telnet to access R1, configure SSH with the following parameters:

key size of 2048 bits

domain name example.com

login authentication must be performed against the locally stored user information

create an entry in the local database for one user, using the username AdminPC2, maximum privilege level, and password Cisco123

Examine the access list configuration on R1:

From PC2, access the R1 router using SSH. Apply the configured access list so that it limits remote access to R1 to only SSH connections from PC2.

From PC2, use SSH to access R1. Use AdminPC2 as the username and Cisco123 as the password. What is the IPv4 address of the loopback interface?
* 10.10.2.1
* **10.10.3.1**
* 10.10.4.1
* 10.10.5.1

	10.10.3.1
	-
	If you issue the show ip interface brief command, you will see that there are two interfaces configured. Ethernet0/0 has the IPv4 address 10.10.1.1 and the loopback0 interface has the IPv4 address 10.10.3.1.
--------

In the lab network, which SSHACCESS access list implementation would correctly limit remote access to only SSH connections from PC2?
* inbound direction on the Ethernet0/0 interface on R1
* inbound direction on the Ethernet0/2 interface on SW1
* **inbound direction on the vty lines on R1**
* outbound direction on the Ethernet0/1 interface on SW2
* outbound direction on the vty lines on R1

	inbound direction on the vty lines on R1
	-
	Answer
	The correct answer is inbound direction on the vty lines on R1. The other proposed implementations would also limit other traffic.
--------

Examine the configuration on SW2. Based on the information in the configuration, use Telnet from PC1 to access the SW2 switch. Which message is displayed upon successful access?
* **Access for authorized users only. Proceed with caution.**
* Only authorized access to this device is allowed!
* Unauthorized access prohibited.
* You must have permissions to access this device! If you are not authorized, do not proceed!

    * Access for authorized users only. Proceed with caution.
	-
	Answer
	The correct answer is Access for authorized users only. Proceed with caution. The banner that is displayed when accessing is called the login banner. Another banner that you will see when connecting to SW2 is the message of the day (MOTD) banner. The MOTD banner is displayed to all terminals that are connected and is useful for sending messages that affect all users (such as impending system shutdowns).

Lab Work 2 ends:
----------------
--------
Which mechanism allows an end user to make a request of a network device and receive an answer from that device?
* **application programming interface (API)**
* Cisco Discovery Protocol
* routing protocol
* syslog protocol

	application programming interface (API)
	-
	API is the mechanism by which an end user makes a request of a network device and the network device responds to the end user. This method provides increased functionality and scalability over traditional network management methods. This is the method modern tools use to interact with network devices.
--------
Which mechanism does NETCONF use to install, manipulate, and delete the configuration of network devices?
* OpenFlow
* **Remote Procedure Call (RPC)**
* REST
* RESTCONF

	Remote Procedure Call (RPC)
--------
Which type of address is automatically assigned to a physical interface when IPv6 is enabled on that interface?
* global unicast address
* **link-local address**
* loopback address
* unique local address

	link-local address
	-
	Although an IPv6-enabled device can auto-configure a global unicast address using the Stateless Address Autoconfiguration (SLAAC) process, it first must be configured to perform auto-configuration. Unique local addresses must also be specifically assigned. The loopback address of ::1/128 is automatically configured during system initialization, but cannot be assigned to a physical interface.
--------
What are two valid IPv6 address scopes for a unique local IPv6 address? (Choose two.)
* global
* interface-local
* link-local
* **organization-local**
* **site-local**

	* organization-local
	* site-local
	-
	Unique local IPv6 addresses are equivalents of private IPv4 addresses. They can be considered globally unique, because the probability of duplication is extremely low. Unique local IPv6 addresses are routable inside of a limited area, such as a site. Also, unique local IPv6 addresses may be routed between a limited set of sites (within an organization), but are not expected to be routable on the global internet.
--------
Which three commands should you use to configure data and voice VLAN on the same interface? (Choose three.)
* **Switch(config-if)# switchport access vlan 2**
* Switch(config-if)# switchport data vlan 2
* **Switch(config-if)# switchport mode access**
* Switch(config-if)# switchport mode trunk
* Switch(config-if)# switchport trunk allowed vlan 2,3
* **Switch(config-if)# switchport voice vlan 3**

	* Switch(config-if)# switchport access vlan 2
	* Switch(config-if)# switchport mode access
	* Switch(config-if)# switchport voice vlan 3
	-
	When connecting a host to a switch port, you can use the switchport access vlan vlan-id command to assign an interface to a VLAN. To simplify the troubleshooting process, IP phones are often placed into a "voice VLAN." Even though we create a separate logical segment, the port mode is not changed to trunk.
--------
What are the two main benefits of using spine-leaf architecture compared to traditional data center architectures, which use virtual Port Channel (vPC)? (Choose two.)
* It is cheaper to implement.
* **It is easier to scale.**
* **The oversubscription of links is reduced.**
* The configuration is simplified.
* The troubleshooting is simplified.

	* It is easier to scale
	* The oversubscription of links is reduced
	-
	Spine-leaf architecture solves the problem of link oversubscription that is present in traditional vPC architecture, where only two active parallel uplinks can be configured in a vPC. With full-mesh topology between spines and leaves, the bottleneck is eliminated, and the network is easier to scale. When more devices need to be connected, a new leaf is added. If link oversubscription occurs, a new spine is added. Spine-leaf topology is more complex and therefore harder to configure and troubleshoot.
--------
What is the Cisco best practice recommendation for port speed and duplex settings when using Fast Ethernet IEEE 802.3u-compliant devices?
* disable auto-negotiation on both sides of the link and manually configure full-duplex on both sides of the link
* disable auto-negotiation on both sides of the link and manually configure half-duplex on both sides of the link
* **enable auto-negotiation on both sides of the link**
* manually configure one side of the link with duplex and speed and enable auto-negotiation on the other side of the link

	enable auto-negotiation on both sides of the link
	-
	You can ensure that the link operates at full capacity by manually configuring it, but any change to the devices on either side of the link might result in a non-operational link.
--------
On Cisco routers, routing for IPv6 is not enabled by default. Which command should you use to enable IPv6 routing?
* ipv6 enable
* ipv6 local policy route-map
* ipv6 route <IPv6 address>
* **ipv6 unicast-routing**

	ipv6 unicast-routing
	-
	The ipv6 local policy route-map command is used to assign a route map for the local policy-based routing to the interface. The ipv6 route command configures an IPv6 static route. When the next hop is a link-local address, the outgoing interface must be specified. The ipv6 enable command enables IPv6 processing on an interface that has not been configured with an explicit IPv6 address.
--------
What is the purpose of the blocking state of ports in STP (Spanning Tree Protocol)?
* To prevent MITM (man-in-the-middle) attacks.
* To prevent retransmission of routing protocol updates.
* **To prevent path loops.**
* To prevent unauthorized usage of unused ports.

	* To prevent path loops.
	-
	STP forces certain ports into a blocking state, so that they do not listen to, forward, or flood data frames. The overall effect is that there is only one active path to each network segment at any time. STP is a protocol on Layer 2 of the OSI model, whereas routing protocol updates are used on Layer 3 of the OSI model. To prevent unauthorized use of ports, they must be disabled.
--------
Lab Work 1 begins:
------------------
Create EtherChannel links between the switches using the Link Aggregation Control Protocol (LACP).
Configure the switches so SW3 is the root switch for VLAN 20 and SW1 is the root switch for VLAN 10.
Ensure there is full connectivity within each VLAN (that is, you can successfully issue the ping command between PC1 and PC2, between SRV1 and SRV2, and between switches).

On SW4, which port is the STP root port for VLAN 20?
* Eth1/0
* Po14
* Po24
* **Po34**

	**Po34**
--------
Create EtherChannel links between the switches using the Link Aggregation Control Protocol (LACP).
Configure the switches so SW3 is the root switch for VLAN 20 and SW1 is the root switch for VLAN 10.
Ensure there is full connectivity within each VLAN (that is, you can successfully issue the ping command between PC1 and PC2, between SRV1 and SRV2, and between switches).

On SW2, when you see the summary information for aggregated link. What is the status code or flags of the port channel Po23?
* down (D)
* **Layer2 - In use (SU)**
* stand-alone (I)
* suspended (s)

	Layer2 - In use (SU)
	-
When you use the show etherchannel summary command, the SU Status code signifies that the aggregated channel is Layer 2 channel and that it is active.
--------
Create EtherChannel links between the switches using the Link Aggregation Control Protocol (LACP).
Configure the switches so SW3 is the root switch for VLAN 20 and SW1 is the root switch for VLAN 10.
Ensure there is full connectivity within each VLAN (that is, you can successfully issue the ping command between PC1 and PC2, between SRV1 and SRV2, and between switches).

Issue the ping command from PC1 to PC2. What is the path that packets traverse?
* **SW1 > SW3 > SW2**
* SW1 > SW3 > SW4 > SW2
* SW1 > SW4 > SW2
* SW1 > SW4 > SW3 > SW2

	SW1 > SW3 > SW2
	-
	This is the resulting path of VLAN 10 after STP calculations are performed, taking aggregated links into consideration.
--------
Create EtherChannel links between the switches using the Link Aggregation Control Protocol (LACP).
Configure the switches so SW3 is the root switch for VLAN 20 and SW1 is the root switch for VLAN 10.
Ensure there is full connectivity within each VLAN (that is, you can successfully issue the ping command between PC1 and PC2, between SRV1 and SRV2, and between switches).

Refer to the exhibit. The figure represents the topology resulting from STP calculations after configuring the Layer 2 EtherChannel. Which VLAN does the topology in the exhibit represent?
* VLAN 1
* VLAN 10
* **VLAN 20**
* VLAN 99


	VLAN 20
	-
	When you use the show spanning-tree command on a switch, the output displays STP information for each VLAN, including the STP root bridge election results and port designations.
Lab Work 1 ends:
------------------
--------
Which algorithm is used to calculate the optimal path to a given destination from data stored in a link-state database (LSDB)?
* Rivest, Shamir, and Adleman (RSA)
* Secure Hash Algorithm (SHA)
* **Shortest Path First (SPF)**
* Quicksort

	Shortest Path First (SPF)
	-
	SPF is a widely used algorithm in computer science for finding the optimal path through nodes in a network or, in this case, a network of routers. The RSA and SHA algorithms are used for secure data transmission. RSA is used for encryption and SHA is a hash function that ensures transmitted data integrity. Quicksort is an algorithm used for sorting an array of data.
--------
Which of the following is preferred when a Cisco router makes a decision about where to forward a packet to a given network?


* default routes


* **directly connected routes**


* routes offered by dynamic routing protocols


* statically configured routes

	Answer
	The correct answer is directly connected routes. Of all possible routes, directly connected ones have the lowest administrative distance (0). Statically configured routes have the administrative distance value of 1, and dynamic protocols have an administrative distance greater than 1.
----------
Which of the following is valid link-local IPv6 addresses?

* **fe80::1 (Ans)**
* ff80::1
* fe90::1
* feb1::1
* fea3::1
* fec3::1
-----------

**ios-sw01#show ip interface brief**
Interface              IP-Address      OK? Method Status                Protocol
GigabitEthernet0/0     unassigned      YES unset  up                    up
GigabitEthernet1/3     unassigned      YES unset  up                    up
Vlan75                 172.16.34.1     YES TFTP   up                    up
ios-sw01#
-----------

**show version**

Next, the show version command is very frequently used to not only view the Cisco IOS version but **also get data like the uptime of the device, the config register, and other details, depending on the platform**. (This virtual version of Cisco IOS does not have it, but you can often also get the serial number and BIA MAC of the device.)

**ios-sw01#show version**
Cisco IOS Software, vios_l2 Software (vios_l2-ADVENTERPRISEK9-M), Experimental Version 15.2(20200924:215240) [sweickge-sep24-2020-l2iol-release 135]
Copyright (c) 1986-2020 by Cisco Systems, Inc.
Compiled Tue 29-Sep-20 11:53 by sweickge

ROM: Bootstrap program is IOSv

ios-sw01 **uptime is 49 minutes**
System returned to ROM by reload
System image file is flash0:/vios_l2-adventerprisek9-m
Last reload reason: Unknown reason

**Configuration register is 0x101**

----------

One of the most important show commands is **show running-config**. Even though it does not give you any operational data, it will give you all the lines of configuration that are running on your network device. You can ignore the lines that begin with ! because that means those lines are commented out and are not lines of configuration.

Issue a show running-config on ios-sw01 and press the space bar key to view the configuration:

**ios-sw01#show running-config**
Building configuration...

Current configuration : 3920 bytes

hostname ios-sw01
!
boot-start-marker
boot-end-marker
!
!
no logging console
!
no aaa new-model
!

* If you are looking for a specific line, you can use the | include phrase after your command. Check the VTP config by modifying your command using show running-config | include vtp:

**ios-sw01#show run | include vtp**
vtp mode transparent
ios-sw01#

* Sometimes, you are only interested in a certain portion of the config but want more than one line. You can view a whole section by adding | section. Check the interface config by issuing the show run | section interface command:

**ios-sw01#show run | section interface**
interface GigabitEthernet0/0
 description Link to ios-sw02
 switchport trunk allowed vlan 75,125,135,150
 switchport trunk encapsulation dot1q
 switchport trunk native vlan 10
 switchport mode trunk
 negotiation auto
interface GigabitEthernet0/1
 description Link to ios-sw04
 switchport trunk allowed vlan 75,125,135,150
 switchport trunk encapsulation dot1q
 switchport trunk native vlan 10
 switchport mode trunk
 negotiation auto

 * One final trick is if you know you want to start at a certain line, but it is not necessarily a section. You can add | begin to a command to start scrolling at a certain line in the configuration. Issue the command show run | begin aaa to start at the AAA config, and you can keep scrolling past there.


**ios-sw01#show run | begin aaa**
no aaa new-model
!
!
!
!
!
vtp mode transparent
!
!
!
ip cef
no ipv6 cef
!
!
!
spanning-tree mode pvst
spanning-tree extend system-id
!
!
vlan 10
 name Native VLAN
!
vlan 75
 --More--

------------

