file:///Users/sajagana/Desktop/CCNA_2024/CCNA%20Labs/Cisco_CCNA_Lab_Guide_v200-301f.pdf

CCNA Sample Configs: https://www.flackbox.com/ccna-project-files


Section 2: Host-to-Host communications Model:

	The OSI reference model separates network tasks into seven layers, which are named and numbered.

	Layer 1: The physical layer defines electrical, mechanical, procedural, and functional specifications for activating, maintaining, and de-activating the physical link between devices. This layer deals with the electromagnetic representation of bits of data and their transmission. The physical layer specifications define line encoding, voltage levels, the timing of voltage changes, physical data rates, maximum transmission distances, physical connectors, and other attributes. This layer is the only layer implemented solely in hardware.

	Layer 2: The data link layer defines how data is formatted for transmission and controlled access to physical media. This layer typically includes error detection and correction to help ensure reliable data delivery. The data link layer involves network interface controller to network interface controller (NIC-to-NIC) communication within the same network or subnet. This layer uses a physical address, sometimes called a MAC address, to identify hosts on the local network.

	Layer 3: The network layer provides connectivity and path selection beyond the local segment, all the way from the source to the final destination. The network layer uses logical addressing to manage connectivity. In networking, the logical address is used to identify the sender and the recipient. The postal system is another common system that uses addressing to identify the sender and the recipient. Postal addresses follow the format that includes name, street name, and number, city, state, and country. Network logical addresses have a different format than postal addresses; they are determined by the network layer rules. Logical addressing helps ensure that a host has a unique address or that it can be uniquely identified in terms of network communication.

	Layer 4: The transport layer defines the segmenting and reassembling of data belonging to multiple individual communications, defines the flow control, and defines the mechanisms for reliable transport if required. The transport layer serves the upper layers, which in turn interface with many user applications. To distinguish between these application processes, the transport layer uses its own addressing. This addressing is valid locally, within one host, unlike addressing at the network layer. The transport services can be reliable or unreliable. The selection of the appropriate service depends on application requirements. For instance, the file transfer may be reliable to guarantee that the file arrives intact and whole. On the other hand, a missing pixel when watching a video might go unnoticed. In networking, this is called an unreliable service.

	Layer 5: The session layer establishes, manages, and terminates sessions between two communicating hosts to allow them to exchange data over a prolonged time period. The session layer is mainly concerned with issues that application processes may encounter and not with lower-layer connectivity issues. The sessions, also called dialogs, can determine whether to handle data in both directions simultaneously or only handle data flow in one direction at a time. It also takes care of checkpoints and recovery mechanisms. The session layer is explicitly implemented with applications that use remote procedure calls.

	Layer 6: The presentation layer helps ensure that data sent by the application layer of one system is "readable" by the application layer of another system. It achieves that by translating data into a standard format before transmission and converting it into a format known to the receiving application layer. It also provides special data processing that must be done before transmission. It may compress and decompress data to improve the throughput and may encrypt and decrypt data to improve security. Compression/decompression and encryption/decryption may also be done at lower layers.

	Layer 7: The application layer is the OSI layer that is closest to the user. It provides services to user applications that want to use the network. Services include email, file transfer, and terminal emulation. An example of a user application is the web browser. It does not reside at the application layer but uses protocols that operate at the application layer. Operating systems also use the application layer when performing tasks triggered by actions that typically do not involve communication over the network. Examples of such actions are opening a remotely located file with a text editor or importing a remotely located file into a spreadsheet. The application layer differs from other layers in that it does not provide services to any other OSI layer.


		Which layer in the OSI model provides path connectivity beyond the local segment? Ans: Network layer


TCP/IP Protocol Suite:

	Link layer: This layer is also known as the media access layer. It defines protocols used to interface the directly connected network. Tasks of the protocols at this layer are closely related to the characteristics of the physical medium and deal primarily with physical network details. The link layer is also referred to as a network interface, network access, or even data link layer. Because there are many different types of physical networks, there are many link layer protocols. An example of the TCP/IP link layer protocol is Ethernet. The link layer introduces physical addresses, sometimes called hardware addresses or MAC addresses, to identify devices sharing a particular physical network segment.

	Internet layer: This layer routes data from the source to the destination, provides a means to obtain information on reaching other networks and deals with reporting errors. The Internet layer provides logical addressing. Logical addressing helps ensure that a host is uniquely identified. An Internet layer logical address, called an IP address, is used to identify a host. This address is valid globally and aims at uniquely identifying the host. End devices, such as laptops, mobile phones, and servers are configured with a logical address before connecting to the network. IP protocols—namely, IPv4 and the newer version, IPv6—reside in this layer. This layer serves the upper transport layer and passes information to the Link layer.

	Transport layer: This layer is the core of the TCP/IP architecture and the Internet layer. It is placed between "data mover" protocols of the link and internet layers and software-oriented protocols of the application layer. There are two main protocols at this layer, TCP and UDP. These protocols serve many application-layer protocols. Transport services "prepare" application data for transfer over the network, follow the transfer process, and ensure that data from different applications is not mixed. To distinguish between the applications, the transport layer identifies each application with its own addressing. This addressing is valid locally, within one host, unlike addressing at the Internet layer, which is valid globally.

	Application layer: The functions of this layer mainly deal with user interaction. It supports user applications by providing protocols and services that let you actually use the network. It also supports network application programming interfaces (APIs) that allow programs to access the network services, regardless of the operating system that they are running on. This layer accommodates protocols such as HTTP, HTTPS, Domain Name System (DNS), FTP, Simple Mail Transfer Protocol (SMTP), Secure Shell (SSH), and many more. These protocols facilitate applications for web browsing, file transfer, names to IP addresses resolution, sending of emails, remote access to devices, and many other functions that network users perform.

		Which four statements about the lower three layers (Link, Internet, and Transport) of the TCP/IP protocol suite are true? (Choose four.) Ans:


			TCP/IP lower layer protocols were designed to make sure that bits are moved over wires or air.



			TCP/IP lower layer protocols were designed to make sure that data reaches the destination host, no matter where it is located.


			TCP/IP lower layer protocols were designed to make sure that data is adapted to the physical medium used, no matter how many different networks data must traverse.


			TCP/IP lower layer protocols were designed to make sure that each application gets its data and not that of the other application.


Peer-To-Peer Communications:

	The term peer means the equal of a person or object. By analogy, peer-to-peer communication means communication between equals. This concept is at the core of layered modeling of a communication process. Although a layer deals with layers directly above and below it in performing its functions, the data it creates is intended for the corresponding layer at the receiving host. The concept is also called the horizontal communication.


	Note:
		The term peer-to-peer is often used in computing to indicate an application architecture in which application tasks and workloads are equally distributed among peers. Contrary to peer-to-peer is client-server architectures in which tasks and workload are unequally divided.

		Data: general term for the PDU that is used at the application layer

		Segment: transport layer PDU

		Packet: internet layer PDU

		Frame: link layer PDU


		What is the PDU called at the internet layer? Ans: **packet**


Encapsulation and De-Encapsulation:

	Note:
		Encapsulation increases the size of the PDU. The added information is required for handling the PDU and is called overhead to distinguish it from user data.

The data is encapsulated as follows:

	1. The user data is sent from a user application to the application layer, where the application layer protocol adds its header. The PDU is now called data.

	2. The transport layer adds the transport layer header to the data. This header includes its own information, indicating which application layer protocol has sent the data. The new data unit is now called a segment. The segment will be further treated by the Internet layer, which is the next to process it.

	3. The Internet layer encapsulates the received segment and adds its own header to the data. The header and the previous data become a packet. The Internet layer adds the information used to send the encapsulated data from the source of the message across one or more networks to the final destination. The packet is then passed down to the Link layer.

	4. The link layer adds its own header and also a trailer to form a frame. The trailer is usually a data-dependent sequence, which is used to check for transmission errors. An example of such a sequence is a Frame Check Sequence (FCS.) The receiver will use it to detect errors. This layer also converts the frame to a physical signal and sends it across the network using physical media.


At the destination, each layer looks at the information in the header added by its counterpart layer at the source. Based on this information, each layer performs its functions and removes the header before passing it up the stack. This process is equivalent to unpacking a box. In networking, this process is called de-encapsulation.

The de-encapsulation process is like reading the address on a package to see if it is addressed to you and then, if you are the recipient, opening the package and removing the contents of the package.

The following is an example of how the destination device de-encapsulates a sequence of bits:

	1. The link layer reads the whole frame and looks at both the frame header and the trailer to check if the data has any errors. Typically, if an error is detected, the frame is discarded, and other layers may ask for the data to be retransmitted. If the data has no errors, the link layer reads and interprets the information in the frame header. The frame header contains information relevant for further processing, such as the type of encapsulated protocol. If the frame header information indicates that the frame should be passed to upper layers, the link layer strips the frame header and trailer and then passes the remaining data up to the Internet layer to the appropriate protocol.

	2. The internet layer examines the internet header in the packet received from the link layer. Based on the information it finds in the header, it decides either to process the packet at the same layer or to pass it up to the transport layer. Before the internet layer passes the message to the appropriate protocol on the transport layer, it first removes the packet header.

	3. The transport layer examines the segment header of the received segment. The information included in the segment header indicates which application layer protocol should receive the data. The transport layer strips the segment header from the segment and hands over data to the appropriate application layer protocol.

	4. The application layer protocol strips the data header. It uses the information in the header to process the data before passing it to the user application.

TCP/IP Stack vs OSI Reference Model:


	OSI Reference Model | TCP/IP Stack

	Application         | Application
	Presentation        | Application
	Session             | Application

	Transport           | Transport

	Network             | Internet

	Data Link           | Link
	Physical            | Link

	The layers of the TCP/IP stack correspond to the layers of the OSI model:

	The TCP/IP link layer corresponds to the OSI physical and data link layers and is concerned primarily with interfacing with network hardware and accessing the transmission media. Like layer 2 of the OSI model, the link layer of the TCP/IP model is concerned with hardware addresses.

	The TCP/IP internet layer aligns with the network layer of the OSI model and manages the addressing of and routing between network devices.

	The TCP/IP transport layer, like the OSI transport layer, provides the means for multiple host applications to access the network layer in a best-effort mode or through a reliable delivery mode.

	The TCP/IP application layer supports applications that communicate with the lower layers of the TCP/IP model and corresponds to the separate application, presentation, and session layers of the OSI model.


	1. Which of the TCP/IP layers would the ISO OSI session layer fit? Ans: Application Layer

	2. Which ISO OSI layer ensures that the application layer of the receiving system will be able to read the information that the application layer of another system has sent? Ans: presentation layer

	3. Which ISO OSI model layer or layers align to the TCP/IP model transport layer? Ans: transport

	4. To which ISO OSI model layer or layers does the TCP/IP model application layer correspond to? Ans: session, presentation, and application


	5. Which statement is false regarding the encapsulation process? Ans: Encapsulation is the process used by the sending device to remove one or more of the protocol headers.


	6. Which TCP/IP stack layer provides logical addressing? Ans: Internet

	7. Which ISO OSI layer defines services to segment the data? Ans: transport layer

	8. Which two statements about the layered model of communication are true? (Choose two.) 
		Ans: 1. Layer processes on a host logically communicate with the same layer processes on another host.
			2. Layering facilitates troubleshooting by making it possible to diagnose and narrow a cause to specific layers.


	9. Match the PDU with its description:
		Ans:

			a Link layer PDU : frame

			an Internet layer PDU: packet

			the general term for the PDU that is used at the application layer: data

			a Transport layer PDU: segment



Section 3: 

	Operating Cisco IOS Software:

		SOHO - Samll Office Home Office

		Cisco's IOS supports change and migration through integration in all evolving classes of network platforms. This includes routers, switches, and other devices that have an impact on an organization's internetwork. Cisco IOS is an operating system that implements and controls the logic and functions of many Cisco devices, and it enables companies to build a single, integrated information systems infrastructure.

Cisco IOS Software Features and Functions

	Cisco IOS Software delivers the following network features and functions:

		Support for basic and advanced networking functions and protocols

		Connectivity for high-speed traffic transmission

		Security for access control and prevention of unauthorized network use

		CLI-based and GUI-based access enabling users to execute configuration commands

		Scalability to allow adding hardware and software components

		Reliability to ensure dependable access to networked resources

Cisco IOS Software CLI Functions:
	
	The CLI is used to enter commands.

	Operations vary on different internetworking devices.

	Users type in or copy and paste entries in the console command modes.

	Command modes have distinctive prompts.

	Pressing Enter instructs the device to parse (translate) and execute the command.

	The two primary EXEC modes are user mode and privileged mode.


	1. Which two statements about the Cisco IOS Software CLI are true? (Choose two.)
		Ans: 1. You can easily tell which command mode you are in because each mode has a distinctive prompt.
			2. When you finish typing in a command, you have to press Enter to execute it.

Cisco IOS Software Modes:

	Cisco IOS Software has various modes that are hierarchically structured. The highest hierarchy is the user EXEC mode. It is followed by the privileged EXEC mode. From the privileged EXEC mode, you can proceed to the global configuration mode and from there to more specific configuration modes such as interface configuration mode and router configuration mode, as shown below.

	1. User EXEC Mode => Switch> => Enter logout, exit, or quit.

	2. Privileged EXEC Mode => Switch# (While in user EXEC mode, enter the enable command.) => Enter disable or exit.

	3. Global Configuration Mode => Switch(config)# (While in privileged EXEC mode, enter the configure terminal command.) => To return to Privileged EXEC Mode, enter exit or end, or press Ctrl-Z.

	4. Interface Configuration Mode => Switch(config-if)# (While in global configuration mode, enter the interface command followed by interface label of the interface you wish to configure.) => To return to the Global Configuration Mode, type exit. Then to return to the Privileged EXEC mode, press Ctrl-Z or type exit or end.

	2. Which statement about the CLI operation modes is correct?
		Ans: To change from the Privileged EXEC Mode to the Interface Configuration Mode, you have to type the configure terminal command first and then type the interface command.


	3. While configuring a router, the network engineer typed the following sequence:

	R1# show ip access-list
	R1# show ip interface brief
	R1# configure terminal
	R1(config)# interface GigabitEthernet 0/2
	R1(config-if)# description Protected Access
	R1(config-if)# end
	R1#
	The engineer is using the terminal history help feature to recall previously used commands. The engineer used the Up Arrow key twice. Which command from the sequence did the engineer recall?

		Ans: show ip interface brief

	4. What is the expected result of the show running-config | exclude ! command executed on the Cisco IOS device?

		Ans: CLI will display the running configuration file but without any lines containing “!” in them

	5. In Cisco IOS Software, what are the two EXEC access levels? (Choose two.)
		Ans: user EXEC and privileged EXEC

	6. Which Cisco IOS command do you use to change from User EXEC Mode into Privileged EXEC Mode?
		Ans: enable

	7. Which three of the following commands can be used to exit the User EXEC Mode in a Cisco CLI session? (Choose three.)
		Ans: exit, quit, logout

	8. Which option is available to a network engineer to interact with a network device?
		Ans: A shell program exposes operating system services and can be accessed via CLI or GUI.

	9. How does the Privileged EXEC Mode restrict the access to the configuration CLI commands?
		Ans: Access to the Privileged EXEC Mode can be password protected to allow only authorized users to execute the privileged set of commands

-----------

Take notes:

Which **four of the following are valid link-local IPv6 addresses?** (Choose four.)
*** fe80::1**
* ff80::1
*** fe90::1**
*** feb1::1**
*** fea3::1**
* fec3::1

	* fe80::1
	* fe90::1
	* feb1::1
	* fea3::1
	-
	All addresses encompassed by the fe80::/10 prefix are considered valid link-local IPv6 addresses. The ff00::/8 prefix is the prefix of multicast IPv6 addresses. Addresses starting with the hexadecimal digits fec3 do not belong to a link-local IPv6 address range.
--------

Which APIs are used for communication between a **software-defined networking (SDN) application and a controller**?
* Eastbound APIs
*** Northbound APIs**
* Southbound APIs
* Westbound APIs

	**Northbound APIs**
	-
	Northbound APIs or northbound interfaces are responsible for the communication between the SDN controller and the services that run over the network. Northbound APIs enable your applications to manage and control the network. Therefore, rather than adjusting and tweaking your network repeatedly to get a service or application running correctly, you can set up a framework that allows the application to demand the network setup that it needs.
----------

Refer to the exhibit. Which two options are common **IPsec or SSL VPN** implementations? (Choose two.)

* **option 1**
* option 2
* option 3
* option 4
* **option 5**

Answer
The correct answers are option 1 and option 5. An IPsec Tunnel VPN is typically established between two network devices, connecting two or more remote networks. An SSL VPN is typically established between a client and a network device. DMVPN and IPsec VTI VPN are typically established between network devices.

--------
What are **two valid IPv6 address scopes for a unique local IPv6 address?** (Choose two.)
* global
* interface-local
* link-local
* **organization-local**
* **site-local**

Answer
The correct answers are **organization-local and site-local.** **Unique local IPv6 addresses are equivalents of private IPv4 addresses.** They can be considered globally unique, because the probability of duplication is extremely low. Unique local IPv6 addresses are routable inside of a limited area, such as a site. Also, unique local IPv6 addresses may be routed between a limited set of sites (within an organization), but are not expected to be routable on the global internet.
---------
When a **particular VLAN is deleted, what happens to interfaces that were assigned to the deleted VLAN?**

The correct answer is **They become inactive.**
-----------
When an enterprise has to comply with **strict data security regulations, which cloud deployment model should they use for their services?**

The correct answer is **private**.
-----------
Which command is used to **verify a default gateway configuration on a Layer 2 switch**?

The correct answers is **show running-config**
------
On SW2, verify the administrative and operational switching modes on interface Ethernet0/3. Which statement correctly describes the administrative mode and operational mode values?

* Administrative mode is access and operational mode is access.
* Administrative mode is dynamic-auto and operational mode is access.
* Administrative mode is dynamic-desirable and operational mode is access.
* **Administrative mode is dynamic-desirable and operational mode is trunk.**
* Administrative mode is trunk and operational mode is trunk.

Answer
The correct answer is **Administrative mode is dynamic-desirable and operational mode is trunk**. Administrative mode displays what you have configured on the interface. Operational mode displays the actual status of the interface. **When manually configuring access or trunking, administrative and operational mode have identical values.**

--------

Which three statements about IPv4 addresses are true? (Choose three.)
* **8.0.0.0 is a public address.**
* **10.8.0.0 is a private address.**
* **127.0.0.1 is a reserved address.**

Answer
The correct answers are 8.0.0.0 is a public address, 10.8.0.0 is a private address, and 127.0.0.1 is a reserved address. 192.170.0.0 is a public IPv4 address, and 172.30.0.0 is a private IPv4 address.

------
When **creating and maintaining the MAC address table, which two activities does a switch perform**? (Choose two.)
* **It adds the source MAC address in the frame and the incoming port number**
* **It resets the aging time of the MAC table entry for the source MAC address**

Answer
The correct answers are **It adds the source MAC address in the frame and the incoming port number and It resets the aging time of the MAC table entry for the source MAC address**. A switch uses the destination MAC address to decide whether to forward or flood a frame. The destination MAC address is not stored in the MAC address table. The aging timer is reset for the source MAC address entry each time the switch receives a frame from that source MAC address.
-------
When a **router is calculating the network portion of an IPv4 address**, which bitwise operation is performed on the IPv4 address and the subnet mask?

Ans: **AND** operation
--------
When an **access port is enabled with the PortFast feature,** which two STP states are bypassed? (Choose two.)

Ans: **learning and listening**
---------------
**If a port is still a designated or root port at the end of the learning state**, which state will it enter?
* blocking
* disabled
* **forwarding**
* learning
* listening

	forwarding
	-
	**This port sends and receives all data frames on the bridged port**. A blocked port only listens to BPDUs (Bridge Protocol Data Units), and it does not forward any frames. Disabled ports do not participate in frame forwarding. A port changes to a learning state after a listening state. After a blocking state, the designated port moves to a listening state.
-----------
Lab with EthernetChannel:

**Q1**. On SW4, which port is the STP root port for VLAN 20?

Answer
The correct answer is **Po34**. SW3 is the root bridge for VLAN 20. SW4 is connected to SW3 via aggregated links represented by interfaces Po14, Po24, and Po34. After verifying the STP status for VLAN 20, you can see that the Po34 interface has the shortest path, hence the lowest cost and is elected as the root port.

**Q2**. On **SW2, when you see the summary information for aggregated link**. What is the status code or flags of the port channel Po23?

Answer
The correct answer is **Layer2 - In use (SU)**. When you use the show etherchannel summary command, the SU Status code signifies that the aggregated channel is Layer 2 channel and that it is active.

**Q3**. Issue the **ping command from PC1 to PC2.** What is the path that packets traverse?

Answer
The correct answer is **SW1 > SW3 > SW2**. This is the resulting path of VLAN 10 after STP calculations are performed, taking aggregated links into consideration.

**Q4**. Refer to the exhibit. The figure represents the topology resulting from **STP calculations after configuring the Layer 2 EtherChannel. Which VLAN does the topology in the exhibit represent?**

Answer
The correct answer is **VLAN 20**. When you use the show spanning-tree command on a switch, the output displays STP information for each VLAN, including the STP root bridge election results and port designations.

---------
Character - Description
! - Each exclamation point indicates receipt of a reply. **(Ping successfully passed)**
. - Each period indicates the network server timed out while waiting for a reply. **(Ping failed)**
U - A destination unreachable error PDU was received. **(Ping failed)**
C - A congestion experienced packet was received.
I - User interrupted test. **(Ping failed)**
? - Unknown packet type. **(Ping failed)**
& - Packet lifetime exceeded. **(Ping failed)**
--------
Level Keyword => Level => Description => Syslog Definition
**emergencies** => **0** => System unstable => **LOG_EMERG**
**alerts** => **1** => Immediate action needed => **LOG_ALERT**
**critical** => **2** => Critical conditions => **LOG_CRIT**
**errors** => **3** => Error conditions => **LOG_ERR**
**warnings** => **4** => Warning conditions => **LOG_WARNING**
**notifications** => **5** => Normal but significant condition => **LOG_NOTICE**
**informational** => **6** => Informational messages only => **LOG_INFO**
**debugging** => **7** => Debugging messages => **LOG_DEBUG**
--------
Which task controls the **download and deployment of software updates**?
* compliance checks
* data collection and telemetry
* device provisioning
* **device software management**

	device software management
	-
	Controlling the download and deployment of software updates is a relatively simple task, but it can be time-consuming, and may be subject to human error. Many automated tools have been created to address this issue, but they can lag behind customer requirements. A simple network programmability solution for device software management is beneficial in many environments.
--------

What is the maximum **cable length of an unshielded twisted-pair (UTP)** cable that still guarantees full connectivity?
* 80 m
* **100 m**
* 120 m
* 150 m

---------
Which component is used to generate a **signal for single-mode fiber** connections?
* cathode
* **laser transmitter**
* LED diode
* oscillator

	**laser transmitter**
----------
**On a Cisco switch, which two commands would you use to identify ports that are configured as trunks?** (Choose two.)

The correct answers are **show interfaces status** and **show interfaces trunk**
--------
Which **two commands display the type of trunking encapsulation** of an interface? (Choose two.) **It may be related to Router**

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
On a Cisco switch, **which two commands display the VLANs allowed on trunk interfaces**? (Choose two.)
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
What is the administrative distance of OSPF?
* 90
* **110**
* 170
* 200

	110
	-
	Internal EIGRP routes have the administrative distance value of 90, external EIGRP routes have 170 and internal BGP routes have an administrative distance of 200.
--------
After the Cisco IOS Software image is loaded and started, from which three components can the device load its configuration? (Choose three.)
* DHCP server
* DNS server
* RAM
* **NVRAM**
* **SCP server**
* **TFTP server**
--------

Which three types of booting are supported on servers? (Choose three.)

* **booting from internal storage**
* **booting from LAN**
* **booting from SAN**
* booting from WAN
* booting from wireless

-------
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
Which task makes **configuring network devices more efficient and reduces errors?**

* compliance checks
* data collection and telemetry
* **device provisioning**
* device software management

	device provisioning
---------

Which two characteristics apply to **small office/home office (SOHO) routers**? (Choose two.)

* They are more expensive than enterprise routers.
* They are more reliable than enterprise routers.
* **They have a web-based administration interface.**
* **They have integrated security functionality.**
* They perform intensive routing tasks.

----------

What is the default gateway that PC1 has received through DHCP?

* 10.10.1.1
* **10.10.1.53**
* 10.10.1.100
* 10.10.1.254

	Answer
	The correct answer is **10.10.1.53**. In real networks, **the gateway address is usually either the first or the last assignable IP address of the subnet.**
---------
Which three fields are included in a TCP header? (Choose three.)

* destination address
* **destination port**
* **flags**
* frame check sequence
* **window size**

----------
Which group of devices in a network receive IPv6 packets with the destination address of **ff05::2**?

* all IPv6 nodes on all the network segments within a site
* all IPv6 nodes on the local network segments
* **all IPv6 routers on all the network segments within a site**
* all IPv6 routers on the local network segments
* all OSPFv3 routers on all the network segments within a site
* all OSPFv3 routers on the local network segments

	Answer
	The correct answer is **all IPv6 routers on all the network segments within a site**. The hexadecimal digits **“ff”** in the IPv6 address **prefix are an indication of a multicast address.** The **fourth hexadecimal digit indicates the scope**, with the number **five representing a site-local scope**. The **group ID of ::2 represents all IPv6 routers**.
----------
**IPv6 Multicast Addresses:**
The IPv6 multicast address range starts with the prefix FF00::/8. Similar to IPv4, certain addresses within this range are reserved for specific functions. For example:

- **FF02::1**: All nodes address, **which targets all devices on the local network segment**
- **FF02::2**: All routers address, **which targets all routers on the local network segment**
--------

An enterprise wants to provide a global service that would be provided from an enterprise resource nearest to the user. For which three reasons does the **enterprise choose to assign anycast IPv6 addresses** to the relevant devices? (Choose three.)

* Because all the devices configured with the IPv6 anycast address would be aware of the user session.

* **Because IPv6 anycast addresses are globally routable.**

* Because routing of IPv6 anycast addresses is more secure than routing other IPv6 address types.

* **Because routing tables will point to the nearest resource configured with the IPv6 anycast address.**

* **Because using IPv6 anycast addresses provides automatic failover.**

--------

In the Wi-Fi 2.4 GHz band, which three channels do not overlap? (Choose three.)


* 0

* **1**

* 2

* **6**

* **11**

* 15

* 21
----------
Which command is used to **verify a default gateway** configuration on a Layer 2 switch?

* **show interface description**

* show interface stats

* show ip default-gateway network

* show management

* **show running-config**
----------
On SW2, verify the administrative and operational switching modes on interface Ethernet0/3. Which statement correctly describes the administrative mode and operational mode values?

* Administrative mode is access and operational mode is access.

* Administrative mode is dynamic-auto and operational mode is access.

* Administrative mode is dynamic-desirable and operational mode is access.

* **Administrative mode is dynamic-desirable and operational mode is trunk.**

* Administrative mode is trunk and operational mode is trunk.

	Answer
	The correct answer is **Administrative mode is dynamic-desirable and operational mode is trunk**. Administrative mode displays what you have configured on the interface. Operational mode displays the actual status of the interface. **When manually configuring access or trunking, administrative and operational mode have identical values.** When you configure Dynamic Trunking Protocol (DTP) to negotiate switching status, administrative and operational mode differ. Cisco recommends disabling DTP on a switch."
---------
Which three IPv4 addresses are private? (Choose three.)

* **10.255.255.254**

* **172.31.255.254**

* 172.32.255.254

* **192.168.1.100**

* 192.169.1.100

	Answer
	The correct answers are **10.255.255.254, 172.31.255.254, and 192.168.1.100**. These ranges of IP addresses are **private: 10.0.0.0 to 10.255.255.255, 172.16.0.0 to 172.31.255.255, and 192.168.0.0 to 192.168.255.255**. Addresses in these ranges are not routed on the internet backbone.
--------
Which type of Cisco **switch memory location stores the MAC address table**?

* **content-addressable memory (CAM) (Ans)**

* flash

* non-volatile random-access memory (NVRAM)

* read-only memory (ROM)
---------
Which two symptoms indicate a **duplex mismatch between a client and an Ethernet switch**? (Choose two.)

* Auto-negotiation will report speed and duplex mismatch errors on the client NIC interface.

* Interface statistics for the full-duplex side of the link will show increasing late collision errors.

* **The full-duplex interface will report increasing numbers of FCS errors or runts on the port**.

* The full-duplex side of the link will slow as CSMA/CD will force it to wait for incoming packets from the other side of the link.

* **The half-duplex side of the link will waste bandwidth due to increased packet retransmissions caused by increasing collisions**.
-------

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
Which statement regarding **online and offline password attacks is true**?

* **Offline attacks are more dangerous because there is no external authentication system.**

* Offline attacks are more dangerous because they target out-of-band management assets.

* Online attacks are more dangerous because distributed sources can deliver them.

* Online attacks are more dangerous because they can target resources connected on the network.
----------
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
	The correct answer is 1. This port exists on non-root bridges. **Only one root port is allowed per switch or per VLAN in Cisco PVST+**. The root port forwards traffic toward the root bridge.
--------

Which line in the preconfigured access list 10 on router R1 will cause the ping connectivity test from PC1 to SRV2 (203.0.113.30) to fail?

* access-list 10 deny 10.0.0.0 0.255.255.255

* **access-list 10 deny 10.10.1.0 0.0.0.255 (Ans)** Note: ACL uses Wildcard masks that is opposite of the IP.

* access-list 10 deny any

* implicit deny

--------
Which Cisco IOS command displays the sequence numbers of the statements in the access list?

* show ip access-group

* **show ip access-lists (Ans)**

* show running-config

* show running-config all
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
--------
Which two Microsoft Windows commands will display the **DNS server address configured** on the host? (Choose two.)

* ipconfig

* **ipconfig /all**

* net config

* netstat -f

* **nslookup**
--------
A client issues a DNS request to its local DNS server. The local DNS server does not have the information required. Which entity will finally send a DNS response to the client?

* the authoritative DNS server for the top-level domain

* the authoritative top-level domain and subdomain DNS servers

* **the client's local DNS server**

* the Internet Service Provider's DNS server

	Answer
	The correct answer is **the client's local DNS server**. When the local DNS server cannot find the queried domain in its database, which indicates that the **local server is not authoritative for this domain, it will query the authoritative root DNS server for the top-level (root) domain**. The root DNS server directs the query to the DNS server for the first subdomain of the queried domain name. The query directing process continues until the local server reaches the authoritative subdomain DNS server. **The authoritative subdomain DNS server resolves the initially queried domain name and replies to the local DNS server. This is how the local DNS server gets the resolved IP address. It is then the local DNS who sends the response to the client.**
--------
For which network entity is the **OSPF designated router/backup designated router (DR/BDR) selection performed?**

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
---------
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
-----------
On R1, at the command prompt, issue the exit command as many times as necessary until you get the "Press RETURN to get started" prompt. Which password do you have to type to access the USER exec mode?

* Cisco123!

* Cisco333!

* CiscoR1!

* **password is not required**

Answer
The correct answer is password is not required. **When accessing the USER exec mode, no password is required.**
---------
Which number represents the **default encryption type of the protected password** used to restrict access to the **privileged EXEC mode**?

* **4**

* 5

* 8

* 9
---------

Examine the Device Access table in the Job Aid. There are four users configured on SW2. The SW2 switch console line access is set to privilege level 5. Presuming command **privileges are set to default, which username should you use to be able to change the SW2 configuration**?

* admin

* monitor

* operator

* **superadmin**

	Answer
	The correct answer is superadmin. By default, Cisco IOS configuration commands require the maximum privilege level, which is 15. This is the privilege level of the user superadmin.
----------


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

--------

Which three of the following application characteristic values are determined in the **service level specification** phase **when designing the quality of service (QoS)** policy of a network? (Choose three.)

* generated data flows

* **required bandwidth**

* required responsiveness

* response criticality

* **tolerable jitter**

* **tolerable packet loss**
---------
Which statement regarding a **small office/home office (SOHO)** of a remote worker is correct?

* **It is a LAN that includes both wireless and wired network devices.**

* It must be permanently connected to the main office.

* It must follow the three-tier architecture model.

* It typically uses dark fiber to connect to the main office.

-------
What is the network ID of the IPv6 address 2001:db8:deca:abce:45eb:27ff:feba:fa38/48?

* 2001::

* 2001:db8::

* **2001:db8:deca::**

* 2001:db8:deca:abce::

	Answer
	The correct answer is 2001:db8:deca::. **Each hexadecimal character represents 4 binary bits**. **The first 12 characters correspond to 48 bits.** 2001:db8:deca:abce:: would have the /64 prefix, 2001:db8:: would have the /32 prefix, and 2001: would have the /16 prefix.
----------
From PC2, use SSH to access R1. Use AdminPC2 as the username and Cisco123 as the password. **What is the IPv4 address of the loopback interface?**

* 10.10.2.1

* **10.10.3.1**

* 10.10.4.1

* 10.10.5.1

	Answer
	The correct answer is 10.10.3.1. If you issue the **show ip interface brief** command, you will see that there are two interfaces configured. Ethernet0/0 has the IPv4 address 10.10.1.1 and the **loopback0 interface has the IPv4 address 10.10.3.1.**
--------
How are NETCONF messages encoded?

* by using CSS

* by using JSON

* by using SQL

* **by using XML**
---------
Which two statements about the **Dynamic Multipoint Virtual Private Network (DMVPN)** are true? (Choose two.)

* **DMVPN creates hub-to-spoke tunnels.**

* **DMVPN creates spoke-to-spoke tunnels.**

* DMVPN is used for connection between an enterprise and a provider.

* DMVPN is used for connection between enterprises.

* DMVPN is used within a branch network.
---------

Which three protocols use **UDP**? (Choose three.)

* **DHCP**

* FTP

* HTTPS

* **SNMP**

* **TFTP**
----------

Which **IPv6 network prefix is only intended for local links and cannot be routed**?

* ::ffff/80

* 2001::/3

* fc00::/7

* **fe80::/10 (Ans)**
----------

What are two characteristics of an **anycast IPv6 address**? (Choose two.)

* It can be assigned to a host (end-user devices).

* **It can be assigned to multiple nodes.**

* It can be recognized by a pre-defined prefix.

* It is used in an IPv6 packet as a source IPv6 address.

* **It is assigned from the unicast IPv6 address space.**
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
-----------
Which of the following network devices defines a **broadcast domain and a collision domain on every one of its ports**?

* bridge

* hub

* **router**

* switch
--------

What are the two main **WLAN deployment types**? (Choose two.)

* **centralized (Ans)**

* router-based

* **standalone (Ans)**

* Wi-Fi Direct

* Zero Touch Provisioning (ZTP)
-------
Which **cloud service model offers customers the most control over their cloud-hosted services?**

* Function as a Service (FaaS)

* **Infrastructure as a Service (IaaS) (Ans)**

* Platform as a Service (PaaS)

* Software as a Service (SaaS)
--------
Which three layers does the hierarchical three-tier model include? (Choose three.)

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
-----------
Which three statements about **IPv4 addresses** are true? (Choose three.)

* **8.0.0.0 is a public address.**

* **10.8.0.0 is a private address.**

* **127.0.0.1 is a reserved address.**

* 172.30.0.0 is a public address.

* 192.170.0.0 is a private address.
--------
When the **store-and-forward switching method is in use, which part of the Ethernet frame is used to perform error checking using cyclic redundancy check (CRC)?**

* **All frame fields, except the FCS field in the trailer.**

* The destination MAC address in the header, and the FCS field in the trailer.

* The frame check sequence (FCS) field in the trailer.

* The source MAC address in the header, and the FCS field in the trailer.
---------
After receiving an Ethernet frame, a switch examines the destination MAC address, and forwards the frame out of all ports except the incoming port. In which communication types can this behavior occur?

* in broadcast and multicast communication

* in broadcast communication

* **in broadcast, multicast, and unicast communication**
--------

Which command would you use to configure a **floating static route?**

* ip route static 192.168.13.0 255.255.255.0 100

* **ip route 192.168.13.0 255.255.255.0 172.17.10.1 100**

* ip route 192.168.13.0 255.255.255.0 172.17.10.1

* ip route 192.168.13.0 255.255.255.0 172.17.10.1 metric 100
--------
For an administrator to be able to access the Layer 2 switch S1 from the internet, which IP connectivity parameters do you have to configure on the S1 switch?

* **default gateway to 192.168.3.254**

* default route via 192.168.3.254

* IPv4 address in the 209.168.200.224/27 subnet

* static route to 209.168.200.254/27

	Answer
	The correct answer is default gateway to 192.168.3.254. For **Switch S1 to be able to replay and respond as the administrator manages it, it must have a default gateway set.** On a Layer 2 switch, you cannot configure routes, since IP routing is not enabled. For the switch virtual interface to work, the VLAN must be associated and active on at least one physical port.
--------
Two computers are connected to a Cisco Catalyst Layer 2 switch. PC1 is assigned the address 10.250.20.20/26 and PC2 is assigned the address 10.250.20.50/26. When a user on PC1 issues the ping 10.250.20.63 command, will PC2 respond to it?

* No, because 10.250.20.63 is not in the subnet that PC1 belongs to.

* No, because 10.250.20.63 is not the IP of PC2.

* **Yes, the PC2 will respond to the 10.250.20.63 broadcast if both ports are operationally in access mode and the same VLAN**

* Yes, if the ip routing command is configured on the switch.
---------
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

Which **three SNMP messages are sent from an SNMP agent to an SNMP manager**? (Choose three.)

* GetRequest

* GetNextRequest

* **InformRequest**

* **Response**

* SetRequest

* **Trap**
--------
Which command would you use to **verify the number of excluded addresses on a router configured as a DHCP server**?

* show ip dhcp bindings

* show ip dhcp conflict

* show ip dhcp database

* **show ip dhcp pool (Ans)**
--------
When using **Hot Standby Router Protocol (HSRP) for gateway redundancy**, which address is used for the gateway on hosts?

* active

* active and standby

* standby

* **virtual**
--------
Where does a router that runs OSPFv2, and that has neighbor adjacencies established, store link-state advertisements (LSAs)?

* **LSDB**

* Neighbors table

* Routing table

* SPF tree
--------
Where does a router that runs **OSPFv2**, and that has neighbor adjacencies established, **store link-state advertisements** (LSAs)?

* **LSDB**

* Neighbors table

* Routing table

* SPF tree
--------
Which **algorithm is used to calculate the optimal path** to a given destination from data stored in a link-state database (LSDB)?

* Rivest, Shamir, and Adleman (RSA)

* Secure Hash Algorithm (SHA)

* **Shortest Path First (SPF)**

* Quicksort
-------
What does the term **per-hop behavior (PHB)** signify?

* a set of node requirements for compliance with the DiffServ model

* a set of packet markings applied to different classes of traffic

* **a set of techniques for traffic shaping (Ans)**

* a set of traffic classes defined in the network
--------
On a router that does not have a default route in the routing table, you issue the following two commands:

Router(config)# ip route 0.0.0.0 0.0.0.0 10.10.10.10 20
Router(config)# ip route 0.0.0.0 0.0.0.0 10.20.250.2 10
What is the result of executing the commands?

* Both routes are installed in the routing table as default routes.

* The route pointing to the IPv4 address 10.10.10.10 is installed as the default route.

* **The route pointing to the IPv4 address 10.20.250.2 is installed as the default route.**

* There are no changes to the routing table.
-----------
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
----------

In the Cisco Software-Defined Access solution, which three network elements are used to build the underlay network? (Choose three.)

* Cisco DNA Center

* Cisco Identity Services Engine

* **Cisco routers (Ans)**

* **Cisco switches (Ans)**

* **Cisco Wireless LAN Controllers (Ans)**
----------
Which three characteristics apply to the 802.1Q protocol? (Choose three.)

* **It carries untagged frames.**

* **It modifies the 802.3 frame header.**

* It includes an 8-bit field for TTL (Time to Live).

* It is a messaging protocol that carries a VLAN configuration.

* **It uses an internal tagging mechanism.**
--------
Which of the following **network devices defines a broadcast domain and a collision domain on every one of its ports**?

* bridge

* hub

* **router**

* switch
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
In an enterprise environment, which guideline should be **implemented to manage passwords securely, and why**?

* A centralized password repository should be avoided, because it is a single point of failure.

* A local password repository should be used, because it is more secure, and there is no need to transmit passwords using a AAA protocol.

* **Access to passwords should be logged along with the user information, in order to have visibility of password usage. (Ans)**

* Passwords should NOT be used, because digital certificates are more secure and scale better.
--------
Which command is used to assign IPv6 addresses to PC1 and PC2?

* ipv6 address autoconfig
* **ipv6 address autoconfig default**
* ipv6 address dhcp
* ipv6 address 2001:db8:0:1::/64 eui-64 on PC1 and ipv6 address 2001:db8:0:2::/64 eui-64 on PC2
--------
What is the purpose of the Cisco Wireless LAN Controller (WLC)?

* ensuring that firewall rules are enforced on wireless networks
* **managing multiple wireless access points (APs)**
* providing a wireless signal to end points
* routing traffic between wireless networks
--------
When configuring an IPv4 static route pointing to the **next-hop IPv4**, which command should you use?

* **ip route 172.16.1.0 255.255.255.0 172.16.2.1**
* ip route 172.16.1.0 net-mask 255.255.255.0 next-hop 172.16.2.1
* ip route 172.16.1.0/24 172.16.2.1
* ip route static 172.16.1.0 net-mask 255.255.255.0 next-hop 172.16.2.1
--------
Which type of address is **automatically assigned to a physical interface when IPv6 is enabled on that interface**?
* global unicast address
* **link-local address**
* loopback address
* unique local address
--------
Which three operations can an **SNMP manager process perform in a network**? (Choose three.)
authenticate users accessing a device
* **configure a device**
* construct a management information base (MIB) on a device
* **retrieve data about the license of the device**
* **retrieve data about the environmental parameters of a device**
--------
When **determining the OSPF router ID, what is the last action that the router will perform**?
* Choosing the highest IPv4 address on a loopback interface.
* **Choosing the highest IPv4 address on an active interface.**
* Choosing the lowest IPv4 address on a loopback interface.
* Choosing the lowest IPv4 address on an active interface.

--------
Which series of phases correctly represents a common attack methodology?
* **Initial Compromise > Escalation of Privileges > Reconnaissance of internal hosts > Lateral movement > Exfiltration**
* Lateral movement > Escalation of Privileges > Reconnaissance of internal hosts > Initial Compromise > Exfiltration
* Lateral movement > Reconnaissance of internal hosts > Escalation of Privileges > Initial Compromise > Exfiltration
* Reconnaissance of internal hosts > Escalation of Privileges > Initial Compromise > Lateral movement > Exfiltration

--------
For a router, which of the following is the **preferred source of information about a destination network**?

* **an active local interface connected to the network**
* Enhanced Interior Gateway Routing Protocol (EIGRP)
* Open Shortest Path First (OSPF)
* the ip route configuration command
------------
What is the **administrative distance for the Enhanced Interior Gateway Routing Protocol (EIGRP)**?

* 50
* 60
* 70
* **90**
--------
Which three statements are **characteristics of the Enterprise mode of Wi-Fi Protected Access**? (Choose three.)

* A shared secret is used for authentication.
* **Access control is centralized.**
* Access control is local.
* **Advanced Encryption Standard (AES) is optional for encryption.**
* **The authentication server is used for key distribution.**
---------
You have set up a small office/home office (SOHO) to work from home. You are using broadband internet with a remote-access Virtual Private Network (VPN) to connect to your company resources. Which statement correctly describes this deployment mode?

* A VPN-capable router is required for the SOHO network.
* **You can use the web browser to establish a VPN tunnel.**
* A permanent VPN connection is required.
* VPN tunneling is performed by the internet service provider (ISP).
----------
When an access point (AP) is operating in local mode, on which network device is wireless client traffic switched?

* on a network switch
* **on a wireless access controller (WLC)**
* on the egress AP
* on the ingress AP
--------
In which network implementations is the spine-leaf topology most commonly used?

* enterprise LAN
* enterprise edge
* **data centers**
* ISP backbone
---------

When creating and maintaining the MAC address table, which two activities does a switch perform? (Choose two.)

* It adds the destination MAC address in the frame and the incoming port number.
* It adds the destination MAC address in the frame and the outgoing port number.
* **It adds the source MAC address in the frame and the incoming port number.**
* It resets the aging timer of all the entries related to the incoming port.
* **It resets the aging time of the MAC table entry for the source MAC address.**
-----------

What is the IP address of the R2 interface connecting to R1?

* 10.10.1.3

* 192.168.3.1

* **192.168.3.2 (Ans)**

* 192.168.3.3

Answer
The correct answer is **192.168.3.2**. By issuing the **show cdp neighbors detail** command on R1, you are able to get the IPv4 address of R2’s interface connecting to R1.
-------
Two routers, A and B, are part of the Hot Standby Router Protocol (HSRP) standby group. There was no priority configured, and router A with the highest IP address for this HSRP group. Which statement is correct?
* Router A will be in the ACTIVE state and router B will be in the ACTIVE state.
* **Router A will be in the ACTIVE state and router B will be in the STANDBY state.**
* Router A will be in the LISTEN state and router B will be in the STANDBY state
* Router A will be in the STANDBY state and router B will be in the STANDBY state.
----------
Where in the network should you implement QoS packet classification?
* **at the input interface of a device at the LAN access edge of the network**
* at the input interface of a device at the WAN edge of the network
* at the output interface of a device at the LAN access edge of the network
* at the output interface of a device at the WAN edge of the network
------------

**Router#show ip route**
Codes:
L - local
C - connected
S - static
R - RIP
M - mobile
B - BGP
D - EIGRP
EX - EIGRP external
O - OSPF
IA - OSPF inter area
N1 - OSPF NSSA external type 1
N2 - OSPF NSSA external type 2
E1 - OSPF external type 1
E2 - OSPF external type 2
E - EGP
i - IS-IS
L1 - IS-IS level-1
L2 - IS-IS level-2
ia - IS-IS inter area
`* - candidate default`
U - per-user static route
o - ODR
P - periodic downloaded static route

Gateway of last resort is not set
-----------
What is the result of running the following sequence of commands on a router running OSPF as its routing protocol?

**Sample OSPF Point-to-Point configuration:**
   config t
   Interface gig 0/0/0
   Ip address 192.168.10.15 255.255.255.0
   ip ospf network point-to-point
   no shutdown
   end
   copy run start

**The routers on that link will no longer elect a designated router (DR) and backup designated router (BDR) for that subnet**

**Answer explanation:** Designating a link as a point-to-point link in OSPF indicates that it will
not send OSPF broadcast frames and not elect a DR and BDR for that subnet. This saves on
OSPF convergence time due to the lack of need for a DR/BDR election.
----------
A network engineer is troubleshooting poor wireless performance in an area of the
corporate building. Based on the size of the area and number of clients, there should be
enough access points to handle the traffic. All access points have been configured on the
same channel. What should the engineer do to resolve the performance issues in this
network?

**Configure the access points to transmit on nonoverlapping channels**
---------
What action could a network engineer take to ensure that all **OSPF routes are given a better administrative distance (AD) than all EIGRP routes when both protocols are configured on the same router**?

**Set the AD value for OSPF to 89**
**Answer explanation:** **EIGRP’s default AD value is 90**, and **OSPF’s default value is 110**. Setting
the AD for OSPF to a value of 89 would ensure that OSPF routes are favored.
---------
Which of the following commands is used to configure a **network address translation (NAT) router with a one-to-one mapping between a private and public IP address**?

**ip nat inside static 192.168.1.12 64.24.76.10**

Answer explanation: This will configure a single private IP address to map to a single public
IP address. This is known as static mapping and is used when there is a need for a single
device with a private IP to use a public IP provided for address translation purposes
-----------
Which is the correct **port on a wireless LAN controller (WLC) to connect to a switch in 802.1q mode** for passing normal access point traffic?

**Distribution**
Answer explanation: A distribution system port is used to pass all access point normal and
management traffic over an 802.1q trunk to a switch.
----------
In **WPA3 Simultaneous Authentication of Equals (SAE)**, what is the final step in the process after which regular data can be transmitted?

**4-way handshake**
Answer explanation: 4-way handshake is the final step of the WPA3 SAE process, which will
generate keys to ensure encryption. Regular data can be transmitted after this.
----------
Which flag is set in the first TCP packet sent by a device initiating a communication?
* ACK
* FIN
* PSH
* RST
* **SYN**
---------
**BR2# show ip route**
<... output omitted ...>

**Gateway of last resort is 172.16.2.3 to network 0.0.0.0**

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
D*EX  **0.0.0.0/0 [170/7289856] via 172.16.2.3, 00:00:22, Ethernet0/0** => **(* indicates the default route that is `D*EX` )**

Refer to the exhibit. Router BR2 receives a packet with the destination IPv4 address of 172.16.5.20. Based on the routing table, what would the router do with the packet?

* **Forward it out of interface Ethernet0/0.**
* Forward it out of interface Ethernet0/1.
* Forward it out of interface Loopback0.
* It will discard the packet.

Answer
The correct answer is **Forward it out of interface Ethernet0/0**. **If a router does not find a match in its routing table, it uses a default route if one exists**. In the example, the **default route points to the IPv4 address of 172.16.2.3, indicated by the "Gateway of last resort is 172.16.2.3 to network 0.0.0.0**" statement in the command output. 172.16.2.3 IPv4 address is reachable over Ethernet0/0 interface. If a route to a gateway of last resort IPv4 address does not exist, the router drops the packet.

------------
What are two results of configuring a default gateway on a host? (Choose two.)

* **A default route is added to the routing table of the host.**
* The host can get an IP address from the DHCP.
* The host can start communicating with other hosts on the same network.
* The ARP table of the host gets populated with IP to MAC address mappings of the hosts on remote networks.
* **The size of the ARP table of the host is reduced.**

Answer
The correct answers are **A default route is added to the routing table of the host** and **The size of the ARP table of the host is reduced**. The host forwards all traffic destined to remote networks to the default gateway. The router does not rely on the proxy ARP feature to forward the requests from the host, and the host does not add entries for remote IP addresses to the ARP table anymore. DHCP addressing should be explicitly configured for the host to be automatically assigned an IP address. DHCP is also used to provide default gateway addresses to the hosts. The host can communicate with other hosts on the same network without default gateway configuration.
---------
Refer to the exhibit. It represents the Cisco Enterprise Architecture model. In this model, where is the firewall located?

* between the edge router and the core switch
* between the edge router and the distribution switch
* between the internet and the core switch
* **between the internet and the edge router**
---------
Which three are the **most reliable network practices used in Networking?** (Choose three.)

* **automated systems testing**
* copying and pasting configuration from a text editor to a device
* manual system testing
* **using programmability tools to automate network configuration**
* **using version controls for all configuration changes**
---------
What is the MAC address of the interface that autoconfigures itself to the IPv6 address of fe80::2a3:C2ff:fefc:4a5d?

* **00:a3:c2:fc:4a:5d**
* 02:a3:c2:fc:4a:5d
* 02:a3:c2:ff:fe:fc
* 2a:3c:2f:ff:ec:4a
* c2:ff:fe:fc:4a:5d

Answer
The correct answer is **00:a3:c2:fc:4a:5d**. Autoconfiguration employs the modified EUI-64 format in order to determine the interface ID portion of the address. **The modified EUI-64 format uses the MAC address. The last 24 bits of the MAC address are preserved and become the last 24 bits of the autoconfigured IPv6 address**. **The first 24 bits of the MAC address have the seventh bit inverted**. Also, the **"fffe" sequence is appended to the end of the modified first 24 bits of the MAC address.** This new **40-bit structure is followed by the last 24 bits of the MAC address to form the IPv6 interface ID.**
---------
Which IPv6 network prefix is only intended for local links and cannot be routed?

* ::ffff/80
* 2001::/3
* fc00::/7
* **fe80::/10**
---------
Why are the SSH and HTTPS protocols preferred for management traffic?

* Because more detailed logging is possible.
* **Because they encrypt the management traffic.**
* Because they provide single sign-on capabilities.
* Because they prevent unauthorized logins.
---------
Refer to the exhibit. PC_A wants to communicate with PC_B, which resides on a different network. The hosts are connected via a router that acts as the default gateway for both. The ARP tables on all three devices are empty. When PC_A sends the first frame, which two things happen in the process? (Choose two.)

* PC_A broadcasts the frame intended for PC_B.
* **PC_A sends a broadcast ARP request looking for the MAC address of the router.**
* **The router adds an IPv4 address to the MAC address's mapping for PC_A to its ARP table**.
* The router drops the packet after checking for the mapping of PC_B's IP address.
* The router receives a frame with its own MAC and mismatched IP address, and drops it.

Answer
The correct answers are **PC_A sends a broadcast ARP request looking for the MAC address of the router** and **The router adds an IPv4 to the MAC address's mapping for PC_A to its ARP table**. Since PC_A does not have a destination MAC address for the IP address of host B, it first acquires this information using ARP. The ARP request is broadcast, and the router and all other devices on the same network segment receive the ARP request. Only the router responds to it with its own MAC address.
---------
A device **running a Windows OS has the IP address 169.254.254.254.** Which of the following statements is true?

* **The address is automatically configured by the device itself.**
* The device is reachable via the internet.
* The IP address is used to communicate with the default gateway.
* The IP address is a loopback address.

Answer
The correct answer is **The address is automatically configured by the device itself**. **The address space 169.254.0.0/16 is reserved for link-local IPv4 addresses**. **An end-device that supports IPv4 link-local addresses self-assigns an IPv4 address from the 169.254.0.0/16 range, when the address is not specified otherwise.** The link-local IPv4 address can be used only for local network connectivity and will not be routed.
---------
After receiving an Ethernet frame, a **switch examines the destination MAC address**, and **forwards the frame out of all ports except the incoming port**. In which communication types can this behavior occur?

* in broadcast and multicast communication
* in broadcast communication
* **in broadcast, multicast, and unicast communication**
* in unicast communication

Answer
The correct answer is in **broadcast, multicast, and unicast communication**. An Ethernet switch forwards a frame out of all ports except the incoming port when the intended recipients are all devices in a network, like in broadcast communication. It also forwards a frame out of all ports except the incoming port when communication is sent to a specific group of hosts, which is the case in multicast communications. In unicast communication, the switch will forward the frame out of all ports except the incoming port only when it does not have the destination MAC address in its MAC table.
---------
When using the modified **EUI-64 format to create the interface ID of an IPv6 unicast address, which two portions of the Ethernet MAC are used unchanged**? (Choose two.)

* Organizational Unique Identifier (OUI) octets
* **network interface card (NIC) specific octets**
* the universal/local bit
* **the unicast/multicast bit**
* the protocol type octet

Answer
The correct answers are **network interface card (NIC) specific octets** and **the unicast/multicast bit**. In an Ethernet MAC address structure, there is no specific type octet. The universal/local bit is the second-least significant bit in the MAC address. In the modified EUI-64 format, it is inverted. As this bit is part of the OUI octets, inverting it changes the value of the OUI octets as well.
---------
Refer to the exhibit. **Which of the routes is a floating static route?**

**BR2# show ip route**
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
**S     192.168.16.0/24 [90/0] via 172.16.2.1**
S     192.168.33.0/24 [1/0] via 172.16.2.1
      209.165.200.0/27 is subnetted, 1 subnets
D        209.165.200.224 [90/307200] via 172.16.2.1, 00:03:01, Ethernet0/0

* route to network 10.8.0.0/13
* route to network 172.16.1.0/30
* **route to network 192.168 16.0/24**
* route to network 192.168.33.0/24

Answer
The correct answer is **route to network 192.168.16.0/24**. **A floating static route is a static route with an administrative distance greater than the default value of 1**. **In the example we have two static routes, the route to network 192.16.33.0/24 has the default administrative distance**, and is therefore not floating static. The other two options are routes sourced from elsewhere, in this case from the EIGRP routing protocol, as indicated by the "D" protocol code.
---------
Which command would you use to configure a router ID on a Cisco router?
* R1 (config-router)# ip router-id ip-address
* **R1 (config-router)# router-id ip-address**
* R1 (config)# ip router-id ip-address
* R1 (config)# router-id ip-address

	R1 (config-router)# router-id ip-address
	-
	For the network device administrator to configure a router ID on a router, the router-id ip-address command is used. The ip router-id ip-address, ip router-id ip-address, and router-id ip-address commands do not configure router IDs.
---------
Which three of the following application characteristic values are determined in the service level specification phase when designing the quality of service (QoS) policy of a network? (Choose three.)
* generated data flows
* **required bandwidth**
* required responsiveness
* response criticality
* **tolerable jitter**
* **tolerable packet loss**
---------
After receiving a dynamic host protocol (DHCP) discover message from a client with an IP address of **0.0.0.0** , how does the DHCP server respond?

**A DHCP offer message is sent to 255.255.255.255**

Answer explanation: The next action in the **DHCP message chain is offer, and the server responds to this with a broadcast to all hosts on a subnet.** The address used is 255.255.255.255 since the host that sent the initial discovery does not have an IP address yet.
---------
An engineer needs to provide a connection for the internet service provider (ISP) to allow
for internet connectivity and wide area network (WAN) access for the corporate backbone
private network in a newly deployed branch office. The ISP has provided a Multiprotocol
Label Switching (MPLS) connection at the demark point. What device would enable them
to meet the requirements?

**Router**

Answer explanation: **Routers are used to create internetworks by connecting networks together and routing traffic between them.** Enterprise grade routers support many connection
types such as MPLS.
---------
A client has enabled **DHCP Snooping on the switches**, and it detects a violation. What will
happen next?

**The packet will be dropped, and an event will be generated that contains the text DHCP_SNOOPING in the log message**

Answer explanation: DHCP Snooping is a security feature. It prevents denial of service. **So, it will drop the packet as soon as a violation is detected, and the generated text will be DHCP_SNOOPING.**
---------
An engineer needs to configure a series of switchports so that the computers connected
to them have access only to engineering resources, while ensuring that the IP phones
connected to those ports are segmented away from engineering resources. Which
sequence of commands would the engineer use to accomplish this goal?

Ans:
	config t
	interface range fa0/1 - 09
	switcport mode access
	switchport access vlan 50
	switchport voice vlan 40
	exit
	copy run start

Answer explanation: To have segmentation for voice and data traffic on the same access
port, while preventing access to other segments of the network on the same switch, the port
must be configured as an access port and must also have a voice VLAN configured on it. This
configuration allows the engineer to accomplish this for a range of switchports intended to be
used for an engineering department’s resources.
---------
Which of the folliwing is used to **create a new switched virtual interface (SVI) and then place a series of ports in the virtual local area network (VLAN)** associated with it?

**spanning-tree vlan 1 root priority 36864**

Answer explanation: Spanning tree root priorities increase in increments of 4096 and must
fall in the range of 0 to 61440. **36864 is an increment of 4096.**
---------
Which of the following could an engineer use to **influence the OSPF metric value for a route?**

**The interface bandwidth subcommand**

Answer explanation: Adjusting the bandwidth value of an interface using the bandwidth
subcommand does not actually affect the available bandwidth the router sends data over an
interface. It will affect the metric value of OSPF for a given route as bandwidth is used to
directly determine the metric value.
---------
A user is trying to send a POST call to URI
https://sandboxdnac.cisco.com/dna/system/api/v1/auth/token. In
Authorization for this API call, the user is using Basic Auth and has provided the
username and password. However, while running the API, the user encounters the given
error. What is causing the error? Error:
<html>
<head><title>401 Bad Request</title></head>
<body bgcolor="white">
<center><h1>401 Bad Request</h1></center>
<hr><center>nginx/1.13.12</center>
</body>
</html>

**The username or password is incorrect**

Answer explanation: **401 means "unauthorized"**; the user does not have valid authentication
credentials for the target resource.
---------
Which command will create a **static default route for packets that do not match a more specific route?**

**ip route 0.0.0.0 0.0.0.0 GigabitEthernet 0/0/0**

Answer explanation: A **static route configured with all zeros and given an interface signifies a default route for all traffic that does not match a more specific route in the layer 3 devices routing table.** In this case, all traffic that does not match a more specific route will be sent to
interface Gigabit Ethernet 0/0/0.


---------
A network technician is addressing a problem where a **Windows desktop computer cannot access a network file share due to a firewall.** The technician wants to verify that the desktop's IP address has been permitted. Which command should the technician execute on the desktop to check the current IP address?

**ipconfig**

Answer explanation: **ipconfig** will show a summary of interfaces on a Windows system,
including assigned IPv4 and IPv6 addresses.
---------
An engineer is troubleshooting an employee's laptop issue and wants to ensure the switch
is correctly forwarding traffic. **The engineer does not see an entry for the laptop's MAC address in the CAM table, even though the laptop was connected to the network just a day ago. Which switching concept explains this absence?**

**Aging**

Answer explanation: **Aging describes the function of removing old entries from the CAM table after the configured amount of time has elapsed.**
---------
The following is a part of a wireshark trace, **which is related to IPSec**. Which phase of the
IPSec process does this trace match? Wireshark trace:

Internet Security Association and Key Management Protocol
Initiator SPI: a00b8ef0902bb8ec
Responder SPI: e47a591fd057587f
Next payload: Hash (8)
Version: 1.0
Exchange type: Quick Mode (32)
Flags: 0x01
Message ID: 0x635a2e6a
Length: 60
Encrypted Data (32 bytes)

**IKE Phase 2**
Answer explanation: This is the correct answer as the Exchange type is Quick Mode (32).
---------
An engineer is **troubleshooting an issue where the native virtual local area network (VLAN)on a trunk port is dropping traffic**. What command can they use on both switches to
confirm the native VLAN for each switch?

**show interfaces trunk**

Answer explanation: This command gives several outputs about the trunking status of a
switch. This includes the native VLAN for each trunk displayed. By running this command on
each switch the engineer can see the native VLAN for each side of the trunk.
---------
Ansible is being used in a network for configuration and management automation. **Which of the following are true statements regarding Ansible?** Select all that apply.

* **Ansible utilizes the concept of playbooks to execute the configuration**
* **Ansible uses SSH for remote device communication**

Answer explanation: Ansible Playbooks are lists of tasks that automatically execute for a
specified inventory or group of hosts. One or more Ansible tasks can be combined to make a
play—an ordered grouping of tasks mapped to specific hosts—and tasks are executed in the
order in which they are written.

Answer explanation: SSH is a critical piece in any Ansible-managed and controlled
infrastructure because Ansible relies on it to perform actions on the hosts.
---------
A network engineer is designing a **wired network to connect all servers and network equipment in a data center.** Which topology would she use to minimize network latency
and network distance between hosts?

**Spine-leaf**

Answer explanation: A **spine-leaf topology connects all hosts to Top of Rack (ToR) switches which then connect to core switches**. This design minimizes network latency and network
distance as all hosts are two hops away from each other.
---------
When configuring a **WLAN with WPA2 PSK in the Cisco Wireless LAN Controller GUI, which TWO formats are available to select? Select all that apply.**

* **HEX**
* **ASCII**

Answer explanation: The key format options available are ASCII and HEX.
Answer explanation: The key format options available are ASCII and HEX.
---------
The output of the command show ip route is shown below. What does the **C** code
signify in the first directly connected line?

Gateway of last resort is not set
192.168.1.0/24 is variably subnetted, 2 subnets, 2 masks
**C 192.168.1.0/24 is directly connected, GigabitEthernet0/0/0**
L 192.168.1.11/32 is directly connected, GigabitEthernet0/0/0
S 192.168.2.0/24 is directly connected, GigabitEthernet0/0/0

**The route is connected to the router**

Answer explanation: A connected route is one that has a corresponding layer 3 network
device directly connected to the router that the show ip route command was issued on.
directly connected and C codes are generated for subnets that are directly
connected to the router itself.
---------
If a route is configured using the following series of commands, where will the layer 3
device send a packet destined to the subnet 10.10.0.0 255.255.0.0 as its next hop? Commands:

	interface loopback 1
	ip address 10.10.2.3 255.255.0.0
	exit
	interface gig0/0/0
	ip address 10.10.2.11 255.255.0.0
	exit
	ip route 10.10.0.0 255.255.0.0 10.10.2.12
	ip route 10.10.2.3 255.255.255.255 10.10.2.2
	end
	copy run start

**To the interface associated with the address 10.10.2.12 as its next hop**

Answer explanation: The **layer 3 device is configured to use 10.10.2.12 as its next hop and would route the packets for 10.10.0.0/16** through the interface associated with that in its
routing table.
---------
An engineer has been asked to **disable Cisco Discovery Protocol (CDP) and Link Layer Discover Protocol (LLDP)** on a port that links to a partner switch. **The switch should still be able to use CDP and LLDP on other ports to ensure power delivery and device discovery.**
Which commands should the engineer run to accomplish this task?

Ans:
	config t
	interface gig 0/1/0
	no cdp enable
	no lldp transmit
	no lldp receive
	exit
	copy running-config startup-config

Answer explanation: This set of commands will allow for LLDP and CDP to run on a Cisco
switch on other ports, but will disable it on the interface which is being configured.
---------
An engineer has been tasked with adding a **backup route using IPv6 to reach a service.**
What should the engineer do to accomplish this?

**Add a static route with an administrative distance greater than that used by the routing protocol**

Answer explanation: **A static router with a greater administrative distance or floating static route would provide an additional way of reaching a network if the routing protocol was unaware of it for some reason.** This prevents the static route from being the primary way of
reaching the subnet as all static routes are given an administrative distance of 1 by default.
---------
A software engineer is tasked with developing a sophisticated logging and alerting
application for a custom data center. This application needs to reliably send information.
**Which network protocol should be used in application to guarantee reliable data packet delivery and retransmission?**

**Transmission Control Protocol (TCP)**

Answer explanation: TCP is a protocol designed to provide windowing, reliable transmision
of data, and is connection-oriented.
---------
Which **component of a wireless network infrastructure uses a single cable connected to an access port on a switch to provide routing for data and management traffic at layer 3?**

**Lightweight Access Point**

Answer explanation: **A lightweight access point in local mode uses a layer 3 connection over an access port on a switch to connect to a WLC using a CAPWAP tunnel.** Traffic is routed
between the two devices to provide data and management connectivity.
---------
An engineer has been given **instructions to mitigate a security threat that uses the default virtual local area network (VLAN) on Cisco switches.** To mitigate the possibility of an attack, he has been instructed to remove the functionality of the default VLAN. Which of the following does he need to type in the command line of the switch to achieve his assignment?

	config t
	interface vlan 1
	shutdown
	exit
	copy running-config startup-config

Answer explanation: This **shuts down the switched virtual interface (SVI) and makes the virtual local area network (VLAN) associated with it unable to pass traffic**. **VLAN 1 cannot be deleted on Cisco switches but putting it in the shutdown state should mitigate the attack.**
---------
Output of the show ip route command is given. According to this output, which of
the following denotes the next-hop packet destined for a host with the IP address of
192.168.23.10? Output:

10.0.0.0/8 is variably subnetted, 2 subnets, 2 masks
C 10.13.24.5/32 is directly connected, Loopback5
O 10.15.24.0/24 [110/65] via 192.168.6.2, 00:09:42, Serial0/1/0
C 192.168.10.0/24 is directly connected, Loopback1
L 192.168.10.1/32 is directly connected, Loopback1
192.168.13.0/32 is subnetted, 1 subnets
O 192.168.13.1/32 [110/2] via 192.168.1.11, 00:25:21, GigabitEthe
O 192.168.23.0/24 [110/65] via 192.168.6.2, 00:15:28, Serial0/1/0

**192.168.6.2**

Answer explanation: **A packet sent to the address of 192.168.23.10 will travel over the 192.168.23.0/24 network given that there is not a more specific route**


---------
Which of the following commands is used to configure a **network address translation (NAT) router with a one-to-one mapping between a private and public IP address**?

**ip nat inside static 192.168.1.12 64.24.76.10**

Answer explanation: This will configure a single private IP address to map to a single public
IP address. This is known as static mapping and is used when there is a need for a single
device with a private IP to use a public IP provided for address translation purposes
---------
A packet is sent to host **8.12.64.54** and routed through a router with the following
output of the show ip route command. What next-hop-address is the packet sent
to? Output:

**Gateway of last resort is 192.168.12.10 to network 0.0.0.0**
10.0.0.0/8 is variably subnetted, 2 subnets, 2 masks
C 10.12.16.4/32 is directly connected, Loopback4
S 10.15.24.0/24 [89/0] via 192.168.12.10
O 192.168.1.0/24 [110/66] via 192.168.23.6, 00:58:14, GigabitEthe
192.168.6.0/30 is subnetted, 1 subnets
O 192.168.6.0/30 [110/65] via 192.168.23.6, 00:58:14, GigabitEthe
192.168.10.0/32 is subnetted, 1 subnets
O 192.168.10.1/32 [110/66] via 192.168.23.6, 00:58:14, GigabitEth
192.168.12.0/24 is variably subnetted, 2 subnets, 2 masks
C 192.168.12.0/24 is directly connected, GigabitEthernet0/0/1
L 192.168.12.11/32 is directly connected, GigabitEthernet0/0/1
192.168.13.0/32 is subnetted, 1 subnets
O 192.168.13.1/32 [110/67] via 192.168.23.6, 00:58:14, GigabitEth
192.168.23.0/24 is variably subnetted, 2 subnets, 2 masks
C 192.168.23.0/24 is directly connected, GigabitEthernet0/0/0
L 192.168.23.5/32 is directly connected, GigabitEthernet0/0/0
S* 0.0.0.0/0 [1/0] via 192.168.12.10

**192.168.12.10**

Answer explanation: The **gateway of last resort is set to send packets via 192.168.12.10**. Since
the 8.0.0.0 network has no route in the routing table it will default to the gateway of last
resort to send the packet on.
---------
An engineer needs to collect and store all information about device state changes. This
includes information about any configuration changes that were made to the network
devices and the administrators who made these changes. What can the engineer do to
ensure this information is collected and stored properly?

**Use the logging host command flag with the appropriate logging trap level to ensure that the network devices record events that happen remotely**

Answer explanation: The host syntax configures a syslog server to send configured log traps
to. This would store the logs generated for the level that is configured to be sent to the syslog
server. Using traps configured at the correct level, the syslog server will store and allow for
network administrators to access the logs for troubleshooting and investigations.
---------
A system administrator is configuring **IPv6 on the external interface of a web server and wants to ensure traffic from the Internet can be routed to the server.** Which type of
Unicast address should be configured on the interface?

**Global**

Answer explanation: IPv6 **global unicast addresses are routable IP addresses similar to public IPv4 addresses.**
------------
Which of the following **commands creates a network route on a layer 3 device for the 10.0.10.0/24 subnet**?

* **ip route 10.0.10.0 255.255.255.0 10.0.10.5**
Answer explanation: This creates a static route for the network 10.0.10.0/24 that is routed via the IP address 10.0.10.5 for its next hop.
-------------
What are the **benefits of using network automation**? Select all that apply.

* **Faster changes with more reliable results**
* **Reduced operational costs**

Answer explanation: Network automation allows administrators to make changes to the
network quickly and consistently, reducing the risk of human error and ensuring that changes
are applied consistently across the network. This helps to minimize downtime and improves
the reliability of the network.

Answer explanation: Automation enables you to reduce manual, tedious, and repetitive work,
which in turn lowers operating costs.
-------------
When **troubleshooting a dynamic host configuration protocol (DHCP)**, an engineer sees a message on a wire capture that states “DHCP offer from 192.168.10.24 to 255.255.255.255." If all is working properly, what message should the engineer see next?

**A DHCP request from host 0.0.0.0**

Answer explanation: **DHCP messages happen in an order often referred to by the acronym DORA, which stands for discover, offer, request, acknowledge.**
---------
When running the command **switchport trunk encapsulation dot1q** on a newly deployed switch, an engineer receives **the error % Invalid input detected at '^' marker**. What should he do to prevent this error in the future?

**Remove the command switchport trunk encapsulation dot1q from the cutsheet**

Answer explanation: The **error occurs because by default all new Cisco equipment uses 802.1q for the trunking protocol and ISL has been deprecated.** Removing the command would keep the error from occurring again as there is no option to use any other protocol than 802.1q.
-----------
A network engineer is designing a wired network for a small company's main campus. Which network topology would she use to minimize the number of core switches needed while still allowing flexibility for expansion?

**Two-tier**

Answer explanation: **The two-tier, or collapsed core, topology reduces costs by combining the core and distribution layers. This allows for a smaller number of core switches, reducing cost, but allowing for expansion over time.**
------------
Which of the following are **Layer 2 security options when configuring a WLAN controller?**
Select all that apply.

* **Static WEP**
* **802.1x**
* **WPA+WPA2**

Static WEP
Answer explanation: WLANs with the same SSID must have unique Layer 2 security policies
so that clients can make a WLAN selection based on the information advertised in beacon
and probe responses. The available Layer 2 security policies are Static WEP.

802.1x
Answer explanation: WLANs with the same SSID must have unique Layer 2 security policies
so that clients can make a WLAN selection based on the information advertised in beacon
and probe responses. The available Layer 2 security policies are 802.1X.

WPA+WPA2
Answer explanation: WLANs with the same SSID must have unique Layer 2 security policies
so that clients can make a WLAN selection based on the information advertised in beacon
and probe responses. The available Layer 2 security policies are WPA+WPA2.
----------
Which of the **following are network management features performed by both traditional network management software and DNA Center?** Select all that apply.

**Device installation (day 0), configuration (day 1), and monitoring (day n) operations Answer explanation: Both methods provide ways to install, configure, and monitor the device operations.**

**Network device discovery**

Answer explanation: Network device discovery is provided by both management methods.
----------
Output of the command show ip route is given. In this output, **which route is the default route?** Output:
	O 192.168.10.1/32 [110/2] via 192.168.1.10, 00:46:50, GigabitEthe
	192.168.12.0/24 is variably subnetted, 2 subnets, 2 masks
	C 192.168.12.0/24 is directly connected, GigabitEthernet0/0/1
	L 192.168.12.10/32 is directly connected, GigabitEthernet0/0/1
	192.168.13.0/24 is variably subnetted, 2 subnets, 2 masks
	C 192.168.13.0/24 is directly connected, Loopback1
	L 192.168.13.1/32 is directly connected, Loopback1
	S* 0.0.0.0/0 is directly connected, GigabitEthernet0/0/1

**S* 0.0.0.0/0 is directly connected, GigabitEthernet0/0/1**

Answer explanation: The **S*** in the routing table code signifies a **static route that is the candidate default route for the layer 3 device.** A route of all zeros for the network identifier and subnet mask is the default route for a layer 3 device and any packets that do not match a more specific route are sent to that route. By default, a layer 3 device drops packets if there is no default route created.
----------
Output of the show ip route command is given. According to this output, to which IP address will a packet from the **IP address of 192.168.1.12 and a subnet mask of 255.255.255.0 be sent?** 
Output:
	Gateway of last resort is not set
	O 192.168.1.0/24 [110/65] via 192.168.6.1, 02:03:49, Serial0/1/0
	192.168.6.0/24 is variably subnetted, 2 subnets, 2 masks
	C 192.168.6.0/30 is directly connected, Serial0/1/0
	L 192.168.6.2/32 is directly connected, Serial0/1/0
	192.168.10.0/32 is subnetted, 1 subnets
	O 192.168.10.1/32 [110/65] via 192.168.6.1, 02:03:49, Serial0/1/0
	192.168.13.0/32 is subnetted, 1 subnets
	O 192.168.13.1/32 [110/66] via 192.168.6.1, 02:03:49, Serial0/1/0
	192.168.15.0/27 is subnetted, 1 subnets
	O 192.168.15.0/27 [110/66] via 192.168.6.1, 02:03:49, Serial0/1/0

**/24**

Answer explanation: A /24 CIDR notation corresponds with a 255.255.255.0 dotted decimal
notion subnet mask.
----------
Which of the following commands is used to **configure a network address translation (NAT) router with a one-to-one mapping between a private and public IP address?**

**ip nat inside static 192.168.1.12 64.24.76.10**

Answer explanation: This will configure a single private IP address to map to a single public
IP address. This is known as static mapping and is used when there is a need for a single
device with a private IP to use a public IP provided for address translation purposes
----------
Which **command would correctly configure the IPv6 address on a router interface using the EUI-64** (Extended Unique Identifier) format for the interface ID?

**Router(config-if)# ipv6 address 2001:0db8:19ab:1::/64 eui-64**

Answer explanation: This command correctly sets the IPv6 address using the EUI-64 format on an interface.
----------
To explain the **data center network segment she works in, an architect describes each service, the unified communications server (UCS), and how they connect to leafs of the application centric infrastructure (ACI).** Which of the following describes the network components that connect to the leafs?

**Endpoint**

Answer explanation: **Endpoints in an ACI deployment are the physical and virtual devices that connect to the ACI leafs**. **Endpoints can also refer to end user devices like IP phones, laptops, smartphones, and tablets.**
----------
A topology is given in which C1 is the router on customer site 1, and C2 is the router on customer site 2. ISP1, ISP2, and ISP3 constitute the Internet. The routing table on ISP2 and the GRE tunnel config on C1 and C2 routers are also given. Based on this information and assuming that all components are correctly configured, **why will the tunnel interface on C1 be unable to ping the tunnel interface on C2?** Topology: <144
_
stem
_
1 "PC1 is
connected to router C1 on customer site 1. PC2 is connected to router C2 on customer
site 2. C1 and C2 can communicate with each other over the internet which in this case
comprises of ISP1,ISP2 and ISP3. ISP1 IP : 8.8.10.1/24 (G0/0/0) and 8.8.8.2/24 (G0/0/1)
ISP2 IP : 8.8.8.1/24 (G0/0/0) and 8.8.9.1/24 (G0/0/1) ISP3 IP : 8.8.9.2/24 (G0/0/0) and
8.8.11.1/24 (G0/0/1) C1 IP : 10.1.3.1/24 (Tun0) and 10.1.1.1/24 (G0/0/0) C2 IP : 10.1.3.2/24
(Tun0) and 10.1.2.1/24 (G0/0/0)"

> Routing table on ISP2:
8.0.0.0/8 is variably subnetted, 6 subnets, 2 masks
8.8.8.0/24 is directly connected, GigabitEthernet0/0/0
8.8.8.1/32 is directly connected, GigabitEthernet0/0/0
8.8.9.0/24 is directly connected, GigabitEthernet0/0/1
8.8.9.1/32 is directly connected, GigabitEthernet0/0/1
8.8.10.0/24 [20/0] via 8.8.8.2, 00:00:00
8.8.11.0/24 [20/0] via 8.8.9.2, 00:00:00

ISP2#
	GRE tunnel config on C1 router:
	interface Tunnel0
	ip address 10.1.3.1 255.255.255.0
	mtu 1476
	tunnel source GigabitEthernet0/0/1
	tunnel destination 8.8.11.2
	
	GRE tunnel config on C2 router:
	interface Tunnel0
	ip address 10.1.3.2 255.255.255.0
	mtu 1476
	tunnel source GigabitEthernet0/0/0
	tunnel destination 8.8.10.2

**Standard IP access list 2 10 permit any**

Answer explanation: Here, we are using inverse mask. The IP address here is irrelevant as we
are asking it to not match with any octet, so any IP address will be allowed.

----------
An engineer is trying to determine **why a serial interface is not electing a designated router (DR) and backup designated router (BDR) in an OSPF-routed network.** They run the following command and get the following output. Why does the link not have a DR and BDR? Command and output:

\	**Router#sh ip ospf interface serial 0/1/0**
	Serial0/1/0 is up, line protocol is up
	Internet address is 192.168.6.2/30, Area 0
\	Process ID 1, Router ID 1.1.1.1, **Network Type POINT-TO-POINT**, Cos
\	Transmit Delay is 1 sec, State **POINT-TO-POINT,**
	Timer intervals configured, Hello 10, Dead 40, Wait 40, Retransmi
	Hello due in 00:00:03
	Index 1/1, flood queue length 0
	Next 0x0(0)/0x0(0)
	Last flood scan length is 1, maximum is 1
	Last flood scan time is 0 msec, maximum is 0 msec
	Neighbor Count is 1, Adjacent neighbor count is 1
	Adjacent with neighbor 192.168.10.1
	Suppress hello for 0 neighbor(s)

**This interface is a point-to-point link**

Answer explanation: The link is in a point-to-point state, which tells OSPF to stop sending
link state advertisement broadcast frames and to disable the DR/BDR election process,
which shortens the convergence time between the two routers.
----------
A network engineer is **documenting information about all the areas of a small OSPF network, including the process ID, area, and authentication type.** Which of the following commands can she use on each router to gather the required information?

**show ip ospf**

Answer explanation: The process ID, area, and authentication type are all shown under the
show ip ospf command. This will allow the engineer to gather the required information
from each router.
----------
What happens **when a packet arrives at a router but has multiple routes that it can use to arrive at its destination?**

**The route with the longest prefix is chosen**

Answer explanation: Routers use the longest match or most specific route to determine
where a packet with overlapping routes is sent. Generally this infers a host route and a
network route exist that overlap.
----------
An engineer has received complaints of **slow connectivity or constant disconnect from the third floor of the main campus building he works in**. An active heatmap of the floor shows that the area where this is occurring has no coverage. What action can the engineer perform to restore connectivity for the employees?

**Deploy a new or replace the existing access point (AP) in that location**

Answer explanation: Access points contain one or more antennas and provide wireless connectivity to devices. Adding an access point is an effective way to increase, or improve, the coverage of a wireless network.
----------
Which **spanning tree ports state is a switchport in, if it is a root port and passing traffic?**

**Forwarding**

Answer explanation: The forwarding state allows traffic to pass for a port and is the state
that forwards frames over a root or designated port. If a BPDU hello is no longer received on a
root port after, the MaxAge time has passed, then it is placed in a blocking state and spanning
tree convergence process begins.
----------
An engineer has been asked to **enable Cisco Discovery Protocol (CDP) globally** on a switch and **disable it from running on all but those ports dedicated to phones and access points**. Which commands should the engineer run to accomplish this task?

Answer:
	config t
	cdp run
	interface range gig 0/1/0 - 14
	no cdp enable
	exit
	copy running-config startup-config

Answer explanation: This would achieve the required results for the engineer. **The cdp run command will enable cdp globally and then the interface range command will allow them to apply the no cdp enable command to all the interfaces that they do not want cdp to run on.**
----------
An engineer has been assigned a task to **verify that a port-channel has been configured and is up.** Entering the following commands returns the following output, which shows the port-channel on both sides of the group is in the down state. **What is the issue causing the port-channel not to form**? Commands and output:

	Switch1#sh etherchannel summary
	----omitted for brevity----
	Number of channel-groups in use: 1
	Number of aggregators: 1
	Group Port-channel Protocol Ports
	------+-------------+-----------+--------------------------------
	1 Po1(SD) PAgP Fa0/1(I) Fa0/2(I) Fa0
	-----------------------------

	Switch2#sh etherchannel summary
	----omitted for brevity----
	Number of channel-groups in use: 1
	Number of aggregators: 1
	Group Port-channel Protocol Ports
	------+-------------+-----------+--------------------------------
	1 Po1(SD) LACP Fa0/1(I) Fa0/2(I)

**The protocols used to form the port-channel are different**

Answer explanation: In the output on **switch1, it states that PAgP** is the protocol used, **while LACP is used on switch2**. Using the same protocol on both should allow the port-channel to form.
----------
A network engineer is monitoring switch traffic in the morning as hybrid workers are plugging in their laptops to the network. The **engineer notices an initial burst of traffic that does not repeat**. Which switching function is likely responsible for this initial burst?

**Flooding**

Answer explanation: **Flooding means forwarding a frame to all active interfaces if the destination is not found in the switch's CAM table.** This occurs when devices are first plugged into the network, or when they come back onto the network after having been disconnected.
----------
Router 1 is already configured properly, and the two routers being connected are part of **area zero which uses the 10.10.10.0/24 network.** Which sequence of commands would result in a pair of routers that are directly connected exchanging OSPF routing information?

Answer:
	config t
	interface loopback 1
	ip address 1.1.1.1
	no shutdown
	exit
	router ospf 1
	network 10.10.10.0 255.255.255.0 area 0
	end
	copy run start

Answer explanation: The configuration will create a network with an area associated with it, **a loopback interface with an IP address that is in an up-up state to stand in place of a router ID, and a process ID for OSPF.** The other router would have similar information and share the same area of one of its configured networks.
----------
**An engineer has received a new wireless LAN controller (WLC) and needs to configure some basic connectivity on it so that its management options are available over the network**. Which type of connection will the engineer use to connect to the WLC from their laptop?

**Console**

Answer explanation: A **console connection allows an engineer to use a console cable to directly connect their laptop to a device, in this case the WLC,** to make configurations on it out-of-band of the network.
----------
An engineer needs to ensure that the **clock for a group of routers is configured to automatically update to daylight savings time.** Which sequence of commands should she use to accomplish this?

* **clock timezone EST -5**
* **clock summer-time EDT recurring**

Answer explanation: **This will set the time zone for the clocks on the routers to US Eastern Standard Time. It will also set the router to automatically use the default of the US daylight savings time rules to adjust to US Eastern Daylight Time.**
----------
Two routers, R1 and R2, are connected to each other directly. **You are trying to connect to R2 from R1 remotely using TELNET,** but the connection is failing. A portion of the config on R2 is given. Assuming everything else has been configured correctly, what might be preventing the connection from working? Portion of config on R2:
	line con 0 exec-timeout 0 0 privilege level 15 logging synchrono
	line vty 0 4 exec-timeout 5 0
	password cisco login local transport input ssh end

**Vty lines have been configured to use ssh protocol and not telnet**

Answer explanation: If you want to prevent non-SSH connections, add the transport input ssh command under the lines to limit the router to SSH connections only. Straight (non-ssh) Telnets are refused. As this is a remote connection, it will use the VTY lines, which have been configured to use SSH.
----------
There is a requirement to secure the given topology based on the given traffic flows.
**Which of the following ACL show outputs contains the correct configuration?**
Topology:

PC1 and PC2 connected to Switch 0 which in turn is connected to Router1. HTTP server 1 and HTTP
server 2 connect to Router1 via Switch1. Then , Router1 is also connected to 3 web servers and a PC over
the internet PC1 IP : 10.1.2.101 PC2 IP : 10.1.2.102 HTTP server 1 IP : 10.1.1.100 HTTP server 2 IP : 10.1.1.101
Traffic flows:
	PC1 IP: 10.1.2.101
	PC2 IP: 10.1.2.102
	HTTP server 1 IP: 10.1.1.100
	HTTP server 2 IP: 10.1.1.101
	Use access list number 100
	Inside PC1 can only access the HTTP server 1 using HTTP on subnet 10.1.1.0/24
	Inside PC2 can only access the HTTP server 2 using HTTPS on subnet 10.1.1.0/24

**Router1 #sh access-lists Extended IP access list 100 10 permit tcp host 10.1.2.101 host 10.1.1.100 eq www 20 permit tcp host 10.1.2.102 host 10.1.1.101 eq 443**

Answer explanation: Here, 10.1.2.101 will reach 10.1.1.100 over port 80/www , and 10.1.2.102 will reach 10.1.1.101 over port 443, which satisfies the requirement.
----------
What command is used to **secure a remote terminal** so that a passphrase must be entered to gain access to the configuration mode of a router or switch after the remote user has successfully logged on using secure shell (SSH)?

**enable secret Cisco123**
Answer explanation: This command is used to secure the virtual terminal (VTY) lines so that
a remote administrator needs to enter a second device passphrase once they access a
network device. This command uses plain text to store the phrase, but can be encrypted by
using password encryption.
----------
What **happens to a packet when a router has multiple routes with the same administrative distance for the destination that the packet is sent to?**

**The router will choose the route with the lowest metric**
Answer explanation: The **lowest metric like the lowest AD** is the next option a router uses to determine the best path to send a packet.
----------
Here are some portions of traces from **wireshark, captured from two different packets**. There are many packets with similar traces. What appears to be the issue with the traces and how could it be prevented?
	Trace 1:
	Sender MAC address: VMware_8e:ee:89 (00:50:56:8e:ee:89)
	Sender IP address: 192.168.1.12
	Target MAC address: Cisco_35:64:8a (00:22:90:35:64:8a

	Trace 2:
	Sender MAC address: VMware_8e:ee:89 (00:50:56:8e:ee:89)
	Sender IP address: 192.168.1.25
	Target MAC address: VMware_8e:5e:33 (00:50:56:8e:5e:

**This looks like ARP spoofing/poisoning, which can be prevented by using Dynamic Arp Inspection**

Answer explanation: Since the **MAC address 00:50:56:8e:ee:89 is corresponding to two different IP addresses**, it is **ARP spoofing, which can be prevented by using Dynamic Arp Inspection.**
----------
Which **method does a wireless LAN controller (WLC) use to pass traffic to and from a lightweight access point when in local mode in a split-MAC architecture?**

**CAPWAP tunneling uses a layer 3 address on the access point to form a layer 3 connection with the WLC and route traffic**

Answer explanation: **CAPWAP tunneling over layer 3 allows the access point to route traffic for all SSIDs back to the WLC without needing an additional trunk configuration on the switch.**
----------
Which part of a **Cisco DNA Center software-defined access (SDA) fabric provides physical connectivity between nodes in the environment to support Virtual Extensible LAN (VXLAN) tunnels?**

**Underlay**

Answer explanation: **Underlays in the SDA fabric are the physical devices and connections between different nodes.** The **underlay generally uses a routed access layer design** to support the **VXLANs** that allow for **tunnling between the overlay nodes.**
----------
The command output of **show ip route from a layer 3 device is given. Which portion of the output represents a prefix that is connected via OSPF and has 256 addresses associated with it?** Output:
	Gateway of last resort is 192.168.12.10 to network 0.0.0.0
	10.0.0.0/8 is variably subnetted, 2 subnets, 2 masks
	C 10.12.16.4/32 is directly connected, Loopback4
	S 10.15.24.0/24 [89/0] via 192.168.12.10
	O 192.168.1.0/24 [110/66] via 192.168.23.6, 01:21:08, GigabitEth
	L 192.168.12.11/32 is directly connected, GigabitEthernet0/0/1
	** omitted for brevity**

**O 192.168.1.0/24 [110/66] via 192.168.23.6, 01:21:08,**

Ans
**GigabitEthernet0/0/0**

Answer explanation: **This represents a subnet with 256 IP addresses that is learned via OSPF**
----------
The **command output of _show ip route_ from a layer 3 device is given.** Which portion of the output represents a locally connected network prefix with one IP address? Output:
Gateway of last resort is not set
	**lines ommitted**
	O 192.168.10.1/32 [110/2] via 192.168.1.10, 00:15:52, GigabitEthe
	192.168.13.0/24 is variably subnetted, 2 subnets, 2 masks
	C 192.168.13.0/24 is directly connected, Loopback1
	L 192.168.13.1/32 is directly connected, Loopback1
	You selected Answer 3 Correct

**L 192.168.13.1/32 is directly connected, Loopback1**

Answer explanation: **This represents a specific route with one IP address available to use for the layer 3 device and is configured on its loopback 1 interface**. This results in a **status code of L , or locally connected.** This is the most specific route available for the layer 3 device.
----------
A network engineer **wants to ensure that data transmitted over the wireless network can't be intercepted and read by unauthorized individuals.** What should she mplement to ensure this?

**Encryption**

Answer explanation: **Encryption is used to hide data so that only users with the correct key can read the data.**
----------
Which option on a **wireless LAN Controller (WLC) graphical user interface (GUI) provides the location to configure a switched virtual interface (SVI) for a service set identifier (SSID)?**

**Controller > interfaces > edit**

Answer explanation: This configuration option allows for the creation and editing of the virtual local area network (VLAN) setting on the WLC, including SVI information.
----------
**What address is used in an OSPF network to send messages to the designated router (DR)?**

**224.0.0.6**

Answer explanation: **The routers in an OSPF network that are not DRs send messages to the DR and backup designated router (BDR) using the multicast address 224.0.0.6.**
----------
What is the administrative distance (AD) given to the statically created route in the output given? Output:
	Gateway of last resort is not set
	O 192.168.1.0/24 [110/65] via 192.168.6.1, 02:26:33, Serial0/1
	192.168.6.0/24 is variably subnetted, 2 subnets, 2 masks
	C 192.168.6.0/30 is directly connected, Serial0/1/0
	L 192.168.6.2/32 is directly connected, Serial0/1/0
	192.168.10.0/32 is subnetted, 1 subnets
	O 192.168.10.1/32 [110/65] via 192.168.6.1, 02:26:33, Seria
	O 192.168.13.1/32 [110/66] via 192.168.6.1, 02:26:33, Seria
	S 192.168.17.0/24 [1/0] via 192.168.6.1

**1**

Answer explanation: **Static routes are given a default AD of 1.** This makes them **preferred over other routes unless adjusted since a lower AD is preferred** when making routing decisions.
----------
You have configured a **router (R1) to use TACACS to authenticate users**, and the command used is given. What is local being used to specify in this command? Command:
	R1 (config)# aaa_authentication login default group tacacs+ local 
	R1 (config)#

**To use local authentication as a backup, if TACACS serve is not reachable**

Answer explanation: The **router fails over to local authtentication only when the TACACS server is not reachable**.
----------
In the given topology, **Router2 can be pinged from Router1, but trying to telnet fails**. Based on the Router1 config, what may be the cause of failure for the telnet connection?
Topology:
In this topology we have 2 routers, Router 1 (IP 10.1.1.1/24) and Router 2 (IP 10.1.1.2/24) directly connected
to each other.
	Router1 config:
	Router1#ping 10.1.1.2
	Type escape sequence to abort.
	Sending 5, 100-byte ICMP Echos to 10.1.1.2, timeout is 2 seconds:
	.!!!!
	Success rate is 80 percent (4/5), round-trip min/avg/max = 0/0/0
	Router1#telnet 10.1.1.2
	Trying 10.1.1.2 ...Open
	[Connection to 10.1.1.2 closed by foreign host] Router1#
Failure:
	interface GigabitEthernet0/0/0 ip address 10.1.1.1 255.255.255.0
	speed auto
	!
	interface GigabitEthernet0/0/1 no ip address duplex auto speed
	shutdown
	!
	interface VLAN1 no ip address
	shutdown
	!
	ip classless
	!
	ip flow-export version 9
	!
	line con 0
	!
	line aux 0
	!
	line vty 0 4
	login
	!
	end
	interface
	GigabitEthernet0/0/0
	on it is up or not

**A login password for the VTY lines needs to be configured**

Answer explanation: **There is no password configured for the VTY lines on the router, so telnet will not work because the login is disabled till the password is set.**
----------
Type **1 hypervisors, which provide network access for services, include components that facilitate intercommunication between these services within the hypervisor before they communicate outside.** Which component is **responsible for passing traffic between the services and allowing those services to communicate at open systems interconnection (OSI) layer 2?**

**Virtual switch**

Answer explanation: **Virtual switches are a component of the hypervisor and are responsible for receiving network traffic from virtual hosts in a hypervisor and distributing network traffic to the virtual hosts**.
----------
Which **quality of service (QoS) toolset is used to refer to the action a network device uses when it has packets waiting to be sent?**

**Queuing**

Answer explanation: **Queuing is the toolset that QoS uses to manage the queues that hold data or packets** while they are waiting to be forwarded out of an outgoing interface. Queuing is used in QoS schemes to manage and help prevent dropped packets.
----------
An engineer needs to **configure a series of switchports so that the computers connected to them have access only to engineering resources, while ensuring that the IP phones connected to those ports are segmented away** from engineering resources. Which sequence of commands would the engineer use to accomplish this goal?

Ans:	
	config t
	interface range fa0/1 - 09
	switcport mode access
	switchport **access** vlan 50
	switchport **voice** vlan 40
	exit
	copy run start

Answer explanation: To have segmentation for voice and data traffic on the same access port, while preventing access to other segments of the network on the same switch, the port must be configured as an access port and must also have a voice VLAN configured on it. This configuration allows the engineer to accomplish this for a range of switchports intended to be used for an engineering department’s resources.

----------
Which of the **following best describes what happens from a downstream switch perspective when the host standby router protocol (HSRP) fails over?**

**The virtual mac address moves to the device that now is the active router, updating the switch.**

Answer explanation: **HSRP uses a virtual mac address to advertise which device is the active router**. While the arp table and layer 3 address do not change, the host’s switch updates its mac address table to point the virtual IP toward the now active HSRP router.
----------
A network engineer is **updating a switch configuration to include a virtual local area network (VLAN) that uses 802.1q tagging to allow IP telephony for phones connected on edge switchports.** Which command should the engineer use to add the VLAN to these ports?

**switchport voice vlan 11**

Answer explanation: **switchport voice vlan 11 adds vlan 11 as a voice VLAN 11 to an access port allowing for a special 802.1q tagged vlan to carry IP telephony traffic.**
----------
What is the **minimum necessary configuration for a router running OSPF as a routing protocol to function?**

**Area, Router-ID, Network, OSPF process ID**

Answer explanation: For OSPF to function, **at least two layer 3 devices running OSPF must be connected, both configured with a network that is assigned to an area, a process-ID, and a router-ID to exchange routing information**. **Alternatively, to a router-ID, a router can be configured with an up-up loopback address** that has a unique IP address assigned to it.
----------
What **advantage does an autonomous access point (AP) architecture provide when compared to an access point leveraging CAPWAP mode?** 

**Autonomous AP architectures provide a more efficient path for data over wired and wireless networks they are part of**

Answer explanation: **Autonomous APs manage traffic between clients connected on the same AP locally instead of sending that traffic back to a controller**. This makes for a simpler and more direct path for data to travel to the switch that AP is connected to, enhancing the performance and responsiveness of the network.
----------
A network engineer is **troubleshooting connectivity issues on a layer 2 switch.** An IP phone that shows as registered and passes traffic is connected to one of the ethernet ports on the switch. **However, a computer plugged into the phone's built-in switchport does not pass traffic on the corporate network over the computer's ethernet port.** What table can the engineer use to look up on the switch to see if the burned-in address of the computer and phone are registered?

**Media access control (MAC) address table**

Answer explanation: **When traffic from a new device is seen for the first time traffic is forwarded out all interfaces and the burned-in or MAC address is added to the MAC address table.** If the switch was able to register the computer's and phone's MAC address would show up.
----------
What **prefix length is used to create a static IPv6 host route?**

**/128**

Answer explanation: This prefix is used to designate a single IPv6 address and is needed to provide a host route.
----------
A network engineer is **deploying a new multilayer switch to an office and replacing the older edge router and switch to conserve space in the network closet**. What function does the **multilayer switch perform in this network segment?**

**It provides open systems interconnect (OSI) layer 2 connectivity and layer 3 routing for the devices connected to the office network**

Answer explanation: The switch can provide layer 2 connectivity for the local area network (LAN), but since the router has been removed, it also provides layer 3 connectivity for routing. OSI layer 2 connectivity will not replace the routing functionality of the router that was removed. A switch that allows for layer 3 functionality can replace both devices in this context.
----------
A system administrator is setting up a **streaming media application that will stream data from a server to multiple clients that are setup as receivers, but not to any clients that are not receivers.** Which IPv6 address type meets this requirement?

**Multicast**

Answer explanation: **Multicast addresses are used to send a message from one source to multiple destination interfaces at the same time.**
----------
A **VXLAN tunnel is configured between two servers**. Which of the following **best defines the VXLAN tunnel in a controller-based network?**

**Overlay network**
**Shaping**

Answer explanation: Devices on **overlay** networks are interconnected through logical links, constituting overlay topologies. Tunnels are established between interconnected overlay devices. Overlay networks support various network protocols and standards, including virtual extensible local area network (VXLAN), Network Virtualisation using Generic Routing Encapsulation (NVGRE), single spanning tree (SST), GRE, Network Virtualisation over Layer 3 (NVO3), and Ethernet Virtual Private Network (EVPN). ----------
An engineer has a remote office that sends and receives data using a committed information rate (CIR) of 200 mbps from a service provider. The service provider discards traffic that exceeds the agreed-upon CIR from clients entering and exiting their network. A second remote site that often sends data to this office uses a CIR of 600 mbps from their service provider, often sending data at a rate that exceeds the CIR of 200 mbps. What can the engineer implement to ensure that the CIR for the remote office is not exceeded?

Answer explanation: **Shaping** uses queuing to slow down packets that egress over a link with higher bandwidth than the CIR given to it. The shaper will allow for burst activity to not exceed the CIR given.
----------
What is the **proper dotted decimal notion (DDN) for a subnet mask corresponding with a /27?**

**255.255.255.224**

Answer explanation: **This subnet mask corresponds with a /27.** The binary output for this is 11111111.11111111.11111111.**11100000**, which leaves 27 ones for the network portion and five zeros for the host portion of the mask.
----------
You have a PC with the IP config given. The **Gateway for this machine is 10.1.1.254 , which is not reachable.** You run the given command on the switch that connects this machine and the gateway, and see the given output. **Which security protocol is preventing the PC from reaching the gateway? IP config:**

	root@kali:~# ifconfig | head -n 3
	eth0: flags=4163&lt;UP, BROADCAST, RUNNING, MULTICAST&gt; mtu 150
	inet6 fe80::52aa:774c: b0e5:acc7 prefixlen 64 scopeid 0x20
Command and output:
	sh ip dhcp snooping binding
	MacAddress IpAddress Lease(sec) Type
	0C:37:5F:E9:5A:00 10.1.1.2 86308 dhcp-snoopin
	GigabitEthernet0/1
	Total number of bindings: 2

**Dynamic ARP inspection**

Answer explanation: **Dynamic ARP inspection allows a network administrator to intercept, log, and discard ARP packets with an invalid MAC address to IP address bindings.** As the MAC address of the machine in the ifconfig output is different from the DHCP binding table, ARP inspection will deny this machine's traffic.
----------
Which **sequence of commands creates a router ID if the router-id OSPF** command is not used?

	config t
	interface loopback 1
	no shut
	ip address 2.2.2.2 255.255.255.255
	exit
	copy run start

Answer explanation: **This syntax is used to create a loopback address that OSPF will use as its router ID**. OSPF uses the highest IP address that is created on a loopback address. As long as that loopback is in an up-up state and has a valid IP, OSPF will use it as a router ID.
----------
What does the **FULL term indicate when seen in the output of show ip ospf neighbor command?**

**The neighbors are either a designated router (DR) or backup designated router (BDR)**

Answer explanation: The **routers can exchange Hello packets, updates, queries, replies, and acknowledgments between each other, and the neighbor is either a DR or BDR.**
----------
An engineer has been given the task of **configuring a switch with the following command**. What is the effect of the command on the network? _Command: Spanning-tree vlan 1 root primary_

**The configured switch will become the primary root of the spanning tree network with a bridge priority of 24576**

Answer explanation: **The command gives the switch its input on a lower priority than the default priority of 24576. If no other switches in the network have been manipulated, this bridge will become the primary root bridge.**
----------
A command line output is given. In this output, what does the **O** code for the last line represent? Command line output:

Gateway of last resort is not set
**lines omitted**
L 192.168.10.1/32 is directly connected, Loopback1
192.168.13.0/32 is subnetted, 1 subnets
O 192.168.13.1/32 [110/2] via 192.168.1.11, 00:00:19, GigabitEthernet 0/0/0
OSPF is the routing protocol being used and is connected to another device via

**GigabitEthernet 0/0/0**

Answer explanation: **OSPF is represented by O** , and the connected device that is exchanging routes with the layer 3 device is using GigabitEthernet 0/0/0 and the IP address of 192.168.1.11 on the other end of the ethernet connection used for routing information between the two layer 3 devices.
----------
Which of the following **commands is used to configure a network address translation (NAT) router with a one-to-one mapping between a private and public IP address?**

**ip nat inside static 192.168.1.12 64.24.76.10**

Answer explanation: This will configure a single private IP address to map to a single public IP address. This is known as static mapping and is used when there is a need for a single device with a private IP to use a public IP provided for address translation purposes
----------
The corporate **dynamic host configuration protocol (DHCP) server is located in a remote data center from a branch office.** Which of the following **should be used to configure a layer 3 device, which doesn't run a DHCP server, to forward DHCP traffic to the remote data center?**

**ip helper-address 192.168.15.10**

Answer explanation: This would configure the device to use the server with an IP address of 192.168.15.10 for all DHCP message traffic to and from the local networks which it is aware of.
----------
An engineer needs to provide a connection for the **internet service provider (ISP)** to allow for internet connectivity and wide area network (WAN) access for the corporate backbone private network in a newly deployed branch office. The ISP has provided a **Multiprotocol Label Switching (MPLS)** connection at the demark point. What device would enable them to meet the requirements?

**Router**

Answer explanation: Routers are used to create internetworks by connecting networks together and routing traffic between them. Enterprise grade routers support many connection types such as MPLS.
----------
An engineer is working to deploy a new set of switches and has created a cut-sheet to copy and paste for easier manual deployment. **The engineer is using SSH to deploy the switch, and once they paste the following section in, they lose connectivity.** The engineer cannot regain access to the switch. What might have caused this issue?

	config t
	interface range gig 0/0/0 - 8
	Interface vlan 1
	shut
	vlan

**The cut-sheet shutdown VLAN 1, causing the switch to lose connectivity and disconnecting the SSH session**

Answer explanation: **All switchports are in the default VLAN and shutting down that VLAN would cause all connectivity to the switch to stop**. This would disconnect the SSH session. The engineer could reboot the switch to revert the changes since the changes were only in the running configuration and had not been saved.
----------
A system administrator wants to configure interfaces on a **group of distributed servers so that traffic is only routed to the closest server**. Which **IPv6** address type meets this requirement?

**Anycast**

Answer explanation: **Anycast addresses use the same address on multiple interfaces and only the closest interface will receive the traffic.**
----------
Which of the following show configuration commands can **show multiple devices on one switchport, leverage sub-interfaces, and display the operating system information of connected devices by a Cisco switch?**

**show cdp neighbors**

Answer explanation: **Cisco Discovery Protocol (CDP) is a proprietary protocol that is used to identify and display information about devices connected to a switchport.** It can display information about multiple devices connected to the same switchport. It also will **display information about the status of the device including operating system.**
----------
Based on the following command output, **which route is chosen when a packet for 10.1.1.9 is sent to this router?** Output:
	Router#show ip route
	** omitted for brevity***
	10.0.0.0/8 is variably subnetted, 2 subnets, 2 masks
	S 10.1.1.0/24 [1/0] via 172.16.12.15
	S 10.1.1.9/32 is directly connected, GigabitEthernet0/0/0
	Router#sh run | s ip route
	ip route 10.1.1.9 255.255.255.255 GigabitEthernet0/0/0
	ip route 10.1.1.0 255.255.255.0 172.16.12.15

**It will route out interface Gigabit Ethernet 0/0/0**

Answer explanation: The more **specific or longer network prefix of a /32 that is associated with a host route created to use Gigabit Ethernet 0/0/0 to pass on packets that are destined for that host will be used for routing any the packet described in the question.**

----------
Which of the following sets of **actions satisfies the requirement for multifactor authentication?**

**The user enters a username and password and then clicks a notification in an authentication app on a mobile device**

Answer explanation: **Multi-factor authentication (MFA) is a multi-step account login process that requires users to enter more information than just a password. For example, along with the password, users might be asked to enter a code sent to their email, answer a secret question, or scan a fingerprint.** **A second form of authentication can help prevent unauthorized account access if a system password has been compromised.**
----------
A router has been configured with a static route of **ip route 10.15.24.0 255.255.255.0 192.168.23.6 109 , however show ip route gives the following output. Why doesn’t the configured route show in the output?** Output:

10.0.0.0/8 is variably subnetted, 2 subnets, 2 masks
C 10.12.16.4/32 is directly connected, Loopback4
S 10.15.24.0/24 [89/0] via 192.168.12.10

**There is a route with a lower administrative distance that already exist**

Answer explanation: A route with an **administrative distance of 89 to that subnet already exists.**
----------
**Ten devices that are plugged into a network via ethernet are unable to pass traffic or connect to the corporate local area network.** **When a support engineer investigates, she cannot find the media access control (MAC) addresses of the devices on any network equipment She also notices that the lights on the ethernet ports are not lit up.** What type of network component can the engineer deploy to resolve this issue?

**Switch**

Answer explanation: **Switches are used to expand networks by adding additional ports for devices to connect to. Each port on a switch is its own collision domain.**
----------
An engineer needs to provide wired and wireless connectivity for **four sales engineers in a regional sales office**. She wants to deploy only one device at this location. Which network topology should she use?

**Small office, home office (SOHO)**

Answer explanation: Small office, home office (SOHO) **describes networks that are used by a small number of people sharing resources such as file servers and printers**. They are generally deployed as a single device.
----------
What is the **next hop for the serial interface as displayed** by the given output of the show ip route command? Output:

Gateway of last resort is not set
O 192.168.1.0/24 [110/65] via 192.168.6.1, 02:03:49, Serial0/1/0
192.168.6.0/24 is variably subnetted, 2 subnets, 2 masks
C 192.168.6.0/30 is directly connected, Serial0/1/0
L 192.168.6.2/32 is directly connected, Serial0/1/0
192.168.10.0/32 is subnetted, 1 subnets
O 192.168.10.1/32 [110/65] via 192.168.6.1, 02:03:49, Serial0/1/0
192.168.13.0/32 is subnetted, 1 subnets
O 192.168.13.1/32 [110/66] via 192.168.6.1, 02:03:49, Serial0/1/0

**192.168.6.1**

Answer explanation: **This is the address for the other router that is connected over serial 0/1/0 and is the next hop address that is used for routing to any of the subnets reachable via serial 0/1/0** that are not local to this router.
----------
A sales company has a headquarters building **which hosts an email server and file server that are used by all company employees. Salespeople for the company travel extensively all over the world and need access to these resource servers while traveling.** Which topology should the company use to enable all its traveling employees to access the internal resources?

**Virtual Private Area Netwrork (VPN)**

Answer explanation: **Virtual Private Area Network (VPN) can provide network services to users anywhere in the world and can include cellular or satellite connections.** VPN's commonly route traffic over the internet and are used for wide area networks (WAN) that require additional security.

----------
Which of the following **command sequences is used to create a dynamic network address translation (NAT) configuration on a Cisco NAT router that uses port mapping and private IP addressing** to perform its necessary functions?

Ans
	config t
	int gig0/0/0
	ip nat inside
	int gig0/0/1
	ip nat outside
	access-list 10 permit 10.10.12.0 0.0.0.255
	ip nat inside source list 10 interface gig0/0/1 overload
	copy run start

Answer explanation: This **configuration identifies the hosts that are inside the enterprise network, and the overload syntax on the access list tells the router to use PAT to identify where traffic is sent from a host outside the enterprise.** This allows for a single public IP address to be used while sending traffic up to 65,000 concurrent flows.
----------
**An admin is trying to configure a banner for a router.** What they see in the router's config is given. Assuming the correct delimiter has been used, what is expected outcome?
Router's config:

!
banner motd ^C
================
No unauthorized access
================
^C
!

**The banner will be seen as soon as the admin connects to the router via any connection**

Answer explanation: **A banner message of the day is prompted before the user authentication and is applied on all lines.** An exec banner is used to display messages post the authentication of a user.
----------
**In WPA3, what key exchange protocol replaces the Pre-Shared Key (PSK) used in previous versions?**

**SAE (Simultaneous Authentication of Equals)**

Answer explanation: **WPA3 replaces the PSK with SAE** to provide better protection against offline dictionary attacks.
----------
An engineer **needs to configure a new switch port to automatically initiate trunk negotiation messages and establish a trunk connection with an upstream switch.** Given that the connecting **port of the upstream switch is statically set as a trunk**, what command should they use to achieve this?

**Switchport mode dynamic desirable**

Answer explanation: **dynamic desirable is the command that will make the trunk port actively look for a statically configured or dynamically configured trunk and then automatically become a trunk port.** **By default, trunk ports are set to dynamic desirable.**
----------
A network engineer is troubleshooting a report of network performance issues on a server. Checking the switch **port shows a high number of CRC errors**. What is the likely cause of the network performance issue?

**Duplex mismatch**

Answer explanation: A **duplex mismatch between a server and a switch will cause a high number of errors,** such as CRC errors or late collisions. This can lead to connectivity issues and poor performance.
----------
A network engineer is delivering part of a new implementation of a branch site. They are responsible for implementing the virtual local area network (VLAN) configuration across all the switches deployed. Part of the deployment configuration disables VLAN 1 without making any other VLAN configuration changes. **However, once the implementation is complete, some Internet of Things (IoT) devices that do not use VLAN tagging can no longer reach their controller.** What does the network engineer need to do to resolve this issue?

**Create a VLAN and configure it as a native VLAN**

Answer explanation: **Untagged traffic passes over the native VLAN. Since the IoT devices communicate with their controllers using untagged traffic in this scenario, this solution would work.**
----------
An engineer has configured an IP route using the command **ip route 192.168.10.0 255.255.255.0 130** , but the route is missing from the router’s routing table when checked, as shown in the following code block. Why does the engineer not see the route? Code block:

192.168.1.0/24 is variably subnetted, 2 subnets, 2 masks
C 192.168.1.0/24 is directly connected, GigabitEthernet0/0/0
L 192.168.1.11/32 is directly connected, GigabitEthernet0/0/0
S 192.168.2.0/24 is directly connected, GigabitEthernet0/0/0
192.168.6.0/30 is subnetted, 1 subnets
O 192.168.6.0/30 [110/65] via 192.168.1.10, 07:35:41, GigabitEthe
192.168.10.0/24 is subnetted, 1 subnets
O 192.168.10.0/24 [110/2] via 192.168.1.10, 07:41:48, GigabitEthe
192.168.12.0/24 is variably subnetted, 2 subnets, 2 masks

**The static route is a floating route**

Answer explanation: The **static route is a floating route that has a higher administrative distance than the OSPF default of 110.** This means that the **router will not add it to the routing table as long as the OSPF route is still available.**
----------
Which of the following commands is used to configure a **network address translation (NAT) router with a one-to-one mapping between a private and public IP address?**

**ip nat inside static 192.168.1.12 64.24.76.10**

Answer explanation: **This will configure a single private IP address to map to a single public IP address.** This is known as static mapping and is used when there is a need for a single device with a private IP to use a public IP provided for address translation purposes.
----------
A network architect is **designing a network with a goal of maintaining maximum control, including physical, of all the company's servers and networking equipment**. Which network topology would they use to meet this goal?

**On-premise**

Answer explanation: **On-premise networks are networks where all equipment is kept in physical locations, such as data centers, controlled by the organization.** This is the only topology that maximizes physical control of devices.
----------
A network segment that functions as the connection between the access layer and distribution layer has 4 switches that are interconnected via single TenGigabit ethernet links. An engineer configures one of the layer 3 switches in the topology to carry ten virtual local area networks (VLANs) over one of the links that carries traffic between the access and distribution layers. **Which command would the engineer use to ensure that both sides of the link connecting the two layer 3 switches always carry all ten configured VLANs and will never revert to carrying only a single VLAN?**

**switchport mode trunk**

Answer explanation: **Statically assigning both sides of the link to the switch and router each as trunk ports will ensure they always form trunks on both sides.**
----------
Which of the following is the **correct administrative distance (AD) for OSPF?**

**110**

Answer explanation:**110 is the correct AD for OSPF.**
----------
Which of the following command **seqeunces will invoke an OSPF process and configure a router ID for a layer 3 device running OSPF?**

Ans:
	router ospf 1
	router-id 1.1.1.1

Answer explanation: **router-id is the command that will create an OSPF identifier for a router**. **This command comes after invoking the OSPF process**. Alternatively, an engineer can use a loopback address that is on an interface in an up-up state to create a router identifier.
----------
What happens when you configure a **router running OSPF as its internal routing protocol** using the following sequence of commands? Commands:

config t
interface gig0/0/1
no shut
no ip address
ip address 172.16.12.15 255.255.0.0
exit
ip route 172.17.0.0 255.255.0.0 172.16.12.16 130
end

**A floating static route for 172.17.0.0 will be configured on the router**

Answer explanation: **A floating route for the network 172.17.0.0/16 will be created with an administrative distance of 130**. **If OSPF is not able to route packets for this network,** then the router will use this static route and inject it into the routing table. **Floating static routes like this are used to create backup routes.**
----------
Which command provides a layer of **assurance on a port configured with PortFast in case a switch is plugged in to that port?**

**spanning-tree bpduguard enable**

Answer explanation: The **bpduguard command looks for bridge protocol data units (BPDUs) from a switch and immediately puts the port in an error-disabled state if one is detected. PortFast is a Cisco proprietary protocl that was created to avoid the problems that come about when a PC is connected to a port and DHCP times out because of spanning tree timers.**
----------
A topology is given in which C1 is the router on customer site 1, and C2 is the router on customer site 2. ISP1, ISP2, and ISP3 constitute the Internet. The routing table on ISP2 and the GRE tunnel config on C1 and C2 routers are also given. Based on this information and assuming that all components are correctly configured, why will the tunnel interface on C1 be unable to ping the tunnel interface on C2?

PC1 is connected to router C1 on customer site 1. PC2 is connected to router C2 on customer site 2. C1 and C2 can communicate with each other over the internet which in this case comprises of ISP1,ISP2 and ISP3. ISP1 IP : 8.8.10.1/24 (G0/0/0) and 8.8.8.2/24 (G0/0/1) ISP2 IP : 8.8.8.1/24 (G0/0/0) and 8.8.9.1/24 (G0/0/1) ISP3 IP : 8.8.9.2/24 (G0/0/0) and 8.8.11.1/24 (G0/0/1) C1 IP : 10.1.3.1/24 (Tun0) and 10.1.1.1/24 (G0/0/0) C2 IP : 10.1.3.2/24 (Tun0) and 10.1.2.1/24 (G0/0/0)

Routing table on ISP2: 
	8.0.0.0/8 is variably subnetted, 6 subnets, 2 masks
	8.8.8.0/24 is directly connected, GigabitEthernet0/0/0 
	8.8.8.1/32 is directly connected, GigabitEthernet0/0/0 
	8.8.9.0/24 is directly connected, GigabitEthernet0/0/1 
	8.8.9.1/32 is directly connected, GigabitEthernet0/0/1 
	8.8.10.0/24 [20/0] via 8.8.8.2, 00:00:00 
	8.8.11.0/24 [20/0] via 8.8.9.2, 00:00:00
	ISP2#

GRE tunnel config on C1 router: 
	interface Tunnel0
	ip address 10.1.3.1 255.255.255.0
	mtu 1476
	tunnel source GigabitEthernet0/0/1
	tunnel destination 8.8.11.2

GRE tunnel config on C2 router:
	interface Tunnel0
	ip address 10.1.3.2 255.255.255.0
	mtu 1476
	tunnel source GigabitEthernet0/0/0
	tunnel destination 8.8.10.2


**It will not work because the tunnel configuration on C2 is incorrect**

Answer explanation: **An incorrect interface has been configured on C2 as the tunnel source. It should have been GigabitEthernet0/0/1.**
----------
Which of the following **interface commands is used to manually configure a routers weight as a neighbor for an OSPF area?**

**ip ospf priority 3**

Answer explanation:**The interface command ip ospf priority with a value after adjusts the weight or priority of a routers interface in an OSPF area**. This affects the priority by which the routers interface is used for the designated router (DR) and backup designated router (BDR) are determined.
----------
A client is using network devices with an **OS that doesn't support Puppet**, but they have a company policy to utilize Puppet for automation.** How can Puppet be used this situation?

**Puppet use a proxy agent running on an external host; the agent can then use SSH to communicate with the network devices**

Answer explanation:**Puppet can help achieve this by using a proxy agent, which utilizes SSH.**
----------
Which command is used to **correctly configure an IPv6 network route?**

**ipv6 route 2001:dc6:1010:2::/64 s0/1/0**

Answer explanation:This creates a **network route that sends traffic destined for the ipv6 network to serial 0/1/0.**
----------
Which **IPsec protocol is responsible for providing encryption, authentication, and integrity for the payload of IP packets?**

**ESP (Encapsulating Security Payload)**

Answer explanation:**IPsec originally defined two protocols for securing IP packets: Authentication Header (AH) and Encapsulating Security Payload (ESP).** The former provides data integrity and anti-replay services, and the latter encrypts and authenticates data.
----------
A wireless **LAN controller (WLC) has lost all network access, and a network engineer needs to restore functionality to the device.** The engineer has physical access to the WLC.  Which of the following should she use to gain access to the device command file?

**Security**

Answer explanation: The **korn shell is a shell used for accessing linux or unix devices that have it installed.** It is not a method for accessing a WLC remotely 
----------
An engineer needs to create a **point-to-point network to provide connectivity between two remote sites** over the corporate backbone network. He has been given a **subnet of 192.168.30.0/28** . Which command would he use to configure the **first available address on one of the Cisco router's Gigabit Ethernet 0/0/0 interfaces?**

**Router(config-if)# ip address 192.168.30.1 255.255.255.240**

Answer explanation:With a **/28 subnet mask the usable addresses for the 192.168.30.0 network are 192.168.30.1-14**. This command correctly sets the IP address to lowest usable address in the range.
----------
A network administrator has been tasked with securing simple network management protocol (SNMP) traffic and configurations. **They will do this by ensuring that only specific SNMP servers send and receive SNMP traffic to network devices, that the traffic is encrypted, and that the server authenticates with the client.** What should network administrator do to meet these requirements?

**Use SNMPv3 and IPv4 and IPv6 ACLs**

Answer explanation:**SNMPv3 supports the encryption of traffic between client and server and the ability to use username and password authentication that is not sent in clear text.** Using IPv4 and IPv6 **ACLs ensures that the traffic between the SNMP network management servers (NMSs) and the SNMP clients is not allowed to pass over other network segments or be exposed to other NMSs and clients.**

----------
Which type of network is represented in the given image?
packet -> R1(Data Plane) -> OSPF Packet -> R2(Data Plane) -> OSPF Packet -> R3(Data Plane) -> Packet
A **packet is being routed through the three routers.**

Ans:
**Traditional network**

Answer explanation:In this image, **each router has its own control plane and has the capability to make its own forwarding decisions.** This is the architecture of a traditional network.
----------
You are an engineer at a compay that has several Cisco Adaptive Security Appliance (ASA) Firewalls deployed in a data center network segment. **You need to automatically prevent known malicious traffic to the segment while allowing legitimate traffic to pass through.** What can you do to ensure that the requirements are met?

**Deploy a Cisco Firepower module to each firewall and configure it for intrusion prevention**

Answer explanation:**Intrustion Prevention Systems (IPS) attempt to detect attacks and stop them before they reach protected systems.** **The Firepower module for an ASA would allow the engineer to deploy an intrusion prevention system (IPS) to the network segment.** This allows for the **automatic detection of malicious traffic and prevent that traffic while allowing legitimate** traffic to pass over the network segment.
----------
**Which of the following statements are correct?** Select all that apply.

* **Radius security protocol uses UDP**
* **TACACS+ security protocol encrypts the entire body of the packet**
* **Radius encrypts only the password in the request packet**

Answer explanation:Radius security protocol utilizes User Datagramp Protocol, which offers best-effort delivery.
Answer explanation:TACACS+ security protocol encrypts the entire body of the packet but leaves a standard TACACS+ header.
Answer explanation:Radius security protocol encrypts only the password in the access- request packet from the client to the server.
----------
A network engineer is designing a wired network for a large enterprise's facilities, **which span multiple physical buildings**. Which network **topology would he use to maximize resiliency and scalability in the switching infrastructure?**

**Three-tier**

Answer explanation:**The three-tier topology uses separate switches for the core, distribution, and access layer f unctionality.** This topology provides easy scalability as well as resiliency.
----------
What is the **advantage of using PortFast configuration on the switchports available** in a desktop switch environment?

**PortFast allows end-user devices to connect almost instantly**

Answer explanation:**PortFast allows a port to bypass spanning tree, allowing it to become active almost immediately once a device is connected**.
----------
Which of the following options **would allow a channel group to always form using Link Aggregation Control Protocol (LACP)?**

**On both switches, use the command channel-group 1 mode active**

Answer explanation:**If both sides of a port-channel are configured using the active command, they will form a port-channel using LACP.** Active mode sends LACP packets and tries to establish a link with the other side when configured in this way.
----------
**A frame is sent from a device on a local area network to the port to which it is connected. The network device has a record of the destination in its media access control (MAC) address table. The frame is malformed, and the data is corrupt.** How does the network device know that the frame is malformed?

**Frame Check Sequence (FCS)**

Answer explanation:**FCS is the function of a frame to determine that the data it transmits is error free**. It is a 4-byte portion of the thernet header and is transmitted at layer 2.
----------
An engineer must configure dynamic host configuration protocol (DHCP) to be available on all devices in a subnet. After configuring the DHCP relay for the network, she wants to confirm if hosts are receiving DHCP-provided IP addresses and gateways. Which of the following should she type in the command prompt on a **Windows laptop to determine** if it will receive DHCP-configured IP addresses when connected to a switch port on the local area network?

**ipconfig /all**

Answer explanation:This will show all the DHCP-provided information for the network interface used to connect to the local network segment. If DHCP is enabled on the interface and a DHCP server is available, the devices will receive information provided by that server and give lease obtained as well as expiration information.
----------
A customer whose **environment comprises of public networks has a requirement of setting up SNMP server**. As a **network security consultant, how would you recommend setting it up?** Select all that apply.

* **Use SNMP v3, as it provides Data Tampering and Eavesdropping protection**
* **Use SNMP v3, as it provides DES/SHA/MD5 encryption**

Answer explanation: As it is a **public facing network, Data Tampering and Eavesdropping
protection is necessary and it is not provided by SNMP v2.**

Answer explanation: As it is a **public facing network, data encryption is necessary. SNMP v2 provides no data encryption.**
----------
What happens **when a packet arrives at a router but has multiple routes that it can use to arrive at its destination?**

**The route with the _longest_ prefix is chosen**

Answer explanation: **Routers use the longest match or most specific route to determine where a packet with overlapping routes is sent.** Generally this infers a host route and a network route exist that overlap.
----------
Which of the **following statements are true for a controller-based network**? Select all that

* **It uses north-bound and south-bound APIs to communicate between architectural layers**
* **It moves the control plane to a central point**

Answer explanation: Controller-based networking is a style of building computer networks
that uses a **controller that centralizes some features and provides application programming interfaces (APIs) that allow for software interactions between applications and the controller (north-bound APIs) and between the controller and the network devices (south-bound APIs).**

Answer explanation: Controller-based networking is a style of building computer networks that uses a controller that centralizes some features and provides **application programming interfaces (APIs) that allow for software interactions between applications and the controller (north-bound APIs) and between the controller and the network devices (south-bound APIs).**
----------
Which sequence **of commands will ensure that remote users use the newest version of secure shell (SSH), prevent insecure protocols for connectivity, and use md5 encryption to secure the enable secret?**

**Ans:**
	config t
	service password-encryption
	enable secret Cisco123
	ip ssh version 2
	crypto key generate rsa general-keys modulus 768
	line vty 0 - 15
	transport input ssh
	end
	copy run start

Answer explanation: This **meets all the requirements listed**. It enables **SSHv2, encrypts the enable secret with md5, and only uses SSH for VTY connectivity.**
----------
Which command **would correctly configure the IPv6 address on a router interface using the EUI-64** (Extended Unique Identifier) format for the interface ID?

**Router(config-if)# ipv6 address _2001:0db8:19ab:1::/64 eui-64_**
**Note:** You should use the **/64 subnet** mask to configure the **EUI64 - IPv6 address.**

Answer explanation: This command correctly sets the IPv6 address using the EUI-64 format on an interface.
----------
An engineer has been asked to **enable Cisco Discovery Protocol (CDP) globally on a switch and disable it from running on all but those ports dedicated to phones and access points**. Which commands should the engineer run to accomplish this task?

**Ans:**
	config t
	cdp run
	interface range gig 0/1/0 - 14
	no cdp enable
	exit
	copy running-config startup-config

Answer explanation: This would achieve the required results for the engineer. The **cdp run command will enable cdp globally and then the interface range command will allow them to apply the no cdp enable command to all the interfaces that they do not want cdp to run on.**
----------
An engineer has received complaints of **slow connectivity or constant disconnect from the third floor of the main campus building he works in**. An active heatmap of the floor shows that the area where this is occurring has no coverage. What action can the engineer perform to restore connectivity for the employees?

**Deploy a new or replace the existing access point (AP) in that location**

Answer explanation: Access **points contain one or more antennas and provide wireless connectivity to devices. Adding an access point is an effective way to increase, or improve, the coverage of a wireless network**.
----------
An engineer has been assigned a task to verify that a port-channel has been configured and is up. Entering the following commands returns the following output, which shows the port-channel on both sides of the group is in the down state. What is the issue causing the port-channel not to form? Commands and output:
	Switch1#sh etherchannel summary
	----omitted for brevity----
	Number of channel-groups in use: 1
	Number of aggregators: 1
	Group Port-channel Protocol Ports
	------+-------------+-----------+--------------------------------
	1 Po1(SD) PAgP Fa0/1(I) Fa0/2(I) Fa0
	-----------------------------
	Switch2#sh etherchannel summary
	----omitted for brevity----
	Number of channel-groups in use: 1
	Number of aggregators: 1
	Group Port-channel Protocol Ports
	------+-------------+-----------+--------------------------------
	1 Po1(SD) LACP Fa0/1(I) Fa0/2(I)

**The protocols used to form the port-channel are different**
**Note: SW1 uses PAgP and S2 uses LACP**

Answer explanation: In the output on **switch1, it states that PAgP is the protocol used, while LACP is used on switch2**. Using the same protocol on both should allow the port-channel to form.
----------
Which of the **following commands is used to configure a network address translation (NAT) router with a one-to-one mapping between a private and public IP address?**

**ip nat inside static 192.168.1.12 64.24.76.10**

Answer explanation: This will configure a single private IP address to map to a single public IP address. This is known as static mapping and is used when there is a need for a single device with a private IP to use a public IP provided for address translation purposes
----------
An engineer has **received a new wireless LAN controller (WLC) and needs to configure some basic connectivity** on it so that its management options are available over the network. Which type of connection will the engineer **use to connect to the WLC from their laptop?**

**Console**

Answer explanation: A **console connection allows an engineer to use a console cable to directly connect their laptop to a device,** in this case the WLC, to make configurations on it out-of-band of the network.
----------
A router has been **configured with a static route of ip route 10.15.24.0 255.255.255.0 192.168.23.6 109** , however **show ip route gives the following output. Why doesn’t the configured route show in the output?** Output:
	10.0.0.0/8 is variably subnetted, 2 subnets, 2 masks
	C 10.12.16.4/32 is directly connected, Loopback4
	S 10.15.24.0/24 [89/0] via 192.168.12.10

**There is a route with a lower administrative distance that already exist**

Answer explanation: **A route with an administrative distance of 89 to that subnet already**
exists.
----------
There is a requirement to secure the given topology based on the given requirements. Which of the following ACL show outputs contains the correct configuration?
Topology:

PC1 and PC2 are connected to Switch 0 which in turn is connected to Router1. HTTP server 1 and HTTP
server 2 are connected to Router1 via Switch1. Router1 is also connected to three web servers and a PC
over the internet.
Requirements:
	Inside PC 1 on subnet 10.1.2.0/24 can only access HTTP servers 1 and 2 on
	subnet 10.1.1.0/24 using HTTP and HTTPS
	Inside PC 1 IP : 10.1.2.101
	HTTP server 1 IP : 10.1.1.100
	HTTP server 2 IP : 10.1.1.101

**access-list 100 permit tcp host 10.1.2.101 10.1.1.100 0.0.0.1 eq www**
**access-list 100 permit tcp host 10.1.2.101 10.1.1.100 0.0.0.1 eq 443**

Answer explanation: In this option, **we have asked the inverse mask to match the first three IP octets and ignore the fourth one, so Inside PC 1 will be able to reach a machine with IP 10.1.1.x.** It will therefore cover both servers, i.e., 10.1.1.100 and 10.1.1.101.
----------
**VXLAN allows us to encapsulate data and deliver it to the destination**. On what layer does this encapsulation happen?

**It encapsulates both Layer 2 and Layer 3 frames**

Answer explanation: **VXLAN encapsulates the entire frame on both the layers.**
----------
Based on the following command output, which route is chosen **when a packet for 10.1.1.9 is sent to this router?** Output:
	Router#show ip route
	** omitted for brevity***
	10.0.0.0/8 is variably subnetted, 2 subnets, 2 masks
	S 10.1.1.0/24 [1/0] via 172.16.12.15
	S 10.1.1.9/32 is directly connected, GigabitEthernet0/0/0
	Router#sh run | s ip route
	ip route 10.1.1.9 255.255.255.255 GigabitEthernet0/0/0
	ip route 10.1.1.0 255.255.255.0 172.16.12.15

**It will route out interface Gigabit Ethernet 0/0/0**

Answer explanation: The more **specific or longer network prefix of a /32** that is associated with a host route created to use Gigabit Ethernet 0/0/0 to pass on packets that are destined for that host will be used for routing any the packet described in the question.
----------
Which sequence of commands **creates a router ID if the router-id OSPF command is not used?**

**Ans:**
	config t
	interface loopback 1
	no shut
	ip address 2.2.2.2 255.255.255.255
	exit
	copy run start

Answer explanation: This syntax is used to create a **loopback address that OSPF will use as its router ID.** OSPF uses the highest IP address that is created on a loopback address. **As long as that loopback is in an up-up state and has a valid IP, OSPF will use it as a router ID.**
----------
A network engineer is **monitoring switch traffic in the morning as hybrid workers are plugging in their laptops to the network.** The engineer notices an **initial burst of traffic that does not repeat**. **Which switching function is likely responsible for this initial burst?**

**Flooding**

Answer explanation: **Flooding means forwarding a frame to all active interfaces if the destination is not found in the switch's CAM table.** This occurs when devices are first plugged into the network, or when they come back onto the network after having been disconnected.
----------
Which spanning **tree ports state is a switchport in, if it is a root port and passing traffic?**

**Forwarding**

Answer explanation: The forwarding state allows traffic to pass for a port and is the state that forwards frames over a root or designated port. If a BPDU hello is no longer received on a root port after, the MaxAge time has passed, then it is placed in a blocking state and spanning tree convergence process begins.
----------
Local authentication has been configured on a router, but when an attempt is made to log in to its console, the enable mode is seen and no authentication prompt is received. The router config is given. Which of the following changes will help resolve the issue? 
Router config:
	!
	username xyz password 0 cisco
	!

**Configure login local for the console interface**

Answer explanation: To **enable a password check at login**, **use the login local command in line configuration mode**. Configure the **line console interface to enable local login by using the command login local.**
----------
What is the **next hop for the serial interface as displayed by the given output of the show ip route command? **Output:
	Gateway of last resort is not set
	O 192.168.1.0/24 [110/65] via 192.168.6.1, 02:03:49, Serial0/1/0
	192.168.6.0/24 is variably subnetted, 2 subnets, 2 masks
	C 192.168.6.0/30 is directly connected, Serial0/1/0
	L 192.168.6.2/32 is directly connected, Serial0/1/0
	192.168.10.0/32 is subnetted, 1 subnets
	O 192.168.10.1/32 [110/65] via 192.168.6.1, 02:03:49, Serial0/1/0
	192.168.13.0/32 is subnetted, 1 subnets
	O 192.168.13.1/32 [110/66] via 192.168.6.1, 02:03:49, Serial0/1/0

**192.168.6.1**

Answer explanation: **This is the address for the other router that is connected over serial 0/1/0 and is the next hop address that is used for routing to any of the subnets reachable via serial 0/1/0 that are not local to this router.**
----------
A network **engineer is designing a wired network for a small company's main campus**. Which network topology would she use to minimize the number of core switches needed while still allowing flexibility for expansion?

**Two-tier**

Answer explanation: **The two-tier, or collapsed core, topology reduces costs by combining the core and distribution layers.** This allows for a **smaller number of core switches, reducing cost, but allowing for expansion over time.**
----------
An engineer is working to deploy a new set of switches and has created a cut-sheet to copy and paste for easier manual deployment. **The engineer is using SSH to deploy the switch, and once they paste the following section in, they lose connectivity. The engineer cannot regain access to the switch**. What might have caused this issue?

	config t
	interface range gig 0/0/0 - 8
	Interface vlan 1
	shut
	vlan

**The cut-sheet shutdown VLAN 1, causing the switch to lose connectivity and disconnecting the SSH session**

Answer explanation: **All switchports are in the default VLAN and shutting down that VLAN would cause all connectivity to the switch to stop.** This **would disconnect the SSH session**. The **engineer could reboot the switch to revert the changes since the changes were only in the running configuration** and had not been saved.
----------
**Ten devices that are plugged into a network via ethernet are unable to pass traffic or connect to the corporate local area network.** When a support engineer investigates, **she cannot find the media access control (MAC) addresses of the devices on any network equipment She also notices that the lights on the ethernet ports are not lit up. What type of network component can the engineer deploy to resolve this issue?**

**Switch**


Answer explanation: **Switches are used to expand networks by adding additional ports for devices to connect to. Each port on a switch is its own collision domain.**
----------
There is a requirement to **configure aaa authentication (for login and enable) using RADIUS with server 10.1.1.250 for R2 in the given topology.** Assuming that the **RADIUS server is configured correctly**, which of the following best explains why this will not meet the requirements?
Topology:
**Router R1 and R2 are connected to a RADIUS server via a multilayer switch S1.**
Config on R2:

	R2 #sh run | i aaa aaa new-model 
	aaa authentication login default group radius local  aaa authentication enable default group radius local
	R2# sh run | i rad 
	aaa authentication login default group radius local  aaa authentication enable default group radius local

**The RADIUS server and its key have not been configured**

Answer explanation: **The command radius-server host 10.1.1.250 key xyz has to be run to point the router to the correct RADIUS server, and the key has to be configured as well.**
----------
A command line output is given. In this output, **what does the O code for the last line represent?** Command line output:
	Gateway of last resort is not set
	**lines omitted**
	L 192.168.10.1/32 is directly connected, Loopback1
	192.168.13.0/32 is subnetted, 1 subnets
	O 192.168.13.1/32 [110/2] via 192.168.1.11, 00:00:19, GigabitEthernet 0/0/0

**OSPF is the routing protocol being used and is connected to another device via GigabitEthernet 0/0/0**

Answer explanation: **OSPF is represented by O, and the connected device that is exchanging routes with the layer 3 device is using GigabitEthernet 0/0/0 and the IP address of 192.168.1.11 on the other end of the ethernet connection used for routing information between the two layer 3 devices.**
----------
What does the **FULL term indicate when seen in the output of show ip ospf neighbor command?**

**The neighbors are either a designated router (DR) or backup designated router (BDR)**

Answer explanation: The **routers can exchange Hello packets, updates, queries, replies, and acknowledgments between each other, and the neighbor is either a DR or BDR.**
----------
**Which Cisco DNA Center tool shows source IP addresses, destination IP addresses, source ports, and destination ports?**

* inventory
* **path trace service**
* ping service
* topology

Answer
The correct answer is **path trace service**. **The path trace service analysis allows you to examine the path that a specific type of packet travels as it makes its way across the network from a source to a destination node.** The result of a path trace will be a visual and textual representation of the path that a packet takes across all the devices, and links between the source and destination.
----------
Which three statements are **correct about the JSON data format**? (Choose three.)

* Empty values cannot be used in the JSON data format.
* JSON arrays separate elements using a semicolon.
* **JSON can be used when data is sent from a server to a web page.**
* **JSON does not support comments.**
* **JSON is a hierarchical data format.**
----------
A company wants to **interconnect all its branches. To ensure minimum downtime, the company wants to use a WAN that provides high availability and high redundancy**. Which WAN topology should the company use?

* **full mesh**
* hub-and-spoke
* partial mesh
* ring
----------
**Which type of cable is typically used to connect a core switch with a data center switch, where bandwidth higher than 40 Gbps and low cost are required?**

* Category 5e UTP
* Category 6 UTP
* **multimode fiber**
* single-mode fiber
----------
Which three statements describes **characteristics of solicited-node IPv6 addresses**? (Choose three.)

* There can be only one per device.
* **They are automatically created by the device.**
* They are created using the device's MAC address.
* **They are multicast addresses.**
* They are valid within an organization.
* **They have a recognizable prefix.**

Answer
The correct answers are **They are automatically created by the device, They are multicast addresses, and They have a recognizable prefix.** A **solicited-node multicast IPv6 address is created using special mapping of the device's unicast address with the recognizable solicited-node multicast prefix of ff02:0:0:0:0:1:ff00::/104.** A **device can have multiple solicited-node multicast addresses, because the multicast addresses are automatically created for every unicast address on a device.**
----------
What is the **MAC address of the interface that autoconfigures itself to the IPv6 address of fe80::2a3:C2ff:fefc:4a5d?**

* **00:a3:c2:fc:4a:5d**
* 02:a3:c2:fc:4a:5d
* 02:a3:c2:ff:fe:fc
* 2a:3c:2f:ff:ec:4a
* c2:ff:fe:fc:4a:5d

Answer
The correct answer is **00:a3:c2:fc:4a:5d**. Autoconfiguration employs the modified EUI-64 format in order to determine the interface ID portion of the address. The modified EUI-64 format uses the MAC address. **The last 24 bits of the MAC address are preserved and become the last 24 bits of the autoconfigured IPv6 address**. **The first 24 bits of the MAC address have the seventh bit inverted.** Also, the "**fffe**" sequence is appended to the end of the modified first 24 bits of the MAC address. **This new 40-bit structure is followed by the last 24 bits of the MAC address to form the IPv6 interface ID.**
----------
On a **Cisco switch**, which two commands would you use to **identify ports that are configured as trunks**? (Choose two.)

* **show interfaces status**
* show interfaces summary
* **show interfaces trunk**
* show ip interface brief
* show vlan brief
----------
**On a Cisco switch, why should you change the default native VLAN configuration of a trunk port?**

* It disables the Dynamic Trunking Protocol (DTP) capability on a port.
* **It leaves the network vulnerable to VLAN hopping attacks from any access port also in the default VLAN.**
* Letting all traffic flow through the default VLAN leads to an increased number of collision domains.
* It can cause frames to loop when sending a double-tagged frame.
----------
Which of the following network devices defines a **broadcast domain and a collision domain on every one of its ports?**

* bridge
* hub
* **router**
* switch
----------
**What is the purpose of a Layer 3 switch?**

* **to route traffic between company VLANs**
* to route traffic between the company network and the internet
* to route traffic between multiple geographical locations
* to route traffic between different protocol networks

Answer
The correct answer is to **route traffic between company VLANs**. Routers route traffic between the company network and the internet, as well as between different geographical networks. Multiprotocol routers provide routing between different networks with different protocols.
----------
Which **three Wi-Fi standards support the 5 GHz spectrum?** (Choose three.)

* **802.11a**
* **802.11ac**
* 802.11b
* 802.11g
* **802.11n**
----------
What is the **benefit of Mobility Express wireless access points (APs)?**

* multiple SSIDs
* multiple VLANs
* Quality of Service (QoS)
* **reduced initial cost**
----------
Which **cloud service model offers customers the most control over their cloud-hosted services?**

* Function as a Service (FaaS)
* **Infrastructure as a Service (IaaS)**
* Platform as a Service (PaaS)
* Software as a Service (SaaS)
----------
Refer to the exhibit. **PC_A wants to communicate with PC_B, which resides on a different network.** The hosts **are connected via a router that acts as the default gateway for both**. The **ARP tables on all three devices are empty. When PC_A sends the first frame, which two things happen in the process?** (Choose two.)

* PC_A broadcasts the frame intended for PC_B.
* **PC_A sends a broadcast ARP request looking for the MAC address of the router.**
* **The router adds an IPv4 address to the MAC address's mapping for PC_A to its ARP table.**
* The router drops the packet after checking for the mapping of PC_B's IP address.
* The router receives a frame with its own MAC and mismatched IP address, and drops it.
----------
Which three **IPv4 addresses are private?** (Choose three.)

* **10.255.255.254**
* **172.31.255.254**
* 172.32.255.254
* **192.168.1.100**
* 192.169.1.100

Answer
The correct answers are **10.255.255.254, 172.31.255.254, and 192.168.1.100.** These ranges of IP addresses are **private: 10.0.0.0 to 10.255.255.255, 172.16.0.0 to 172.31.255.255, and 192.168.0.0 to 192.168.255.255.** Addresses in these ranges are not routed on the internet backbone.
----------
A device running a Windows OS has the IP address **169.254.254.254**. Which of the following statements is true?

* **The address is automatically configured by the device itself.**
* The device is reachable via the internet.
* The IP address is used to communicate with the default gateway.
* The IP address is a loopback address.
----------
The **copper cabling used in your network is too close to electrical interferences.** Consequently, the **interface statistics show an unusually large number of compromised frames**. While you **attempt to solve the issue, which frame forwarding method should you implement on the Cisco switches in order to lower the number of compromised frames?**

* cut-through
* express forwarding
* process switching
* **store-and-forward**
----------
If you want to use a **static route as a backup route when the primary route fails,** which feature of the **static route will you have to change?**

* **administrative distance**
* default gateway
* IP address
* neighbor discovery
----------
On a **Cisco router, which command should you use to display the IPv6 routing table?**

* show ipv6 neighbors
* show ipv6 protocols
* **show ipv6 route**
* show ipv6 router
----------
Which of the following is the correct binary representation of the third octet of the IPv4 address 172.20.**170**.50?

* 0001 1110
* 0110 0110
* **1010 1010**
* 1100 1011
----------
When using a **AAA server along with an access switch, which two features benefit from centralized authentication**? (Choose two.)

* IPsec VPN access
* **management access**
* **network access**
* network telemetry authentication
* spanning tree authentication

Answer
The correct answers are **management access** and **network access**. By having a switch communicating to an authentication server, it is possible to authenticate a user's network access using 802.1X or other methods. It is also possible to authenticate administrative management sessions, such as SSH or HTTPs remote sessions.
----------
When an access port is enabled with the **PortFast feature, which two STP states are bypassed**? (Choose two.)

* administratively down
* blocking
* forwarding
* **learning**
* **listening**
----------
In Cisco **PVST+, how many root ports per VLAN are allowed on a device?**

* **1**
* 8
* 24
* 32
----------
What are the **default OSPF hello and dead timer values on point-to-point links?**

Hello value is 10 seconds, dead value is 20 seconds.
**Hello value is 10 seconds, dead value is 40 seconds.**
Hello value is 20 seconds, dead value is 50 seconds.
Hello value is 30 seconds, dead value is 120 seconds.
----------
After a **designated router (DR) and backup designated router (BDR) are selected on the multi-access segment** in an OSPF routing domain, **what is the OSPF state of the routers that are not elected as DR or BDR?**

* **2-way**
* exchange
* full
* loading

Answer
The correct answer is **2-way**. **Among the routers on a LAN that are not elected as the DR or BDR, the exchange process stops at this point, and the routers remain in the 2-way state.** The **master/slave routers exchange one or more database description (DBD) packets that contain a link-state database (LSDB) summary, and they are in the exchange state**. When routers start sending link-state requests (LSRs), they are in the loading state. When all LSRs have been satisfied for a given router, the adjacent routers are considered synchronized and are in the full state.
----------
Where in the **network should you implement QoS packet classification?**

* **at the input interface of a device at the LAN access edge of the network**
* at the input interface of a device at the WAN edge of the network
* at the output interface of a device at the LAN access edge of the network
* at the output interface of a device at the WAN edge of the network
----------
Which statement is true regarding **subnet 192.168.1.64/26?**

* The broadcast address of this subnet is 192.168.1.95.
* The subnet supports 126 host addresses.
* The valid subnet mask for this subnet is 255.255.255.224. 
* **There are 6 bits available for addressing hosts.**

Answer
The correct answer **is There are 6 bits available for addressing hosts**. With 6 bits available for host addressing, you can address 62 hosts. In **order to address 126 hosts**, the **maximum prefix would have to be /25.** The **subnet mask of 255.255.255.224 is represented by the /27 prefix.**
----------
Which statement about the **HTTP PUT request method is correct**?

* HTTP PUT creates a new resource.
* HTTP PUT resends received requests.
* HTTP PUT retrieves a representation of a resource.
* HTTP PUT retrieves resource headers.
* **HTTP PUT updates or modifies an existing resource.**
----------
What is the **interface ID of the IPv6 address 2001:db8::a:a9cd:47ff:fe57:fe94/64?**

* 47ff:fe57:fe94
* a:a9cd:47ff:fe57:fe94
* **a9cd:47ff:fe57:fe94**
* fe57:fe94
* 2001:db8
* 2001:db8::a

Answer
The correct answer is a9cd:47ff:fe57:fe94. An **IPv6 address starting with the hexadecimal digits 2 or 3 falls into the category of global unicast addresses.** The **first 48 bits represent the Global Routing Prefix** and are **followed by a 16-bit Subnet ID.** The **remaining 64 bits represent the Interface ID, which is equivalent to the host portion of an IPv4 address.**
----------
Presuming **there are no specific obstacles on locations where you are setting up a WLAN network, for which location should you use a patch antenna?**

* a big laboratory
* a group of small offices
* a large meeting room
* **a warehouse rack**

Answer
The correct answer is **a warehouse rack**. A **patch antenna propagates the signal in one direction and is typically used for long hallways and warehouse racks**. For **wider areas, omni-directional antennas are recommended, because they propagate the signal in all directions, covering the 360-degree field.**
----------
When is an architecture design called a **"collapsed core architecture"**?

* **When the core and the distribution layer are merged into one layer.**
* When the core layer fails to provide fault tolerance.
* When the backbone and the access layer are merged into one layer.
* When the distribution and access layer are merged into the core layer.

Answer
The correct answer is **When the core and the distribution layer are merged into one layer.** **In smaller networks, core and distribution layers are often combined in order to reduce cost**. Collapsed core is the name for a network architecture and does not indicate the lack of a feature. The backbone layer is a synonym for the core layer. An access layer can only be combined with the distribution layer. In a collapsed core architecture, there are two distinctive layers and not only one.
----------
What does a switch on an **Ethernet network do if it receives a unicast frame with the destination MAC address that resides at the same switch port as the source frame?**

* block the frame
* **drop the frame**
* flood the frame
* forward the frame
----------
Which is the **correct subnet mask for a host route?**

* 0.0.0.0
* 255.254.0.0
* 255.255.255.254
* **255.255.255.255**

Answer
The correct answer is **255.255.255.255.** The host **route is a static route for a single host**. A single host is specified by the subnet mask of 255.255.255.255. **The host route has all the bits in the network mask set to 1, for IPv4 this can be 192.168.1.1/32, and for IPv6 it could be ::1/128.**
----------
You are configuring an **IPv6 static route using the link-local IPv6 address as the next-hop**. Which command has the correct syntax?

* ipv6 route 2001:0db8:beef:: 2001:0db8:feed::1
* ipv6 route 2001:0db8:beef:: fa1/0 fe80::2
* ipv6 route 2001:0db8:beef::/32 2001:0db8:feed::1
* **ipv6 route 2001:0db8:beef::/32 fa1/0 fe80::2**

Answer
The correct answer is **ipv6 route 2001:0db8:beef::/32 fa1/0 fe80::2**. A **static route gives an option for the link-local next hop address, which is specified with the "fe80" prefix**. When using a link-local address as the next hop, **you must use an exit interface, as this link-local address can be used on any interface. "2001:0db8:feed::1" shows a route to the network that points to the global IPv6 address**. **The answers ipv6 route 2001:0db8:beef:: 2001:0db8:feed::1 and ipv6 route 2001:0db8:beef:: fa1/0 fe80::2 are missing prefixes.**
----------
Which IPv6 **command on a Cisco router can be used to provide the name-to-IP address resolution in case the DNS service in the network fails?**

* hostname TFTP-SERVER 2001:db8:a:a::69
* ipv6 host TFTP-SERVER interface Gi0/0
* **ipv6 host TFTP-SERVER 2001:db8:a:a::69 2001:db8:a:a::169**
* ipv6 hostname TFTP-SERVER 2001:db8:a:a::69

Answer
The correct answer is **ipv6 host TFTP-SERVER 2001:db8:a:a::69 2001:db8:a:a::169**. To define a static host name to address mapping in the host name cache, use the ipv6 host name [port] ipv6-address command in global configuration mode. The syntax of the command requires that you enter the host's name followed by one or more associated IPv6 addresses. Optionally, you can specify the port number. To remove the hostname-to-address mapping, use the no form of this command.
----------
Which part of the **Open Shortest Path First (OSPF) process is omitted if two routers are connected with a point-to-point link?**

* **Designated router/Border designated router (DR/BDR) election**
* exchange of hello packets
* exchange of link-state database (LSDB) summary
* Shortest Path First (SPF) calculation
----------

----------

----------

----------

----------

----------

----------

----------

----------

----------

----------

----------

----------

----------

----------

----------

----------

----------

----------

----------

----------

----------
