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


Which four of the following are valid link-local IPv6 addresses? (Choose four.)
* fe80::1
* ff80::1
* fe90::1
* feb1::1
* fea3::1
* fec3::1

	* fe80::1
	* fe90::1
	* feb1::1
	* fea3::1
	-
	All addresses encompassed by the fe80::/10 prefix are considered valid link-local IPv6 addresses. The ff00::/8 prefix is the prefix of multicast IPv6 addresses. Addresses starting with the hexadecimal digits fec3 do not belong to a link-local IPv6 address range.
--------

Which APIs are used for communication between a software-defined networking (SDN) application and a controller?
* Eastbound APIs
* Northbound APIs
* Southbound APIs
* Westbound APIs

	Northbound APIs
	-
	Northbound APIs or northbound interfaces are responsible for the communication between the SDN controller and the services that run over the network. Northbound APIs enable your applications to manage and control the network. Therefore, rather than adjusting and tweaking your network repeatedly to get a service or application running correctly, you can set up a framework that allows the application to demand the network setup that it needs.


----------

Refer to the exhibit. Which two options are common **IPsec or SSL VPN** implementations? (Choose two.)



option 1


option 2


option 3


option 4


option 5


Answer
The correct answers are option 1 and option 5. An IPsec Tunnel VPN is typically established between two network devices, connecting two or more remote networks. An SSL VPN is typically established between a client and a network device. DMVPN and IPsec VTI VPN are typically established between network devices.

--------

What are two valid IPv6 address scopes for a unique local IPv6 address? (Choose two.)


global


interface-local


link-local


organization-local


site-local

Answer
The correct answers are organization-local and site-local. Unique local IPv6 addresses are equivalents of private IPv4 addresses. They can be considered globally unique, because the probability of duplication is extremely low. Unique local IPv6 addresses are routable inside of a limited area, such as a site. Also, unique local IPv6 addresses may be routed between a limited set of sites (within an organization), but are not expected to be routable on the global internet.

---------

When a particular VLAN is deleted, what happens to interfaces that were assigned to the deleted VLAN?

The correct answer is They become inactive. 

----------

On a Cisco switch, which two commands would you use to identify ports that are configured as trunks? (Choose two.)

The correct answers are show interfaces status and show interfaces trunk

-----------

When an enterprise has to comply with strict data security regulations, which cloud deployment model should they use for their services?

The correct answer is private.

-----------

Which command is used to verify a default gateway configuration on a Layer 2 switch?

The correct answers is show running-config


------

On SW2, verify the administrative and operational switching modes on interface Ethernet0/3. Which statement correctly describes the administrative mode and operational mode values?


Administrative mode is access and operational mode is access.


Administrative mode is dynamic-auto and operational mode is access.


Administrative mode is dynamic-desirable and operational mode is access.


Administrative mode is dynamic-desirable and operational mode is trunk.


Administrative mode is trunk and operational mode is trunk.

Answer
The correct answer is Administrative mode is dynamic-desirable and operational mode is trunk. Administrative mode displays what you have configured on the interface. Operational mode displays the actual status of the interface. When manually configuring access or trunking, administrative and operational mode have identical values.

--------

Which three statements about IPv4 addresses are true? (Choose three.)

Answer
The correct answers are 8.0.0.0 is a public address, 10.8.0.0 is a private address, and 127.0.0.1 is a reserved address. 192.170.0.0 is a public IPv4 address, and 172.30.0.0 is a private IPv4 address.

--------

What is the maximum cable length of an unshielded twisted-pair (UTP) cable that still guarantees full connectivity?

Answer
The correct answer is 100 m. Maximum UTP cable length is limited due to physical limitations of copper wires, where signal strength degrades with distance.

------

When creating and maintaining the MAC address table, which two activities does a switch perform? (Choose two.)

Answer
The correct answers are It adds the source MAC address in the frame and the incoming port number and It resets the aging time of the MAC table entry for the source MAC address. A switch uses the destination MAC address to decide whether to forward or flood a frame. The destination MAC address is not stored in the MAC address table. The aging timer is reset for the source MAC address entry each time the switch receives a frame from that source MAC address.

-------

When a router is calculating the network portion of an IPv4 address, which bitwise operation is performed on the IPv4 address and the subnet mask?

Ans: AND operation

--------

When an access port is enabled with the PortFast feature, which two STP states are bypassed? (Choose two.)

Ans: learning and listening
---------------
If a port is still a designated or root port at the end of the learning state, which state will it enter?
* blocking
* disabled
* **forwarding**
* learning
* listening

	forwarding
	-
	This port sends and receives all data frames on the bridged port. A blocked port only listens to BPDUs (Bridge Protocol Data Units), and it does not forward any frames. Disabled ports do not participate in frame forwarding. A port changes to a learning state after a listening state. After a blocking state, the designated port moves to a listening state.
-------

If a port is still a designated or root port at the end of the learning state, which state will it enter?


The correct answer is forwarding. This port sends and receives all data frames on the bridged port. A blocked port only listens to BPDUs (Bridge Protocol Data Units), and it does not forward any frames. Disabled ports do not participate in frame forwarding. A port changes to a learning state after a listening state. After a blocking state, the designated port moves to a listening state.


-------

Lab with EthernetChannel:

Q1. On SW4, which port is the STP root port for VLAN 20?

Answer
The correct answer is Po34. SW3 is the root bridge for VLAN 20. SW4 is connected to SW3 via aggregated links represented by interfaces Po14, Po24, and Po34. After verifying the STP status for VLAN 20, you can see that the Po34 interface has the shortest path, hence the lowest cost and is elected as the root port.

Q2. On SW2, when you see the summary information for aggregated link. What is the status code or flags of the port channel Po23?

Answer
The correct answer is Layer2 - In use (SU). When you use the show etherchannel summary command, the SU Status code signifies that the aggregated channel is Layer 2 channel and that it is active.

Q3. Issue the ping command from PC1 to PC2. What is the path that packets traverse?

Answer
The correct answer is SW1 > SW3 > SW2. This is the resulting path of VLAN 10 after STP calculations are performed, taking aggregated links into consideration.

Q4. Refer to the exhibit. The figure represents the topology resulting from STP calculations after configuring the Layer 2 EtherChannel. Which VLAN does the topology in the exhibit represent?

Answer
The correct answer is VLAN 20. When you use the show spanning-tree command on a switch, the output displays STP information for each VLAN, including the STP root bridge election results and port designations.

---------


Character - Description
! - Each exclamation point indicates receipt of a reply.
. - Each period indicates the network server timed out while waiting for a reply.
U - A destination unreachable error PDU was received.
C - A congestion experienced packet was received.
I - User interrupted test.
? - Unknown packet type.
& - Packet lifetime exceeded.

--------

Level Keyword => Level => Description => Syslog Definition
emergencies => 0 => System unstable => LOG_EMERG
alerts => 1 => Immediate action needed => LOG_ALERT
critical => 2 => Critical conditions => LOG_CRIT
errors => 3 => Error conditions => LOG_ERR
warnings => 4 => Warning conditions => LOG_WARNING
notifications => 5 => Normal but significant condition => LOG_NOTICE
informational => 6 => Informational messages only => LOG_INFO
debugging => 7 => Debugging messages => LOG_DEBUG

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

What is the maximum cable length of an unshielded twisted-pair (UTP) cable that still guarantees full connectivity?
* 80 m
* **100 m**
* 120 m
* 150 m

---------
Which component is used to generate a signal for single-mode fiber connections?
* cathode
* **laser transmitter**
* LED diode
* oscillator

	**laser transmitter**

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
Which task makes configuring network devices more efficient and reduces errors?

* compliance checks
* data collection and telemetry
* **device provisioning**
* device software management

	device provisioning
---------

Which two characteristics apply to small office/home office (SOHO) routers? (Choose two.)

* They are more expensive than enterprise routers.
* They are more reliable than enterprise routers.
* **They have a web-based administration interface.**
* **They have integrated security functionality.**
* They perform intensive routing tasks.

----------

