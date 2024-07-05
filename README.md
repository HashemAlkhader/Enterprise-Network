# Enterprise-Network

![image](https://github.com/HashemAlkhader/CAN/assets/56479179/c982bf65-ae17-4688-8b56-84612e9ae4d8)

1. Introduction
This document provides a comprehensive overview of the enterprise network designed using Cisco Packet Tracer. The network integrates various technologies and protocols to ensure robust connectivity, security, and performance.
2. Network Topology
Overview
•	Type: Enterprise Network
•	Topology: Hierarchical
3. Network Protocols
OSPF Configuration
•	Area 0:
o	Routers: R1, R2, R3, R4
o	Configuration on R1:
router ospf 10
router-id 1.1.1.1
 network 10.10.10.0 0.0.0.255 area 0
 network 11.11.11.0 0.0.0.3 area 0
 network 12.12.12.0 0.0.0.3 area 0

o	Configuration on R2:
router ospf 10
router-id 2.2.2.2
 network 10.10.10.0 0.0.0.255 area 0
 network 13.13.13.0 0.0.0.3 area 0
 network 12.12.12.0 0.0.0.3 area 0

o	Configuration on R3:
router ospf 10
router-id 3.3.3.3
 network 10.10.10.0 0.0.0.255 area 0
 network 11.11.11.0 0.0.0.3 area 0
 network 14.14.14.0 0.0.0.3 area 0



o	Configuration on R4:
router ospf 10
router-id 4.4.4.4
 network 10.10.10.0 0.0.0.255 area 0
 network 13.13.13.0 0.0.0.3 area 0
 network 14.14.14.0 0.0.0.3 area 0
 network 15.15.15.0 0.0.0.3 area 0
 network 16.16.16.0 0.0.0.3 area 0
 network 17.17.17.0 0.0.0.3 area 0
 network 18.18.18.0 0.0.0.3 area 0
•	Area 1:
o	Routers: R9, R10, R20, R19
o	Configuration on R9:
router ospf 10
router-id 5.5.5.5
 network 15.15.15.0 0.0.0.3 area 1
 network 28.28.28.0 0.0.0.3 area 1
 network 29.29.29.0 0.0.0.3 area 1
o	Configuration on R10:
router ospf 10
router-id 6.6.6.6
 network 16.16.16.0 0.0.0.3 area 1
 network 27.27.27.0 0.0.0.3 area 1
 network 31.31.31.0 0.0.0.3 area 1
o	Configuration on R19:
router ospf 10
router-id 11.11.11.11
network 29.29.29.0 0.0.0.3 area 1
network 31.31.31.0 0.0.0.3 area 1

o	Configuration on R20:
router ospf 10
router-id 12.12.12.12
network 28.28.28.28 0.0.0.3 area 1
network 27.27.27.27 0.0.0.3 area 1
•	Area 2:
o	Routers: R11, R12, R17, R18
o	Configuration on R11:
router ospf 10
router-id 7.7.7.7
 network 17.17.17.0 0.0.0.3 area 2
 network 20.20.20.0 0.0.0.3 area 2
 network 23.23.23.0 0.0.0.3 area 2
o	Configuration on R12:
router ospf 10
router-id 8.8.8.8
 network 18.18.18.0 0.0.0.3 area 2
 network 21.21.21.0 0.0.0.3 area 2
 network 22.22.22.0 0.0.0.3 area 2
o	Configuration on R17:
router ospf 10
router-id 9.9.9.9
network 20.20.20.0 0.0.0.3 area 2
network 21.21.21.0 0.0.0.3 area 2
network 25.25.25.0 0.0.0.3 area 2
o	Configuration on R18:
router ospf 10
router-id 10.10.10.10
network 22.22.22.0 0.0.0.3 area 2
network 23.23.23.0 0.0.0.3 area 2
network 25.25.25.0 0.0.0.3 area 2
EIGRP Configuration
•	AS Number: 100
•	Routers: R13, R14, R15, R16
o	Configuration on R13:
router eigrp 20
 network 19.19.19.0 0.0.0.3
 network 20.20.20.0 0.0.0.255
 network 21.21.21.0 0.0.0.3
 network 22.22.22.0 0.0.0.3
o	Configuration on R14:
router eigrp 20
 network 20.20.20.0 0.0.0.255
 network 21.21.21.0 0.0.0.3
 network 23.23.23.0 0.0.0.3
o	Configuration on R15:
router eigrp 20
 network 20.20.20.0 0.0.0.255
 network 22.22.22.0 0.0.0.3
 network 24.24.24.0 0.0.0.3
o	Configuration on R16:
router eigrp 20
 network 20.20.20.0 0.0.0.255
 network 23.23.23.0 0.0.0.3
 network 24.24.24.0 0.0.0.3
 network 65.65.65.0 0.0.0.255
 network 70.70.70.0 0.0.0.255
RIP Configuration
•	Version: 2
•	Routers: R17, R18, R19, R20
o	Configuration on R17:
router rip
 version 2
network 20.20.20.0 
network 21.21.21.0 
network 25.25.25.0 
o	Configuration on R18:
router rip
 version 2
network 22.22.22.0 
network 23.23.23.0 
network 25.25.25.0
o	Configuration on R19:
router rip
 version 2
network 29.29.29.0 
network 31.31.31.0 
o	Configuration on R20:
router rip
 version 2
network 28.28.28.28 
network 27.27.27.27 
Static Routing
•	Routers: R16
o	Configuration on R16:
ip route 0.0.0.0 0.0.0.0 20.20.20.1
4. Network Services
DHCP
•	Server: DHCP Server1
o	Configuration:
ip dhcp pool VLAN10
 network 192.168.99.0 255.255.255.0
 default-router 192.168.99.1
 dns-server 192.168.10.10

ip dhcp pool VLAN30
 network 192.168.70.0 255.255.255.0
 default-router 192.168.70.1
 dns-server 192.168.10.10
•	Server: DHCP Server2
o	Configuration:
ip dhcp pool VLAN20
 network 192.168.98.0 255.255.255.0
 default-router 192.168.98.100
 dns-server 192.168.200.10

ip dhcp pool TOWER
 network 192.168.200.0 255.255.255.0
 default-router 192.168.200.100
 dns-server 192.168.200.10
•	Server: DHCP Server3
o	Configuration:
ip dhcp pool VLAN10
 network 192.168.50.0 255.255.255.0
 default-router 192.168.50.100
 dns-server 192.168.50.10

ip dhcp pool VLAN20
 network 192.168.3.0 255.255.255.0
 default-router 192.168.3.100
 dns-server 192.168.50.10
•	Server: DHCP Server4
o	Configuration:
ip dhcp pool VLAN20
 network 192.168.6.0 255.255.255.0
 default-router 192.168.6.100
 dns-server 192.168.30.10


FTP
•	Server: FTP Server
o	IP Address: 192.168.10.10, 192.168.200.10, 192.168.50.10, 192.168.30.10
o	Configuration:
ip ftp server enable
NTP
•	Server: NTP Server
o	Configuration:
ntp server 192.168.10.10
Email
•	Server: Email Server
o	Configuration:
email server enable
5.VLAN Configuration
•	VLAN 10: Management (192.168.99.0/24)
•	VLAN 20: Sales (192.168.98.0/24)
•	VLAN 65: Call Center (65.65.65.0/24)
•	VLAN 70: IT (70.70.70.0/24)
6. Security
Port Security
•	Switch: SW6, SW7, SW8, SW9, SW10, SW11, SW12, SW13, SW14
o	Configuration:
interface range FastEthernet0/5-6
 switchport mode access
 switchport port-security
 switchport port-security maximum 2
 switchport port-security violation restrict
 switchport port-security mac-address sticky
7. EtherChannel
•	Switches: SW1, SW2, SW6, SW7, SW8, SW9, SW10, SW11, SW12, SW13, SW14, SW15, SW16, SW17, SW18
o	Configuration on SW2:
interface Port-channel1
 switchport mode trunk
!
interface FastEthernet0/1
 channel-group 1 mode active
!
interface FastEthernet0/2
 channel-group 1 mode active
8. IP Phone Configuration
•	Switch: SW19
o	Configuration:
interface FastEthernet0/3
 switchport mode access
 switchport voice vlan 65
9. IoT Configuration
•	Devices: Cameras
o	Configuration:
ip address dhcp
10. 3G/4G Cellular Data Service
•	Device: Cellular Router
o	Configuration:
interface Cellular0/0/0
 ip address negotiated
12. Appendices
Device Inventory
•	Routers: cisco 2911
•	Switches: cisco 2960 and cisco catalyst 3650
•	Servers: DHCP, NTP, IOT, FTP, DNS, Email Server

