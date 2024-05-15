1.6 Configure and verify IPv4 addressing and subnetting

  To configure and verify IPv4 addressing and subnetting on a Cisco router, you can follow these steps:

  1. Connect to your router: Use a console cable to connect to your Cisco router. 

  2. Enter the user exec mode: Once connected, you can enter the user exec mode by typing `enable` in the command line interface (CLI) and press `Enter`.

  3. Enter global configuration mode: To configure the router, you need to enter the global configuration mode. Type `configure terminal` and press `Enter`.

  4. Select the interface you want to configure: Type `interface FastEthernet 0/0` (or the appropriate interface you want to use) and press `Enter`.

  5. Configure the IP address and subnet mask for the interface: Type `ip address 192.168.1.1 255.255.255.0` (replace 192.168.1.1 and 255.255.255.0 with your desired IP address and subnet mask) and press `Enter`.

  6. Enable the interface: Type `no shutdown` and press `Enter`.

  7. Exit interface configuration mode: Type `exit` and press `Enter`.

  8. Repeat steps 4-7 for each interface you want to configure.

  9. Save your changes: To save your changes, type `write memory` or `copy running-config startup-config` and press `Enter`.

  To verify your configuration:

  1. View the IP configuration: In the privileged exec mode (type `enable` and press `Enter` if you're not already in this mode), type `show ip interface brief`. This command will display a summary of the device's interfaces, including their IP addresses and status.

  2. Check the routing table: Type `show ip route` to display the routing table and verify that the network for each interface is listed.

  Please replace the IP addresses and subnet mask in the steps with the ones suitable for your network configuration.

---------------------------------------------------------------------------------------------------------

1.8 Configure and verify IPv6 addressing and prefix

  Configuring and verifying IPv6 addressing and prefix on a Cisco router involves similar steps as with IPv4, but with a few different commands. Here's how to do it:

  1. Connect to your router: Use a console cable to connect to your Cisco router.

  2. Enter the user exec mode: Once connected, you can enter the user exec mode by typing `enable` in the command line interface (CLI) and press `Enter`.

  3. Enter global configuration mode: To configure the router, type `configure terminal` and press `Enter`.

  4. Select the interface you want to configure: Type `interface FastEthernet 0/0` (or the appropriate interface you want to use) and press `Enter`.

  5. Enable IPv6 processing on the interface: Type `ipv6 enable` and press `Enter`.

  6. Configure the IPv6 address and prefix for the interface: Type `ipv6 address 2001:0db8:85a3:0000:0000:8a2e:0370:7334/64` (replace with your desired IPv6 address and prefix length) and press `Enter`.

  7. Enable the interface: Type `no shutdown` and press `Enter`.

  8. Exit interface configuration mode: Type `exit` and press `Enter`.

  9. Repeat steps 4-8 for each interface you want to configure.

  10. Save your changes: To save your changes, type `write memory` or `copy running-config startup-config` and press `Enter`.

  To verify your configuration:

  1. View the IPv6 configuration: In the privileged exec mode (type `enable` and press `Enter` if you're not already in this mode), type `show ipv6 interface brief`. This command will display a summary of the device's interfaces, including their IPv6 addresses and status.

  2. Check the IPv6 routing table: Type `show ipv6 route` to display the IPv6 routing table and verify that the network for each interface is listed.

  Please replace the IPv6 addresses and prefix in the steps with the ones suitable for your network configuration.


---------------------------------------------------------------------------------------------------------

2.1 Configure and verify VLANs (normal range) spanning multiple switches
  2.1.a Access ports (data and voice)

    Sure, here are the steps to configure and verify VLANs spanning multiple switches and configuring access ports for data and voice:

    1. Connect to your first switch using a console cable and open your terminal program.

    2. Once connected, enter the user exec mode by typing `enable` and press `Enter`.

    3. Enter the global configuration mode by typing `configure terminal` and press `Enter`.

    4. Create a new VLAN by typing `vlan [VLAN_NUMBER]` (replace `[VLAN_NUMBER]` with your desired VLAN number between 1 and 1005). Then press `Enter`.

    5. You can optionally give the VLAN a name by typing `name [VLAN_NAME]` (replace `[VLAN_NAME]` with your desired VLAN name) and press `Enter`.

    6. Exit back to the global configuration mode by typing `exit` and press `Enter`.

    7. Assign a switchport to the VLAN by typing `interface FastEthernet0/1` (replace `FastEthernet0/1` with your desired port), then press `Enter`, followed by `switchport mode access` and `switchport access vlan [VLAN_NUMBER]`.

    8. Configure the port for voice VLAN by typing `switchport voice vlan [VOICE_VLAN_NUMBER]`.

    9. Repeat these steps for each port you want to add to the VLAN.

    10. Save your changes by typing `do write` or `do copy running-config startup-config`.

    To verify your configuration:

    1. In the privileged exec mode (type `enable` and press `Enter` if you're not already in this mode), type `show vlan brief`. This command will display a summary of the VLANs on the switch.

    2. Type `show interfaces status` to see the status and VLAN assignment of each port.

    These steps need to be repeated on each switch where you want the VLAN to exist. For the VLAN to span multiple switches, the switches need to be interconnected with trunk ports, which carry traffic from all VLANs by default.

    Remember to replace `[VLAN_NUMBER]` with the VLAN number you chose, `[VLAN_NAME]` with the name you want to give the VLAN, `FastEthernet0/1` with the port you want to use, and `[VOICE_VLAN_NUMBER]` with the number of your voice VLAN.


  2.1.b Default VLAN


    Configuring and verifying VLANs spanning multiple switches for the default VLAN involves the following steps:

    By default, all switch ports are part of VLAN 1. So if you wish to change the default VLAN, you have to create a new VLAN and assign all ports to the new VLAN.

    1. Connect to your switch using a console cable and open your terminal program.

    2. Enter the user exec mode by typing `enable` and press `Enter`.

    3. Enter the global configuration mode by typing `configure terminal` and press `Enter`.

    4. Create a new VLAN by typing `vlan [VLAN_NUMBER]` (replace `[VLAN_NUMBER]` with your desired VLAN number between 1 and 1005). Press `Enter`.

    5. Exit back to the global configuration mode by typing `exit` and press `Enter`.

    6. Now, assign all ports to the new VLAN by typing `interface range FastEthernet 0/1 - 24` (or the range of your specific model), then `switchport mode access`, then `switchport access vlan [VLAN_NUMBER]` and press `Enter`.

    7. Save your changes by typing `exit`, then `copy running-config startup-config`.

    To verify your configuration:

    1. In the privileged exec mode (type `enable` and press `Enter` if you're not already in this mode), type `show vlan brief`. This command will display a summary of the VLANs on the switch.

    2. Type `show interfaces switchport` to see the access mode and VLAN assignment of each port.

    Repeat these steps on each switch where you want the VLAN to exist. For the VLAN to span multiple switches, the switches need to be interconnected with trunk ports, which carry traffic from all VLANs by default.

    Remember to replace `[VLAN_NUMBER]` with the VLAN number you chose, and adjust the range of interfaces based on your specific switch model.

  2.1.c InterVLAN connectivity

    InterVLAN connectivity allows devices on different VLANs to communicate with each other. This requires a router or a layer 3 switch. Here's how to configure it:

    1. Connect to your switch using a console cable and open your terminal program.

    2. Enter the user exec mode by typing `enable` and press `Enter`.

    3. Enter the global configuration mode by typing `configure terminal` and press `Enter`.

    4. Create your VLANs (if not created already) by typing `vlan [VLAN_NUMBER]` (replace `[VLAN_NUMBER]` with your desired VLAN number between 1 and 1005). Press `Enter` and then type `exit`.

    5. Assign the VLANs to the ports by typing `interface [INTERFACE_ID]` (replace `[INTERFACE_ID]` with the interface you want to assign), then `switchport mode access` and then `switchport access vlan [VLAN_NUMBER]`.

    6. Connect the switches to the router or Layer 3 switch. The interfaces on the router or Layer 3 switch connected to the switches should be configured as sub-interfaces, one for each VLAN.

    7. On the router or Layer 3 switch, enter the interface configuration mode by typing `interface [INTERFACE_ID].[VLAN_NUMBER]` (replace `[INTERFACE_ID]` with the interface connected to the switch and `[VLAN_NUMBER]` with the VLAN number).

    8. Assign each sub-interface to a VLAN by typing `encapsulation dot1Q [VLAN_NUMBER]` and assign an IP address to each sub-interface by typing `ip address [IP_ADDRESS] [SUBNET_MASK]`.

    9. Save your changes by typing `exit`, then `copy running-config startup-config`.

    To verify your configuration:

    1. On the switch, in the privileged exec mode (type `enable` and press `Enter` if you're not already in this mode), type `show vlan brief`. This command will display a summary of the VLANs on the switch.

    2. On the router or Layer 3 switch, type `show ip interface brief` to display the IP addresses of the sub-interfaces.

    Remember to replace `[VLAN_NUMBER]`, `[INTERFACE_ID]`, `[IP_ADDRESS]`, and `[SUBNET_MASK]` with your specific VLAN numbers, interfaces, IP addresses, and subnet masks.

---------------------------------------------------------------------------------------------------------

2.2 Configure and verify interswitch connectivity
  2.2.a Trunk ports

    Sure, here's how you can configure and verify trunk ports for interswitch connectivity on a Cisco switch:

    1. Connect to your switch using a console cable and open your terminal program (like PuTTY).

    2. Once connected, enter the user exec mode by typing `enable` and press `Enter`.

    3. Enter the global configuration mode by typing `configure terminal` and press `Enter`.

    4. Select the interface you want to configure as a trunk port: Type `interface FastEthernet 0/1` (replace `FastEthernet 0/1` with the interface you want to use) and press `Enter`.

    5. Set the switchport mode to trunk: Type `switchport mode trunk` and press `Enter`.

    6. (Optional) By default, a trunk port will carry all VLANs. If you want to limit which VLANs can be carried over the trunk link, use the `switchport trunk allowed vlan` command followed by the VLAN numbers.

    7. Exit the interface configuration mode: Type `exit` and press `Enter`.

    8. Save your changes: Type `copy running-config startup-config` and press `Enter`.

    To verify your trunk configuration:

    1. In the privileged exec mode (type `enable` and press `Enter` if you're not already in this mode), type `show interfaces trunk`. This command will display information about all the current trunk ports including the native VLAN and the allowed VLANs on each trunk.

    Please replace `FastEthernet 0/1` with the interface you want to configure as a trunk port.

  2.2.b 802.1Q

    The 802.1Q protocol is used for VLAN tagging in Ethernet networks. This protocol allows multiple VLANs to be used over a single link (trunk link) between switches. Here's how to configure and verify it on a Cisco switch:

    1. Connect to your switch using a console cable and open your terminal program (like PuTTY).

    2. Once connected, enter the user exec mode by typing `enable` and press `Enter`.

    3. Enter the global configuration mode by typing `configure terminal` and press `Enter`.

    4. Select the interface you want to configure as a trunk port: Type `interface FastEthernet 0/1` (replace `FastEthernet 0/1` with the interface you want to use) and press `Enter`.

    5. Set the switchport mode to trunk: Type `switchport mode trunk` and press `Enter`.

    6. Set the encapsulation mode to 802.1Q: Type `switchport trunk encapsulation dot1q` and press `Enter`.

    7. (Optional) By default, a trunk port will carry all VLANs. If you want to limit which VLANs can be carried over the trunk link, use the `switchport trunk allowed vlan` command followed by the VLAN numbers.

    8. Exit the interface configuration mode: Type `exit` and press `Enter`.

    9. Save your changes: Type `copy running-config startup-config` and press `Enter`.

    To verify your trunk configuration:

    1. In the privileged exec mode (type `enable` and press `Enter` if you're not already in this mode), type `show interfaces trunk`. This command will display information about all the current trunk ports including the encapsulation type (should be 802.1Q), native VLAN and the allowed VLANs on each trunk.

    Please replace `FastEthernet 0/1` with the interface you want to configure as a trunk port.

  2.2.c Native VLAN

    The Native VLAN is a specified VLAN that a trunk port sends untagged frames to when it receives untagged frames. Here's how to configure and verify it:

    1. Connect to your switch using a console cable and open your terminal program.

    2. Once connected, enter the user exec mode by typing `enable` and press `Enter`.

    3. Enter the global configuration mode by typing `configure terminal` and press `Enter`.

    4. Choose the interface you wish to configure as a trunk port: Type `interface FastEthernet 0/1` (replace `FastEthernet 0/1` with the interface you want to use), and press `Enter`.

    5. Set the switchport mode to trunk: Type `switchport mode trunk` and press `Enter`.

    6. Set the Native VLAN ID: Type `switchport trunk native vlan [VLAN_ID]` (replace `[VLAN_ID]` with the VLAN ID you want to use as the Native VLAN), and press `Enter`.

    7. Exit the interface configuration mode: Type `exit` and press `Enter`.

    8. Save your changes: Type `copy running-config startup-config` and press `Enter`.

    To verify your Native VLAN configuration:

    1. In the privileged exec mode (type `enable` and press `Enter` if you're not already in this mode), type `show interfaces trunk`. This command will display information about all the current trunk ports, including the Native VLAN for each trunk.

    Note: For proper network operation, the Native VLAN should be the same on both ends of the trunk link.

    Please replace `FastEthernet 0/1` and `[VLAN_ID]` with the interface and VLAN ID you want to configure as the Native VLAN, respectively.

---------------------------------------------------------------------------------------------------------

2.3 Configure and verify Layer 2 discovery protocols (Cisco Discovery Protocol and LLDP)

  Sure, here's how you can configure and verify Layer 2 discovery protocols like Cisco Discovery Protocol (CDP) and Link Layer Discovery Protocol (LLDP) on a Cisco switch:

  1. Connect to your switch using a console cable and open your terminal program.

  2. Once connected, enter the user exec mode by typing `enable` and press `Enter`.

  3. Enter the global configuration mode by typing `configure terminal` and press `Enter`.

  For CDP:

  1. To enable CDP globally, type `cdp run` and press `Enter`.

  2. To disable CDP on a specific interface, first select the interface by typing `interface FastEthernet 0/1` (replace `FastEthernet 0/1` with the interface you want), press `Enter`, then type `no cdp enable`.

  For LLDP:

  1. To enable LLDP globally, type `lldp run` and press `Enter`.

  2. To disable LLDP on a specific interface, select the interface by typing `interface FastEthernet 0/1` (replace `FastEthernet 0/1` with the interface you want), press `Enter`, then type `no lldp transmit` and `no lldp receive`.

  To verify your configuration:

  1. For CDP, in the privileged exec mode (type `enable` and press `Enter` if you're not already in this mode), type `show cdp neighbors` to display a summary of neighboring devices discovered by CDP.

  2. For LLDP, in the privileged exec mode, type `show lldp neighbors` to display a summary of neighboring devices discovered by LLDP.

  Please replace `FastEthernet 0/1` with the interface you want to configure.

---------------------------------------------------------------------------------------------------------

2.4 Configure and verify (Layer 2/Layer 3) EtherChannel (LACP)

  EtherChannel allows you to combine several physical Ethernet links to create one logical Ethernet link for the purpose of providing fault-tolerance and high-speed links between switches, routers, and servers. Here's how to configure and verify it:

  1. Connect to your switch using a console cable and open your terminal program.

  2. Once connected, enter the user exec mode by typing `enable` and press `Enter`.

  3. Enter the global configuration mode by typing `configure terminal` and press `Enter`.

  4. Choose the interfaces you want to configure as part of the EtherChannel. Type `interface range FastEthernet 0/1 - 2` (replace `FastEthernet 0/1 - 2` with the interfaces you want to use), and press `Enter`.

  5. Set the interfaces to use LACP (Link Aggregation Control Protocol) by typing `channel-group 1 mode active` and press `Enter`. This will create a new port-channel interface (Port-channel 1) and enable LACP.

  6. Exit the interface configuration mode: Type `exit` and press `Enter`.

  7. Now, configure the Port-channel interface. Type `interface Port-channel 1` and press `Enter`.

  8. (Optional) If you are configuring Layer 3 EtherChannel, assign an IP address to the Port-channel interface by typing `ip address [IP_ADDRESS] [SUBNET_MASK]` and press `Enter`.

  9. Save your changes: Type `exit`, then `copy running-config startup-config` and press `Enter`.

  To verify your EtherChannel configuration:

  1. In the privileged exec mode (type `enable` and press `Enter` if you're not already in this mode), type `show etherchannel summary`. This command will display information about the EtherChannel, including the interfaces in the channel and the protocol used.

  Please replace `FastEthernet 0/1 - 2`, `[IP_ADDRESS]`, and `[SUBNET_MASK]` with the interfaces, IP address, and subnet mask you want to use, respectively.

---------------------------------------------------------------------------------------------------------

2.9 Configure the components of a wireless LAN access for client connectivity using GUI only such as WLAN creation, security settings, QoS profiles, and advanced WLAN settings

  To configure the components of a wireless LAN access for client connectivity using GUI only, you'd typically use a web interface provided by the wireless router or access point. The exact steps can vary depending on the specific model of your wireless device, but here's a general guideline:

  1. **Accessing the web interface**:
     Connect to your wireless router or access point either wirelessly or using an Ethernet cable. Open a web browser and enter the IP address of the device in the address bar (often something like 192.168.0.1 or 192.168.1.1). You should be prompted for a username and password.

  2. **WLAN creation**:
     Once logged in, look for a section or tab labeled "Wireless," "Wireless Settings," or something similar. Here, you can set up your wireless network(s). You might have the option to create multiple wireless networks (SSIDs).

  3. **Security settings**:
     Still under the "Wireless" section, look for "Security" settings. You can select the type of security (WPA2 is generally recommended), and set the password (also known as a pre-shared key) for the network.

  4. **QoS profiles**:
     Quality of Service (QoS) settings can usually be found under their own section or tab, labeled "QoS" or something similar. Here, you can prioritize different types of traffic to ensure, for example, that video streaming gets priority over file downloads.

  5. **Advanced WLAN settings**:
     Under "Wireless" or a separate "Advanced" section, you can adjust various other settings like the wireless mode (b/g/n/ac), channel width, and more. Unless you know what you're doing, it's often best to leave these at their default settings.

  6. **Save your settings**:
     Make sure to save your settings before exiting. There is usually a "Save" or "Apply" button at the bottom of each page.

  Remember, these are general steps. The exact labels and locations of these settings can vary widely between different devices, so refer to your device's manual or online documentation for specific instructions.


---------------------------------------------------------------------------------------------------------

3.3 Configure and verify IPv4 and IPv6 static routing
  3.3.a Default route

    Configuring static routing, including a default route, on a Cisco router involves the following steps. 

    For IPv4:

    1. Connect to your router using console cable and launch your terminal program.

    2. Enter the user exec mode by typing `enable` in the command line interface (CLI).

    3. Enter the global configuration mode by typing `configure terminal`.

    4. To set a default route, type `ip route 0.0.0.0 0.0.0.0 [next_hop_IP]`, where `[next_hop_IP]` is the IP address of the next hop router or exit interface.

    5. Press `Enter`.

    6. Save your changes by typing `exit`, then `copy running-config startup-config`.

    For IPv6:

    1. Connect to your router using console cable and launch your terminal program.

    2. Enter the user exec mode by typing `enable` in the command line interface (CLI).

    3. Enter the global configuration mode by typing `configure terminal`.

    4. To set a default route, type `ipv6 route ::/0 [next_hop_IPv6]`, where `[next_hop_IPv6]` is the IPv6 address of the next hop router or exit interface.

    5. Press `Enter`.

    6. Save your changes by typing `exit`, then `copy running-config startup-config`.

    To verify your configuration:

    1. In the privileged exec mode, type `show ip route` for IPv4 or `show ipv6 route` for IPv6 to display the routing table and verify that the default route is listed.

    Please replace `[next_hop_IP]` and `[next_hop_IPv6]` with the IP address of your next hop router or exit interface.


  3.3.b Network route
  
    To configure IPv4 and IPv6 static routes on a Cisco router, follow these steps:

    For IPv4:

    1. Connect to your router using console cable and launch your terminal program.

    2. Enter the user exec mode by typing `enable` in the command line interface (CLI).

    3. Enter the global configuration mode by typing `configure terminal`.

    4. To set a static route, type `ip route [destination_network] [subnet_mask] [next_hop_IP]` or `ip route [destination_network] [subnet_mask] [exit_interface]`, where `[destination_network]` is the network you want to reach, `[subnet_mask]` is the subnet mask of the destination network, `[next_hop_IP]` is the IP address of the next-hop router, and `[exit_interface]` is the local interface to use to forward packets.

    5. Press `Enter`.

    6. Save your changes by typing `exit`, then `copy running-config startup-config`.

    For IPv6:

    1. Connect to your router using console cable and launch your terminal program.

    2. Enter the user exec mode by typing `enable` in the command line interface (CLI).

    3. Enter the global configuration mode by typing `configure terminal`.

    4. To set a static route, type `ipv6 route [destination_network] [next_hop_IPv6]` or `ipv6 route [destination_network] [exit_interface]`, where `[destination_network]` is the network you want to reach, `[next_hop_IPv6]` is the IPv6 address of the next-hop router, and `[exit_interface]` is the local interface to use to forward packets.

    5. Press `Enter`.

    6. Save your changes by typing `exit`, then `copy running-config startup-config`.

    To verify your configuration:

    1. In the privileged exec mode, type `show ip route` for IPv4 or `show ipv6 route` for IPv6 to display the routing table and verify that the static route is listed.

    Please replace `[destination_network]`, `[subnet_mask]`, `[next_hop_IP]`, `[next_hop_IPv6]`, and `[exit_interface]` with your specific network details. 

  3.3.c Host route

    To configure IPv4 and IPv6 static routes for a specific host on a Cisco router, follow these steps:

    For IPv4:

    1. Connect to your router using console cable and launch your terminal program.

    2. Enter the user exec mode by typing `enable` in the command line interface (CLI).

    3. Enter the global configuration mode by typing `configure terminal`.

    4. To set a static route to a specific host, type `ip route [host_IP] 255.255.255.255 [next_hop_IP]` or `ip route [host_IP] 255.255.255.255 [exit_interface]`, where `[host_IP]` is the IP address of the host you want to reach, `[next_hop_IP]` is the IP address of the next-hop router, and `[exit_interface]` is the local interface to use to forward packets.

    5. Press `Enter`.

    6. Save your changes by typing `exit`, then `copy running-config startup-config`.

    For IPv6:

    1. Connect to your router using console cable and launch your terminal program.

    2. Enter the user exec mode by typing `enable` in the command line interface (CLI).

    3. Enter the global configuration mode by typing `configure terminal`.

    4. To set a static route to a specific host, type `ipv6 route [host_IPv6]/128 [next_hop_IPv6]` or `ipv6 route [host_IPv6]/128 [exit_interface]`, where `[host_IPv6]` is the IPv6 address of the host you want to reach, `[next_hop_IPv6]` is the IPv6 address of the next-hop router, and `[exit_interface]` is the local interface to use to forward packets.

    5. Press `Enter`.

    6. Save your changes by typing `exit`, then `copy running-config startup-config`.

    To verify your configuration:

    1. In the privileged exec mode, type `show ip route` for IPv4 or `show ipv6 route` for IPv6 to display the routing table and verify that the static route to the host is listed.

    Please replace `[host_IP]`, `[next_hop_IP]`, `[host_IPv6]`, `[next_hop_IPv6]`, and `[exit_interface]` with your specific host and network details.


  3.3.d Floating static

    A floating static route is a static route that has an administrative distance greater than the administrative distance (AD) of another static route or dynamic routes. Floating static routes provide a backup path in case of a failure of the primary path.

    Here's how to configure a floating static route for IPv4 and IPv6:

    For IPv4:

    1. Connect to your router using a console cable and launch your terminal program.

    2. Enter the user exec mode by typing `enable` in the command line interface (CLI).

    3. Enter the global configuration mode by typing `configure terminal`.

    4. To set a floating static route, type `ip route [destination_network] [subnet_mask] [next_hop_IP] [administrative_distance]`, where `[destination_network]` is the network you want to reach, `[subnet_mask]` is the subnet mask of the destination network, `[next_hop_IP]` is the IP address of the next-hop router, and `[administrative_distance]` is the AD you want to set (it should be higher than the AD of the primary route).

    5. Press `Enter`.

    6. Save your changes by typing `exit`, then `copy running-config startup-config`.

    For IPv6:

    1. Connect to your router using a console cable and launch your terminal program.

    2. Enter the user exec mode by typing `enable` in the command line interface (CLI).

    3. Enter the global configuration mode by typing `configure terminal`.

    4. To set a floating static route, type `ipv6 route [destination_network] [next_hop_IPv6] [administrative_distance]`, where `[destination_network]` is the network you want to reach, `[next_hop_IPv6]` is the IPv6 address of the next-hop router, and `[administrative_distance]` is the AD you want to set (it should be higher than the AD of the primary route).

    5. Press `Enter`.

    6. Save your changes by typing `exit`, then `copy running-config startup-config`.

    To verify your configuration:

    1. In the privileged exec mode, type `show ip route` for IPv4 or `show ipv6 route` for IPv6 to display the routing table and verify that the floating static route is listed.

    Please replace `[destination_network]`, `[subnet_mask]`, `[next_hop_IP]`, `[next_hop_IPv6]`, and `[administrative_distance]` with your specific network details.


---------------------------------------------------------------------------------------------------------

3.4 Configure and verify single area OSPFv2
  3.4.a Neighbor adjacencies

    Open Shortest Path First version 2 (OSPFv2) is a routing protocol for IPv4. Here's how to configure OSPFv2 and verify neighbor adjacencies:

    1. Connect to your router using a console cable and open your terminal program.

    2. Enter the user exec mode by typing `enable` and press `Enter`.

    3. Enter the global configuration mode by typing `configure terminal`.

    4. Enable the OSPF process and assign a process ID by typing `router ospf [process_id]`, where `[process_id]` is a number you assign to uniquely identify the OSPF process on the router. The range is from 1 to 65535.

    5. Assign the router to an OSPF area by typing `network [network_address] [wildcard_mask] area [area_id]`. Here, `[network_address]` is the IP address of the network, `[wildcard_mask]` is the inverse of the subnet mask, and `[area_id]` is the ID of the area to which you want to assign the network.

    6. (Optional) Configure the router ID, which helps identify the router in the OSPF network, by typing `router-id [router_id]`, where `[router_id]` is the ID you want to assign to the router. If not configured manually, the router will use the highest IP address of its active interfaces.

    7. Save your changes by typing `exit`, then `copy running-config startup-config`.

    To verify your configuration:

    1. In the privileged exec mode (type `enable` and press `Enter` if you're not already in this mode), type `show ip ospf neighbor`. This command will display information about OSPF neighbor adjacencies, including the neighbor's router ID, priority, state, and IP address.

    Please replace `[process_id]`, `[network_address]`, `[wildcard_mask]`, `[area_id]`, and `[router_id]` with your specific OSPF parameters.

  3.4.b Point-to-point

    Configuring a point-to-point OSPFv2 connection involves setting up OSPF on the interfaces that connect directly to each other. Here's how to do it:

    1. Connect to your router using a console cable and open your terminal program.

    2. Enter the user exec mode by typing `enable` and press `Enter`.

    3. Enter the global configuration mode by typing `configure terminal` and press `Enter`.

    4. Enable the OSPF process and assign a process ID by typing `router ospf [process_id]`, where `[process_id]` is a number you assign to uniquely identify the OSPF process on the router. The range is from 1 to 65535.

    5. (Optional) Configure the router ID, which helps identify the router in the OSPF network, by typing `router-id [router_id]`, where `[router_id]` is the ID you want to assign to the router. If not configured manually, the router will use the highest IP address of its active interfaces.

    6. Go into the interface configuration mode for the interface you want to configure by typing `interface [interface_id]`, where `[interface_id]` is the ID of the interface.

    7. Enable OSPF on the interface by typing `ip ospf [process_id] area [area_id]`, where `[process_id]` is the OSPF process ID you assigned earlier and `[area_id]` is the ID of the OSPF area you want the interface to belong to.

    8. Set the network type to point-to-point by typing `ip ospf network point-to-point`.

    9. Save your changes by typing `exit`, then `copy running-config startup-config`.

    To verify your configuration:

    1. In the privileged exec mode (type `enable` and press `Enter` if you're not already in this mode), type `show ip ospf interface brief`. This command will display brief information about the OSPF interfaces, including the network type.

    Please replace `[process_id]`, `[interface_id]`, `[area_id]`, and `[router_id]` with your specific OSPF parameters.

  3.4.c Broadcast (DR/BDR selection)

    In a broadcast multi-access network, OSPF elects one router to be a Designated Router (DR) and another to be a Backup Designated Router (BDR) to manage the OSPF information exchange between routers. Here's how to configure it:

    1. Connect to your router using a console cable and open your terminal program.

    2. Enter the user exec mode by typing `enable` and press `Enter`.

    3. Enter the global configuration mode by typing `configure terminal` and press `Enter`.

    4. Enable the OSPF process and assign a process ID by typing `router ospf [process_id]`, where `[process_id]` is a number you assign to uniquely identify the OSPF process on the router. The range is from 1 to 65535.

    5. (Optional) Configure the router ID, which helps identify the router in the OSPF network, by typing `router-id [router_id]`, where `[router_id]` is the ID you want to assign to the router. If not configured manually, the router will use the highest IP address of its active interfaces.

    6. Go into the interface configuration mode for the interface you want to configure by typing `interface [interface_id]`, where `[interface_id]` is the ID of the interface.

    7. Enable OSPF on the interface by typing `ip ospf [process_id] area [area_id]`, where `[process_id]` is the OSPF process ID you assigned earlier and `[area_id]` is the ID of the OSPF area you want the interface to belong to.

    8. (Optional) To influence the DR/BDR election process, you can assign a priority to the interface by typing `ip ospf priority [priority]`, where `[priority]` is a number between 0 and 255. The router with the highest priority will become the DR. If the priorities are equal, the router with the highest router ID will become the DR.

    9. Save your changes by typing `exit`, then `copy running-config startup-config`.

    To verify your configuration:

    1. In the privileged exec mode (type `enable` and press `Enter` if you're not already in this mode), type `show ip ospf neighbor`. This command will display information about the OSPF neighbors, including the DR and BDR.

    Please replace `[process_id]`, `[interface_id]`, `[area_id]`, `[router_id]`, and `[priority]` with your specific OSPF parameters.

  3.4.d Router ID

    To configure and verify the OSPFv2 Router ID, follow the steps below:

    1. Connect to your router using a console cable and launch your terminal program.

    2. Enter the user exec mode by typing `enable` in the command line interface (CLI).

    3. Enter the global configuration mode by typing `configure terminal`.

    4. Enable the OSPF process and assign a process ID by typing `router ospf [process_id]`, where `[process_id]` is a number you assign to uniquely identify the OSPF process on the router. The range is from 1 to 65535.

    5. Configure the router ID, which helps identify the router in the OSPF network, by typing `router-id [router_id]`, where `[router_id]` is the ID you want to assign to the router.

    6. Save your changes by typing `exit`, then `copy running-config startup-config`.

    To verify your configuration:

    1. In the privileged exec mode (type `enable` and press `Enter` if you're not already in this mode), type `show ip ospf`. This command will display information about the OSPF process, including the Router ID.

    Please replace `[process_id]` and `[router_id]` with your specific OSPF parameters. The router ID should be a unique, routable IP address in your network. It's often a good practice to use a loopback interface IP for the router ID, as it's not associated with a physical interface that could go down.

---------------------------------------------------------------------------------------------------------

4.1 Configure and verify inside source NAT using static and pools

  Network Address Translation (NAT) allows a device like a router to translate IP addresses from one network to another. This is often used to allow multiple devices on a local network to share a single public IP address. Here's how to configure inside source NAT using static mapping and pools on a Cisco router:

  **For Static NAT:**

  1. Connect to your router using a console cable and launch your terminal program.

  2. Enter the user exec mode by typing `enable` and press `Enter`.

  3. Enter the global configuration mode by typing `configure terminal` and press `Enter`.

  4. Configure a static NAT translation by typing `ip nat inside source static [local_IP] [global_IP]`, where `[local_IP]` is the IP address of the host on the local network and `[global_IP]` is the IP address that the host will use on the global network.

  5. Press `Enter`.

  6. Go into the interface configuration mode for the inside interface (connected to the local network) by typing `interface [inside_interface_id]`, where `[inside_interface_id]` is the ID of the inside interface.

  7. Enable NAT on the inside interface by typing `ip nat inside`.

  8. Press `Enter`.

  9. Go into the interface configuration mode for the outside interface (connected to the global network) by typing `interface [outside_interface_id]`, where `[outside_interface_id]` is the ID of the outside interface.

  10. Enable NAT on the outside interface by typing `ip nat outside`.

  11. Press `Enter`.

  12. Save your changes by typing `exit`, then `copy running-config startup-config` and press `Enter`.

  **For Dynamic NAT with a Pool:**

  1. Follow steps 1-3 from the static NAT configuration above.

  2. Define a pool of global addresses for NAT to use by typing `ip nat pool [pool_name] [start_IP] [end_IP] netmask [subnet_mask]`, where `[pool_name]` is the name you want to give to the address pool, `[start_IP]` and `[end_IP]` define the range of addresses in the pool, and `[subnet_mask]` is the subnet mask of the global network.

  3. Press `Enter`.

  4. Define which local addresses should be translated by creating an access list. For example, to translate all addresses in the local network, type `access-list 1 permit [local_network] [wildcard_mask]`, where `[local_network]` is the network address of the local network and `[wildcard_mask]` is the inverse of the subnet mask.

  5. Press `Enter`.

  6. Configure NAT to use the pool and access list by typing `ip nat inside source list 1 pool [pool_name]`, where `[pool_name]` is the name of the address pool you created earlier.

  7. Press `Enter`.

  8. Follow steps 6-12 from the static NAT configuration above.

  To verify your NAT configuration, type `show ip nat translations` in the privileged exec mode to display the current NAT translations.

  Please replace `[local_IP]`, `[global_IP]`, `[inside_interface_id]`, `[outside_interface_id]`, `[pool_name]`, `[start_IP]`, `[end_IP]`, `[subnet_mask]`, `[local_network]`, and `[wildcard_mask]` with your specific network parameters.


---------------------------------------------------------------------------------------------------------

4.2 Configure and verify NTP operating in a client and server mode

  Configuring and verifying Network Time Protocol (NTP) operating in a client-server mode mainly involves setting up one device as a server and another as a client, then ensuring that the client can synchronize its time with the server.

  Here's a simplified version of how you can do this on a Cisco device:

  1. **Configuring the NTP Server:**

  On your server device, enter the following commands in configuration mode:

  ```
  Router> enable
  Router# configure terminal
  Router(config)# ntp master 1
  Router(config)# end
  ```

  This sets the device as an NTP server with a stratum level of 1, which is the highest level of accuracy.

  2. **Configuring the NTP Client:**

  On your client device, you would point it towards the server using the server's IP address:

  ```
  Router> enable
  Router# configure terminal
  Router(config)# ntp server 192.168.1.1
  Router(config)# end
  ```

  Replace "192.168.1.1" with the IP address of your server.

  3. **Verifying NTP Operation:**

  You can verify that NTP is functioning correctly on both the client and server with the command:

  ```
  Router> show ntp status
  ```

  On the server, it should show `synchronized to local sys`, and on the client, it should show `synchronized to 192.168.1.1`, or whatever the IP of your server is.

  Keep in mind that NTP synchronization may take several minutes. Also, the specifics of these instructions can vary depending on the exact equipment and software you're using. Always refer to your device's specific documentation for the most accurate information.



---------------------------------------------------------------------------------------------------------

4.6 Configure and verify DHCP client and relay

  Configuring and verifying a DHCP client and relay involves setting up a device to receive an IP address from a DHCP server and a relay to forward DHCP requests between networks.

  Here's a simplified version of how you can do this on a Cisco device:

  1. **Configuring the DHCP Client:**

  On your client device, enter the following commands in configuration mode:

  ```bash
  Router> enable
  Router# configure terminal
  Router(config)# interface gigabitEthernet 0/0
  Router(config-if)# ip address dhcp
  Router(config-if)# no shutdown
  Router(config-if)# end
  ```

  This sets the device's GigabitEthernet 0/0 interface to automatically receive an IP address from a DHCP server.

  2. **Configuring the DHCP Relay:**

  On your relay device, you would set it to forward DHCP requests to a specific server:

  ```bash
  Router> enable
  Router# configure terminal
  Router(config)# interface gigabitEthernet 0/0
  Router(config-if)# ip helper-address 192.168.1.1
  Router(config-if)# end
  ```

  Replace "192.168.1.1" with the IP address of your DHCP server. This will forward all DHCP requests that the device receives on its GigabitEthernet 0/0 interface to the specified server.

  3. **Verifying DHCP Operation:**

  You can verify that the DHCP client and relay are functioning correctly with the commands:

  ```bash
  Router> show ip interface brief
  ```

  For the client, this will show the IP address that it has received from the DHCP server.

  ```bash
  Router> show ip helper-address
  ```

  For the relay, this will show the IP address of the DHCP server that it is forwarding requests to.

  Keep in mind that DHCP may take a few moments to assign an IP address. Also, the specifics of these instructions can vary depending on the exact equipment and software you're using. Always refer to your device's specific documentation for the most accurate information.


---------------------------------------------------------------------------------------------------------

4.8 Configure network devices for remote access using SSH

  Secure Shell (SSH) is a cryptographic network protocol for securely accessing network devices over an unsecured network. Here's a basic procedure on how to configure a Cisco device for remote access using SSH:

  1. **Configure Hostname and Domain Name:**

  SSH requires a hostname and domain name to generate necessary RSA keys. If your router doesn’t have them configured yet, you can do so as follows:

  ```bash
  Router> enable
  Router# configure terminal
  Router(config)# hostname MyRouter
  MyRouter(config)# ip domain-name mydomain.com
  ```

  2. **Generate RSA Key:**

  SSH works by using a pair of keys: one public and one private. You need to generate these keys on your router:

  ```bash
  MyRouter(config)# crypto key generate rsa
  ```

  When prompted, choose a modulus of at least 1024 bits for security.

  3. **Configure User and Password:**

  You need to configure the local database with usernames and passwords to use for SSH login:

  ```bash
  MyRouter(config)# username admin password mypassword
  ```

  4. **Enable SSH on the VTY lines:**

  Now enable SSH access on the VTY lines and specify the local user database for authentication:

  ```bash
  MyRouter(config)# line vty 0 4
  MyRouter(config-line)# transport input ssh
  MyRouter(config-line)# login local
  MyRouter(config-line)# exit
  ```

  5. **Set SSH Version:**

  To increase security, it is recommended to set the SSH version to 2:

  ```bash
  MyRouter(config)# ip ssh version 2
  ```

  6. **Verify SSH Configuration:**

  You can verify SSH access to your router by using the following command:

  ```bash
  MyRouter# show ip ssh
  ```

  This will display the SSH version and RSA key pair details.

  The device is now configured for SSH remote access. You can SSH into the router using the created user credentials. Always make sure to replace "MyRouter", "mydomain.com", "admin", and "mypassword" with your own specific values. Also, these instructions may vary depending on your specific equipment and software. Always refer to your device's documentation for the most accurate information.



---------------------------------------------------------------------------------------------------------

5.3 Configure and verify device access control using local passwords

  To configure and verify device access control using local passwords on a Cisco device, you would generally follow these steps:

  1. **Setting Up a Password for Privileged Mode (Enable Password):**

  ```bash
  Router> enable
  Router# configure terminal
  Router(config)# enable secret mypassword
  ```

  Here, replace "mypassword" with the password you want to use for privileged mode.

  2. **Setting Up a Password for Console Access:**

  ```bash
  Router(config)# line console 0
  Router(config-line)# password mypassword
  Router(config-line)# login
  Router(config-line)# exit
  ```

  Again, replace "mypassword" with the password you want to use for console access.

  3. **Setting Up a Password for Remote (VTY) Access:**

  ```bash
  Router(config)# line vty 0 4
  Router(config-line)# password mypassword
  Router(config-line)# login
  Router(config-line)# exit
  Router(config)# exit
  ```

  Replace "mypassword" with the password you want to use for remote access.

  4. **Verifying Access Control:**

  To verify that the passwords are working, you can simply try accessing the device through the console or remotely via Telnet or SSH (if configured). You should be prompted for the password.

  Remember to replace "mypassword" with the password you want to use. The `enable secret` command provides a higher security level for protecting privileged access than the older `enable password` command. Also, always refer to your device's specific documentation for the most accurate information.


---------------------------------------------------------------------------------------------------------

5.6 Configure and verify access control lists

  Access Control Lists (ACLs) are used to filter network traffic on Cisco routers. Here's a simplified version of how you can configure and verify standard ACLs:

  1. **Configuring an Access Control List:**

  You can configure a standard ACL to permit or deny traffic from a certain IP address. For example, to deny traffic from the IP address 192.168.1.1, you would enter the following commands:

  ```bash
  Router> enable
  Router# configure terminal
  Router(config)# access-list 1 deny 192.168.1.1 0.0.0.0
  Router(config)# access-list 1 permit any
  Router(config)# end
  ```

  The first command denies traffic from 192.168.1.1, and the second permits all other traffic. The number "1" is the ACL number.

  2. **Applying the ACL to an Interface:**

  Next, apply the ACL to an interface, for example, the GigabitEthernet 0/0 interface:

  ```bash
  Router> enable
  Router# configure terminal
  Router(config)# interface gigabitEthernet 0/0
  Router(config-if)# ip access-group 1 in
  Router(config-if)# end
  ```

  This applies the ACL to incoming traffic on the GigabitEthernet 0/0 interface.

  3. **Verifying the ACL:**

  You can view the configuration of your ACLs with the command:

  ```bash
  Router# show access-lists
  ```

  This will display all ACLs configured on the router, including their permit and deny statements.

  Remember, the specifics of these instructions can vary depending on the exact equipment and software you're using. Always refer to your device's specific documentation for the most accurate information. Also, be careful when configuring ACLs, as incorrect configurations can cause network connectivity issues.


---------------------------------------------------------------------------------------------------------

5.7 Configure Layer 2 security features (DHCP snooping, dynamic ARP inspection, and port security)

  Configuring Layer 2 security features on a Cisco switch involves setting up DHCP snooping, dynamic ARP inspection, and port security. Here's a basic procedure for each:

  1. **DHCP Snooping:** 

  DHCP snooping filters out untrusted DHCP messages and prevents DHCP spoofing attacks.

  ```bash
  Switch> enable
  Switch# configure terminal
  Switch(config)# ip dhcp snooping
  Switch(config)# ip dhcp snooping vlan 1
  Switch(config)# interface fastEthernet 0/1
  Switch(config-if)# ip dhcp snooping trust
  Switch(config-if)# end
  ```

  Replace "vlan 1" with your VLAN number and "fastEthernet 0/1" with your interface name. The trusted interface should be the one facing the DHCP server.

  2. **Dynamic ARP Inspection (DAI):** 

  DAI validates ARP packets in a network. It prevents ARP spoofing attacks.

  ```bash
  Switch> enable
  Switch# configure terminal
  Switch(config)# ip arp inspection vlan 1
  Switch(config)# interface fastEthernet 0/1
  Switch(config-if)# ip arp inspection trust
  Switch(config-if)# end
  ```

  Replace "vlan 1" with your VLAN number and "fastEthernet 0/1" with your interface name. The trusted interface should be the one facing the DHCP server.

  3. **Port Security:**

  Port Security allows you to restrict input to an interface by limiting the MAC addresses of the stations allowed to access the port.

  ```bash
  Switch> enable
  Switch# configure terminal
  Switch(config)# interface fastEthernet 0/1
  Switch(config-if)# switchport mode access
  Switch(config-if)# switchport port-security
  Switch(config-if)# switchport port-security maximum 1
  Switch(config-if)# switchport port-security mac-address sticky
  Switch(config-if)# switchport port-security violation restrict
  Switch(config-if)# end
  ```

  Replace "fastEthernet 0/1" with your interface name. This configuration allows only one MAC address to access the interface, learns the MAC address dynamically, and restricts traffic with unknown source addresses.

  Remember to always refer to your device's specific documentation for the most accurate information.

---------------------------------------------------------------------------------------------------------

5.10 Configure WLAN using WPA2 PSK using the GUI

  To set up a WLAN using WPA2 PSK via the GUI, you'll typically need to access your wireless router or access point's web interface and adjust the wireless security settings. Here's a basic step-by-step guide:

  1. **Access your router's web interface:**
     - Open a web browser on a device connected to your network.
     - Type the IP address of your router into the address bar (common default IP addresses are 192.168.0.1, 192.168.1.1, or 192.168.1.254).
     - Press Enter.
     
  2. **Log in:**
     - Enter your username and password when prompted. If you haven't changed these, they'll be the factory default credentials. 

  3. **Navigate to the Wireless Settings:**
     - This option is usually located in a main menu or sidebar. The exact navigation can vary depending on your router brand and model. Look for "Wireless," "Wireless Settings," "Wireless Setup," or something similar.

  4. **Configure your WLAN settings:**
     - Set your SSID (network name). This is the name that will be visible when searching for available wireless networks.
     - Set the Mode to "WPA2-PSK" or "WPA2 Personal" depending on your router model.
     - Enter your preferred password into the "Pre-Shared Key" or "Password" field. This should be a strong password to help protect your network.

  5. **Save your settings:**
     - Click "Save," "Apply," or similar to save your changes.
     
  6. **Test your connection:**
     - Try connecting to your WiFi network using the new SSID and password from a wireless device.

  Please note that the exact steps and terms may vary depending on the brand and model of your wireless router or access point. Always refer to the specific manual or online help pages if you're unsure.

---------------------------------------------------------------------------------------------------------
---------------------------------------------------------------------------------------------------------
---------------------------------------------------------------------------------------------------------
--------------------------------------------------------------------------------------------------------- 