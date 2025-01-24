# Basic-Network-Architecture-for-Companies

Computer Networks and Design ProjectThis project was developed to design, implement, and establish the network infrastructure of a textile company, and also to serve as a guide for companies in different fields.
Project ObjectivesEstablishing a central network infrastructure.
Ensuring communication between different branches.
Optimizing network traffic using VLAN and routing techniques.
Applying security policies using ACL (Access Control List).
Ensuring the proper functioning of DNS and web servers.
Project StructureThe project consists of the following components:
1. TopologyHead Office (Ankara):
Multilayer Switch (Core Switch)
DNS Server
Head Office Router
Edge Switch 1 and Edge Switch 2
Izmir Branch:
Izmir Router
Izmir Switch
Izmir Client PC
Konya Branch:
Konya Router
Konya Switch
Konya Client PC
Antalya Workshop:
Antalya Router
Antalya Client PC
2. VLAN StructureEach network device is assigned a specific VLAN, segmenting network traffic and enhancing security.
VLAN 34: Management PCs (172.34.34.0/24)
VLAN 50: User PCs (172.34.50.0/24)
VLAN 80: Servers (172.34.80.0/24)
VLAN 99: Guest PCs (172.34.99.0/24)
VLAN 15: DNS Server (15.15.15.0/24)
VLAN 16: Web Server (16.16.16.0/24)
3. RoutingStatic routing and the OSPF routing protocol were used to manage traffic between the head office and branches.
Head Office Router - Antalya Router: Static Route (25.0.0.0/30)
Head Office Router - Auxiliary Router: Static Route (12.0.0.0/30)
Auxiliary Router - Izmir and Konya Routers: Routing via OSPF
4. ACL (Access Control List)The following ACL rules were applied for network security:
Guest PCs: Limited access to specific networks.
User PCs: Full access to all networks, with ping restrictions applied.
Izmir and Konya branches: Cannot ping each other.
5. ServersDNS Server:
IP Address: 15.15.15.10
Resolves queries for google.com.
Web Server:
IP Address: 16.16.16.10
Provides access to web pages for users.
6. Access TestsThe Head Office User PC can ping all IPs except for the Guest PC.
The Izmir Client PC cannot ping the Konya Client PC.
Configuration StepsVLAN Configuration:
VLANs were defined, and each port was assigned to the appropriate VLAN.
IP Addressing:
All devices were assigned IP addresses, and subnet masks were configured.
Routing:
Static and OSPF routing protocols were implemented.
ACL Applications:
Access restrictions were defined using ACL.
Server Setup:
DNS and Web servers were configured.
UsageTo review this project on your own computer, install Cisco Packet Tracer and open the project file (.pkt). Example scenarios and tests are defined within the project.
Project FilesProject Report: ReportFile.docx
Project Topology File: Project.pkt
