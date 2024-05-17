--------- 1 -----------
The devices in the topology are pre-configured with IP addressing and can communicate with each other. You need to configure and verify the time-related configuration which will allow devices to synchronize time in a pre-determined way.

Perform the following tasks:

Examine the current NTP and time zone configuration on the devices.

Configure R1 as the NTP master with stratum = 1.

Configure R2 and SW to synchronize time directly with R1.

Ans Begins:
-----------

Step 1: Configure R1 as a ntp master

R1# show clock
R1# show ntp status
R1# conf t
R1# ntp master << <1-15>  Stratum number >>
R1# end
R1# write memor -> << to save it to `running-config startup-config` >>
R1# show ntp status

R1#show ip interface brief -> to show the router ip address

Step2: Configure R2 and SW as a ntp client machine

R2# conf t
R2# ntp peer ip 198.51.100.2 => << syntax is ntp peer ip ntp master ip address >>
R2# end
R2# write memory

SW# conf t
SW# ntp peer ip 198.51.100.2 => << syntax is ntp peer ip ntp master ip address >>
SW# end
SW# write memory

Wait for some time to check the startum value of the R2.


After configuring R2 and SW to synchronize their clocks directly to R1, what are the stratum levels of R2 and SW?

Ans: 
   R2# show ntp status
   SW# show ntp status

   The correct answer is The R2 stratum level is 2 and the SW stratum level is 2. Because both R2 and SW are synchronizing time directly with R1, they both have the same stratum value. **Because R1 has a stratum value of 1, R2 and SW increment their values by one (to 2).**

What is the maximum stratum level that you can configure on a Cisco device?

Ans:
   R2# conf t
   R2# ntp master ? it will display the allowed startum value.
   15

On the SW switch, display the established NTP associations. What is the value displayed in the address column?

Ans:
   SW# show ntp associations

   The correct answer is __*~198.51.100.2__. An asterisk (*) next to a configured peer represents that the device is synced to this peer and using it as the master clock. A tilde (~) next to a configured peer represents that this is a configured master server.
--
------------- 1 ends -----------

------------- 2 -----------

The network switches must be configured to separate workstations and servers into different VLANs as displayed in the topology. To ensure inter-VLAN connectivity, router R1 is already pre-configured.

Ensure that the devices in one VLAN can communicate with each other. Perform the following tasks:

Configure IPv4 addressing on workstations and servers so that they belong to the appropriate subnet.

Configure the default gateway IPv4 address on workstations and servers.

Configure VLANs and trunking.

Do not change the default configuration on the Ethernet0/3 interface on SW2.

When configuring devices and verifying device configurations, use the information provided in the documentation, that is in the topology figure and Job Aids.


Configuration Steps:

R1#show ip interface  brief
Interface                  IP-Address      OK? Method Status                Protocol
Ethernet0/0                unassigned      YES NVRAM  up                    up      
Ethernet0/0.65             192.168.65.254  YES NVRAM  up                    up      
Ethernet0/0.80             192.168.80.254  YES NVRAM  up                    up   

Lets assume:

   Create the vlan 65 and 80 on SW1 and SW2

SW1# conf t
SW1# int eth0/1
SW1# switchport mode trunk
SW1# switchport trunk allowed vlan 65




VLAN - 65
PC1 - Eth0/0 - 192.168.65.11 - SW1 eth0/1

PC2 - Eth0/0 - 192.168.65.12 - SW2 eth0/1



SW1# conf t
SW1# int eth0/1
SW1# switchport mode trunk
SW1# switchport trunk allowed vlan 80


VLAN - 80
SV1 - Eth0/0 - 192.168.65.21 - SW1 eth0/2

SV2 - Eth0/0 - 192.168.65.22 - SW2 eth0/2


then finally try to ping each others.


When you examine the MAC address table on SW2, which VLAN does MAC aa-aa-aa-aa-22-22 belong to?

Answer
The correct answer is 65. The MAC address aa-aa-aa-aa-22-22 belongs to PC2 and as such is a member of VLAN 65. VLAN 80 contains both server nodes. VLAN 1001 is not present in this lab topology and VLAN 1005 is a reserved FDDI/Token Ring VLAN.


On SW2, verify the administrative and operational switching modes on interface Ethernet0/3. Which statement correctly describes the administrative mode and operational mode values?

**show interface eth0/3 switchport**

show 
Answer:
   The correct answer is Administrative mode is dynamic-desirable and operational mode is trunk. Administrative mode displays what you have configured on the interface. Operational mode displays the actual status of the interface. 

   **When manually configuring access or trunking, administrative and operational mode have identical values. When you configure Dynamic Trunking Protocol (DTP) to negotiate switching status, administrative and operational mode differ. Cisco recommends disabling DTP on a switch."**

Examine the topology and the configuration. On PC2, when you use the ping command to check connectivity to Server 1, what is the order of the devices that packets traverse?

   Ans: **PC2 > SW2 > SW1 > R1 > SW1 > Server1**


Which interfaces on SW1 are trunk interfaces?

Answer
The correct answer is E0/0 and E0/3. SW1 has four interfaces. The interfaces E0/0 and E0/3 are connected to a router and another switch, respectively. As such, those two interfaces are set up as trunk interfaces in order to carry multiple VLANs. The interfaces E0/1 and E0/2 are connected to end nodes, and are configured as access interfaces.

------------- 2 ends -----------

------------- 3 begins -----------


In this task you will configure link aggregation and examine its effects on STP topology. The network devices are pre-configured with basic connectivity parameters and Rapid Per VLAN Spanning Tree Protocol Plus (Rapid PVSTP+) to prevent traffic loops. The topology consists of three segments: workstations, servers, and connecting segment. All devices have their basic configurations in place, including hostnames and IP addresses.

Carefully examine the device configurations. There are some mistakes in the interface configuration on network devices. First, find the mistakes and correct them. Then, perform the following configuration tasks, and answer the questions.

Create EtherChannel links between the switches using the Link Aggregation Control Protocol (LACP).

Configure the switches so SW3 is the root switch for VLAN 20 and SW1 is the root switch for VLAN 10.

Ensure there is full connectivity within each VLAN (that is, you can successfully issue the ping command between PC1 and PC2, between SRV1 and SRV2, and between switches).



**1. Create EtherChannel links between the switches using the Link Aggregation Control Protocol (LACP).**

EtherChannel is a port link aggregation technology developed by Cisco, allowing the grouping of several physical Ethernet links to create a single logical Ethernet link for increased bandwidth and redundancy. LACP (Link Aggregation Control Protocol) is part of the IEEE specification (802.3ad) that allows for automatic creation of EtherChannels by exchanging LACP packets between switches.

Let's say you want to create an EtherChannel between two Cisco switches, SW1 and SW2, using LACP. Here are the steps to configure LACP for EtherChannel on Cisco switches:


### Configure LACP on Cisco Switch SW1

1. **Enter Global Configuration Mode**:
   ```
   SW1> enable
   SW1# configure terminal
   SW1(config)#
   ```

2. **Navigate to the Interface Range Configuration Mode**:
   Select the interfaces that you want to add to the EtherChannel. For example, if you're aggregating GigabitEthernet ports 0/1 and 0/2:
   ```
   SW1(config)# interface range GigabitEthernet0/1 - 2
   ```

3. **Configure the Interfaces for LACP**:
   Assign the physical interfaces to an EtherChannel group using LACP. The channel-group number is arbitrary but must match on both switches.
   ```
   SW1(config-if-range)# channel-group 1 mode active
   ```
   The `active` keyword enables LACP unconditionally.

4. **Assign a Port-Channel Interface**:
   This step is done automatically by the switch when the channel-group command is given, but you can configure settings for the logical interface as well.
   ```
   SW1(config)# interface Port-channel1
   SW1(config-if)# switchport mode trunk  (Optional, if you want to configure it as a trunk)
   ```

5. **Exit Configuration Mode**:
   ```
   SW1(config-if)# end
   SW1# write memory
   ```
   or
   ```
   SW1# copy running-config startup-config
   ```


### Verify the EtherChannel Configuration

1. **Check the EtherChannel Summary**:
   Use the `show etherchannel summary` command on both switches to verify the status of the EtherChannel.
   ```
   SW1# show etherchannel summary
   SW2# show etherchannel summary
   ```
   Look for the `Port-channel` you created, and ensure that the status is `P` (bundled in the port-channel).

2. **Check the LACP Configuration**:
   You can also verify that LACP is configured correctly with the following command:
   ```
   SW1# show lacp neighbor
   SW2# show lacp neighbor
   ```

By following these steps, you should have successfully configured an LACP EtherChannel between two Cisco switches. Remember that the physical ports included in the EtherChannel should have the same configuration (speed, duplex, and switchport mode). If there's a mismatch, the ports will not successfully bundle into the EtherChannel.



**2. Configure the switches so SW3 is the root switch for VLAN 20 and SW1 is the root switch for VLAN 10.**

To configure Spanning Tree Protocol (STP) so that SW3 is the root switch for VLAN 20 and SW1 is the root switch for VLAN 10, you will need to adjust the bridge priority values for these VLANs on the respective switches. Lower bridge priority values result in a switch being more likely to be elected as the root.

### Configure SW3 as Root Switch for VLAN 20

1. **Enter Global Configuration Mode on SW3**:
   ```
   SW3> enable
   SW3# configure terminal
   SW3(config)#
   ```

2. **Set Bridge Priority for VLAN 20**:
   Set the bridge priority to a lower value than the default (32768) to make SW3 the most likely candidate to become the root switch for VLAN 20.
   ```
   SW3(config)# spanning-tree vlan 20 priority 8192
   ```
   You can choose a value lower than 32768, such as 8192, to ensure it becomes the root bridge. Valid priority values are in increments of 4096.

3. **Exit Configuration Mode**:
   ```
   SW3(config)# end
   SW3# write memory
   ```
   or
   ```
   SW3# copy running-config startup-config
   ```

### Configure SW1 as Root Switch for VLAN 10

1. **Enter Global Configuration Mode on SW1**:
   ```
   SW1> enable
   SW1# configure terminal
   SW1(config)#
   ```

2. **Set Bridge Priority for VLAN 10**:
   Similarly, ensure SW1 has a lower priority for VLAN 10.
   ```
   SW1(config)# spanning-tree vlan 10 priority 8192
   ```

3. **Exit Configuration Mode**:
   ```
   SW1(config)# end
   SW1# write memory
   ```
   or
   ```
   SW1# copy running-config startup-config
   ```

### Verify the STP Configuration

After configuring the priorities, you should verify that SW3 is the root bridge for VLAN 20 and SW1 is the root bridge for VLAN 10.

1. **Check STP Status on SW3 for VLAN 20**:
   ```
   SW3# show spanning-tree vlan 20
   ```
   Look for the line that indicates this switch is the root, for example, "This bridge is the root".

2. **Check STP Status on SW1 for VLAN 10**:
   ```
   SW1# show spanning-tree vlan 10
   ```
   Verify that SW1 is the root by looking for the same indication.

3. **Check STP Status on Other Switches**:
   Perform similar checks on other switches to confirm that SW3 and SW1 are recognized as the root bridges for VLANs 20 and 10, respectively.

### Optional: Configure Root Guard

On ports where you expect only to see the root bridge and no other switch should become root, you can enable root guard to prevent unexpected root bridge changes.

```
SWx(config)# interface [interface-id]
SWx(config-if)# spanning-tree guard root
```

Replace `[interface-id]` with the actual interface identifier.

By following these steps, SW3 will be configured as the root switch for VLAN 20, and SW1 will be configured as the root switch for VLAN 10. Remember that STP changes can take effect over several seconds or minutes due to STP timers, so allow sufficient time for the STP topology to converge.



------------- 3 ends -----------

------------- 4 begins -----------

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

**Perform the following task:**

* Using Telnet to access R1, configure SSH with the following parameters:

* key size of 2048 bits

* domain name example.com

* login authentication must be performed against the locally stored user information

* create an entry in the local database for one user, using the username AdminPC2, maximum privilege level, and password Cisco123

Examine the access list configuration on R1:

# Qus1: From PC2, access the R1 router using SSH. Apply the configured access list so that it limits remote access to R1 to only SSH connections from PC2.


### 1. Set Hostname and Domain Name
You need to set a hostname and a domain name on the router to generate the RSA keys required for SSH.
```plaintext
R1> enable
R1# configure terminal
R1(config)# ip domain-name example.com
```

### 2. Generate RSA Keys
Generate the RSA key pair, which is used to encrypt and decrypt the SSH sessions.
```plaintext
R1(config)# crypto key generate rsa
```
You will be asked to specify the size of the key; 1024 bits is commonly used, but 2048 bits is more secure.

### 3. Create a Local User
Create a username and password for SSH authentication.
```plaintext
R1(config)# username AdminPC2 secret Cisco123
```

### 4. Enable SSH and Set SSH Version (Optional)
Enable SSH on the router and (optionally) set the SSH version. Version 2 is more secure than version 1.
```plaintext
R1(config)# ip ssh version 2
```

### 5. Configure the VTY Lines for SSH
Configure the VTY (Virtual Terminal Lines) to only accept SSH connections.
```plaintext
R1(config)# line vty 0 15
R1(config-line)# transport input ssh
R1(config-line)# login local
R1(config-line)# exit
```

### 7. Save Configuration
Save the configuration to ensure that it persists after a reboot.
```plaintext
MyRouter# write memory
or
MyRouter# copy running-config startup-config
```

### Access the Router from a PC

**For Linux:**

1. Open a terminal.
2. Use the `ssh` command to connect to the router:
```plaintext
ssh -l AdminPC2 192.168.1.1
Then enter password:
```
To check the loopback ip address use **show running-config**

# Qus2:
In the lab network, which SSHACCESS access list implementation would correctly limit remote access to only SSH connections from PC2?

**inbound direction on the vty lines on R1**

Answer
The correct answer is inbound direction on the vty lines on R1. The other proposed implementations would also limit other traffic.

# Qus3: Examine the configuration on SW2. Based on the information in the configuration, use Telnet from PC1 to access the SW2 switch. Which message is displayed upon successful access?

**Login to SW2 to get the access details before doing the telnet from PC1.**

From PC1 connect SW2 using telnet:

```plaintext
   PC1>enable
   PC1#telnet 10.10.1.3
   Trying 10.10.1.3 ... Open
   You must have permissions to access this device! If you are not authorized, do not proceed! Unauthorized access prohibited.

   User Access Verification

   Username: PC1
   Password:  **Access for authorized users only. Proceed with caution.**
   SW2>
```
**Access for authorized users only. Proceed with caution.**

------------- 4 ends -----------

------------- 5 begins -----------

The devices are pre-configured with the basic connectivity requirements.

Your task is to configure additional Layer 2 security features on a Cisco network switch.

The logging-on switch is configured so only alerts and emergencies are sent to the console.

Carefully examine the pre-existing configuration of SW1 and answer questions 1, 2, and 3. Then perform the configuration tasks and answer questions 4 and 5.

Perform the following tasks:

Configure port security on SW1 on the port that is connected to PC1 to allow the MAC addresses of the first two devices that connect to the port. If any additional devices are connected to this port, the port must drop all packets, but it must not increment the security-violation count.

Configure port security on SW1 on the ports that are connected to PC2 and the Inventory server to allow a maximum of two MAC addresses. Configure the port so it remembers the MAC addresses of the first two devices that connect to the port. If any additional devices are connected to this port, the port must drop all packets and increment the security-violation count.

# Qus 1: On SW1, what is the state of the port connecting to the Inventory server?

**Correct Answer is: err-disabled**

SW1#show interfaces eth0/3
Ethernet0/3 is down, line protocol is down (**err-disabled**) 
  Hardware is AmdP2, address is aabb.cc00.0630 (bia aabb.cc00.0630)
  Description: ***Connected to Inventory server***
  MTU 1500 bytes, BW 10000 Kbit/sec, DLY 1000 usec, 
     reliability 255/255, txload 1/255, rxload 1/255
  Encapsulation ARPA, loopback not set
  Keepalive set (10 sec)
  Auto-duplex, Auto-speed, media type is unknown
  input flow-control is off, output flow-control is unsupported 
  ARP type: ARPA, ARP Timeout 04:00:00
  Last input 00:00:02, output 00:06:14, output hang never
  Last clearing of "show interface" counters never
  Input queue: 0/2000/0/0 (size/max/drops/flushes); Total output drops: 0
  Queueing strategy: fifo
  Output queue: 0/0 (size/max)
  5 minute input rate 0 bits/sec, 0 packets/sec
  5 minute output rate 0 bits/sec, 0 packets/sec
     53 packets input, 6187 bytes, 0 no buffer
     Received 15 broadcasts (0 multicasts)
     0 runts, 0 giants, 0 throttles 
     0 input errors, 0 CRC, 0 frame, 0 overrun, 0 ignored
     0 input packets with dribble condition detected
     10 packets output, 2226 bytes, 0 underruns
     0 output errors, 0 collisions, 0 interface resets
     0 unknown protocol drops
     0 babbles, 0 late collision, 0 deferred
     0 lost carrier, 0 no carrier
     0 output buffer failures, 0 output buffers swapped out

# Qus2: From PC2, ping Ethernet0/0 interface of the Border router. What is the cause for ping to fail?

**The maximum number of sticky MACs is already reached for `switch` interface Ethernet0/2.**

# Qus3: What is the Security Violation counter for the Ethernet 0/3 interface on SW1?

SW1#show port-security interface eth0/3
Port Security              : Enabled
Port Status                : Secure-shutdown
Violation Mode             : Shutdown
Aging Time                 : 0 mins
Aging Type                 : Absolute
SecureStatic Address Aging : Disabled
Maximum MAC Addresses      : 1
Total MAC Addresses        : 1
Configured MAC Addresses   : 1
Sticky MAC Addresses       : 0
Last Source Address:Vlan   : aabb.cc00.0a00:1
**Security Violation Count**  : **1**

# Qus4: What is the port-security status of the Ethernet 0/1 interface on SW1?
After configuring the port security on SW1 on the port that is connected to PC1, what is the port-security status of the Ethernet 0/1 interface. The interface status will be **Secure-up**.

# Qus5: Verify the line protocol status of the Ethernet0/3 port on SW1. How would you correct the issue?

**Shut down and enable the interface on SW1.**

------------- 5 ends -----------

------------- 6 begins -----------

IPv4 addressing is configured on all devices.

The SW2 neighbor discovery protocol is pre-configured. Do not change the existing configuration parameters on SW2.

CDP is already configured on R2. You will not have direct access to the R2 router. **You can gain information about R2 configuration using neighbor discovery protocols on neighboring devices.**

**In this task you will discover the topology using Link Layer Discovery Protocol (LLDP) and the Cisco Discovery Protocol (CDP).** Router R2 is already pre-configured. Perform the following tasks:

Task 1:
   Examine the configurations of the SW1 and SW2 switches. Answer the first question.

Task 2:
   Configure switch SW1 and router R1 so that Layer 2 connectivity information is provided among all devices in the topology, that is: SW1, SW2, R1, and R2.

# Qus1: Examine the configurations of the switches SW1 and SW2. SW2 cannot obtain Layer 2 information from SW1 using CDP. Why?

Connect SW2 and check the cdp status.
   SW2#show cdp
   % CDP is not enabled
   SW2#

**because CDP is globally disabled on SW2**

When the CDP is enabled on a device:
   SW1#show cdp
   Global CDP information:
         Sending CDP packets every 60 seconds
         Sending a holdtime value of 180 seconds
         Sending CDPv2 advertisements is enabled
   SW1# 

# Qus2: What is the IP address of the R2 interface connecting to R1?

   The correct answer is 192.168.3.2. By issuing the show cdp neighbors detail command on R1, you are able to get the IPv4 address of R2’s interface connecting to R1.

**R1#show cdp neighbors detail**
**% CDP is not enabled**
R1#conf t
Enter configuration commands, one per line.  End with CNTL/Z.
**R1(config)#cdp run**
R1(config)#end
R1#wr 
Building configuration...

*May 17 07:38:45.007: %SYS-5-CONFIG_I: Configured from console by console[OK]
**R1#show cdp neighbors detail**
-------------------------
Device ID: **R2**
Entry address(es): 
  IP address: **192.168.3.2**
Platform: Linux Unix,  Capabilities: Router 
Interface: Ethernet0/1,  Port ID (outgoing port): Ethernet0/0
Holdtime : 171 sec

Version :
Cisco IOS Software, Linux Software (I86BI_LINUX-ADVENTERPRISEK9-M), Version 15.2(4)M3, DEVELOPMENT TEST SOFTWARE
Technical Support: http://www.cisco.com/techsupport
Copyright (c) 1986-2013 by Cisco Systems, Inc.
Compiled Tue 26-Feb-13 19:06 by prod_rel_team

advertisement version: 2
Duplex: half

# Qus3: What are the ports that interconnect switches SW1 and SW2?

Answer is: **SW1 Ethernet0/0 and SW2 Ethernet0/0**

Enable CDP on SW1 and SW2.

SW1#conf t
Enter configuration commands, one per line.  End with CNTL/Z.
SW1(config)#cdp run
SW1(config)#end
SW1#wr
Building configuration...
Compressed configuration from 922 bytes to 639 bytes[OK]
SW1#
*May 17 07:42:24.906: %SYS-5-CONFIG_I: Configured from console by console
**SW1#show cdp neighbors detail**
-------------------------
**Device ID: SW2**
Entry address(es): 
  IP address: 10.10.1.3
Platform: Linux Unix,  Capabilities: Switch IGMP 
Interface: Ethernet0/0,  Port ID (outgoing port): **Ethernet0/0**
Holdtime : 156 sec


**SW2#show cdp neighbors detail**
-------------------------
Device ID: **SW1**
Entry address(es): 
  IP address: 10.10.1.2
Platform: Linux Unix,  Capabilities: Switch IGMP 
Interface: Ethernet0/0,  Port ID (outgoing port): **Ethernet0/0**
Holdtime : 175 sec

-------------------------
**Device ID: R1**
Entry address(es): 
  IP address: 10.10.1.1
Platform: Linux Unix,  Capabilities: Router 
Interface: Ethernet0/1,  Port ID (outgoing port): **Ethernet0/0**
Holdtime : 169 sec

# Qus3: In the topology you discovered in this exercise, can R1 obtain information about SW1 using CDP?

Answer is: **No, because R1 and SW1 are not directly connected.**

**SW1#show cdp neighbors detail**
-------------------------
**Device ID: SW2**
Entry address(es): 
  IP address: 10.10.1.3
Platform: Linux Unix,  Capabilities: Switch IGMP 
Interface: Ethernet0/0,  Port ID (outgoing port): **Ethernet0/0**
Holdtime : 156 sec
----------

------------- 6 ends -----------

------------- 7 begins -----------




You have been given the task of administering a network that is running dynamic routing protocols, in this case the OSPFv2 routing protocol. The previous administrator has already configured OSPF on R4, as well as the parameters for the election of the designated router and the backup designated router in the multi-access segment.

In order to complete the routing configuration in the network, perform the following tasks:

Enable OSPF for routing information exchange on routers R1, R2, and R3. Use the following router IDs:

R1: 1.1.1.1

R2: 2.2.2.2

R3: 3.3.3.3

On R1, configure OSPF so that it advertises its default route to other OSPF-enabled routers.

Verify the routing tables on all routers. The routes to all networks should be visible on all routers to establish full connectivity.

# Qus1: Examine the OSPF configurations on routers in the multi-access segment, that is R1, R2, and R3. OSPF priority has been pre-configured on all routers. If all the routers would reboot at the same moment, which two routers would be elected as Designated Router (DR) and Backup Designated Router (BDR)?

Correct Ans: **R1 is DR and R3 is BDR.**

# Qus2: What are the OSPF hello and dead timer values on R2?

Correct Ans: **Hello is 10 seconds and dead is 40 seconds.**

# Qus3: In the routing table on R2, what is the protocol code for the default route?

Correct Ans: **O*E2**

# Qus4: The R4 router is not participating in OSPF. What is causing the issue?
Correct Ans: **The OSPF area is configured incorrectly on R4.**

------------- 7 ends -----------

------------- 8 begins -----------



Consult the topology diagram and address table to understand the network connectivity and addressing. Not all systems are initially configured with IPv6 addresses. OSPFv3 is configured between routers.

Perform the following tasks:

Configure SRV1 (Ethernet0/0) with the IPv6 address that is the first available after the address assigned to SW3. Make sure that the ping from SRV1 to the R3 Ethernet0/0 is successful.

Configure PC1 and PC2 to auto-configure both their IPv6 addresses and their default gateways. The ping from PC1 to PC2 should be successful.

Configure the SW1 and SW2 IPv6 addresses and default gateways as listed in the Job Aids.

Configure the routers with link-local addresses so that each interface on a router has the same link-local address.

For R1, use fe80::1.

For R2, use fe80::2.

For R3, use fe80::3.

Pending tasks are below

# Qus1: Which command is used to assign IPv6 addresses to PC1 and PC2?

Correct Ans: **ipv6 address autoconfig default**


# Qus2: Which IPv6 address is assigned to the SRV1 server?

Correct Ans: **2001:db8:0:3::31/64**

# Qus3: Use the show ipv6 route command, examine the routing table on the R1 router. What is the next-hop IPv6 address to the 2001:db8:0:2::/64 network?

Correct Ans: **fe80::2**

# Qus4: Use the shutdown command, disable the R2 Ethernet0/2 interface. What is the next-hop IPv6 address to the 2001:DB8:0:2::/64 network when examining the IPv6 routing table on the R1 router?

Correct Ans: **fe80::3**

# Qus5: What is the IPv6 default gateway address for the SW2 switch?

Correct Ans: **2001:db8:0:2::2**

Run **`show running-config`** command on R2 which is connected with SW2. **The R2 IPv6 address is the default gateway for SW2.**
R2#show run
Building configuration...
interface Ethernet0/0
 description Link to SW2
 ip address 10.10.2.1 255.255.255.0
 ipv6 address 2001:DB8:0:2::2/64
 ospfv3 1 ipv6 area 0

------------- 8 ends -----------

------------- 9 begins -----------
Devices in the IT department are pre-configured.

Router R2 is a DHCP server and provides IP addresses to multiple network segments in Department A.

End clients in department A need to be configured so that they receive all relevant network configuration through DHCP. However, router R1 is not yet configured to facilitate this operation.

Perform the following tasks:

Configure router R1 so that the PC1 and PC2 hosts get DHCP information from router R2.

Ensure that both PC1 and PC2 hosts get their addresses via DHCP.

# Qus1: What is the default gateway that PC1 has received through DHCP?

* 10.10.1.1
* **10.10.1.53**
* 10.10.1.100
* 10.10.1.254

Answer
The correct answer is 10.10.1.53. In real networks, **the gateway address is usually either the first or the last assignable IP address of the subnet.**

# Qus2: What is the lease time for the assigned IP address on PC2?


* 1 second


* **1 minute**


* 1 hour


* 1 day



# Qus3: What is the IPv4 address of the DNS server assigned by DHCP to PC1?


* 10.10.1.1


* 198.51.100.1


* 203.0.113.1


* **203.0.113.30**

------------- 9 ends -----------





Perform the following tasks:





------------- 4 begins -----------

The lab is prepared with the devices that are represented in the topology diagram. All devices have their basic configurations in place, including hostnames and IP addresses. Static routing is configured on all devices.


On R1, configure port forwarding so that Telnet connections to SRV1 are possible from outside networks. For the public IPv4 address, use the IPv4 address of the Ethernet 0/3 interface. For the publicly accessible port, use 2323.

Ensure that traffic from the 10.10.2.0/24 subnet is dynamically translated, using the following pool of public addresses: 209.165.202.128/27.

Ensure that traffic from the 10.10.1.0/24 subnet is translated to the IPv4 address of the Ethernet 0/3 interface on R1.


------------- 4 ends -----------

------------- 5 begins -----------


This lab tests your knowledge about basic security configuration of the device management plane. IP addressing on all devices is already configured.

The SW2 switch in the topology has already been configured. You will have no direct access to this device, however, you can access it remotely from other devices in the topology.

SW2 already has a local database of user credentials. The Device Access table provides detailed information.

In the task, you will configure the SW1 switch and the R1 router.

On SW1, perform the following tasks:

Restrict access to the privileged EXEC mode. Configure the protected password CiscoSW1! using the default encryption type. Configure the unprotected password Cisco123! and ensure it is obfuscated in the configuration file (that is, it does not show in the plain text).

Define two users in the local database, using the following credentials:

username => password => privilege level
TECH => CiscoTech1! => default
ADMIN => CiscoAdm1! => 15


On R1, perform the following tasks:

Restrict access to the privileged EXEC mode. Configure the protected password CiscoR1! using the default encryption type.

Configure the unprotected password Cisco123! and ensure it is obfuscated in the configuration file.

Protect the access to the console by requiring a password to access the console. Set the console password to Cisco333!.


enable secret cisco

enable password cisco

username admin secret cisco


------------- 5 ends -----------
