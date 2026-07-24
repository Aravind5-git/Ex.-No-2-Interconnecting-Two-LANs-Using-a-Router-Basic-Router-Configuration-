# Date :
## Ex.-No-2-Interconnecting-Two-LANs-Using-a-Router-Basic-Router-Configuration


# Objective
To configure a router to connect two separate LANs and enable communication between them using static IP addressing.
________________________________________
# Apparatus/Tools Required
•	Cisco Packet Tracer<br>
•	2 PCs<br>
•	2 Switches<br>
•	1 Router (e.g., 1841 or 2911)<br>
•	Straight-through cables<br>
________________________________________
# Network Topology Diagram
 Description:<br>
•	PC0 → Switch0 → Router (FastEthernet0/0)<br>
•	PC1 → Switch1 → Router (FastEthernet0/1)<br>
(Insert screenshot of your Packet Tracer setup here)<br>
________________________________________
# IP Addressing Table
Device	Interface	IP Address	Subnet Mask<br>
PC0	NIC	192.168.1.10	255.255.255.0<br>
PC1	NIC	192.168.2.10	255.255.255.0<br>
Router0	FastEthernet0/0	192.168.1.1	255.255.255.0<br>
Router0	FastEthernet0/1	192.168.2.1	255.255.255.0<br>
________________________________________
# Procedure
1.	Open Cisco Packet Tracer and add 2 PCs, 2 Switches, and 1 Router.
2.	Connect each PC to a switch, and each switch to the router using straight-through cables.
3.	Assign IP addresses to both PCs according to the IP table.
4.	Configure the router interfaces:
o	FastEthernet0/0 → 192.168.1.1
o	FastEthernet0/1 → 192.168.2.1
5.	Use no shutdown on both router interfaces to activate them.
6.	Set each PC’s default gateway:<br>
o	PC0 → 192.168.1.1<br>
o	PC1 → 192.168.2.1<br>
7.	Test connectivity using ping from PC0 to PC1.<br>
________________________________________
# Commands Used (Router CLI)
bash<br>
CopyEdit<br>
Router> enable<br>
Router# configure terminal<br>
Router(config)# interface fastethernet0/0<br>
Router(config-if)# ip address 192.168.1.1 255.255.255.0<br>
Router(config-if)# no shutdown<br>

Router(config)# interface fastethernet0/1<br>
Router(config-if)# ip address 192.168.2.1 255.255.255.0<br>
Router(config-if)# no shutdown<br>
________________________________________
# Output (Screenshots)

•	Router CLI configuration<br>

<img width="1917" height="1140" alt="image" src="https://github.com/user-attachments/assets/8e576bb5-47ec-431a-a3a2-dc761c6c472a" />

•	IP configurations on PCs<br>

<img width="1917" height="1141" alt="Screenshot 2026-07-24 110527" src="https://github.com/user-attachments/assets/1670b28a-6b4e-4892-84e7-52098410c4a5" />

<img width="1915" height="1136" alt="image" src="https://github.com/user-attachments/assets/5f77394c-72f7-4591-b17a-98ec134f96d0" />

•	Successful ping between PC0 and PC1<br>

<img width="1917" height="1142" alt="Screenshot 2026-07-24 111147" src="https://github.com/user-attachments/assets/85cfc0b8-15ad-4c44-8395-6639a2766006" />

________________________________________
# Result
Successfully configured a router to connect two LANs. Communication between PC0 and PC1 across different networks was tested and verified.

