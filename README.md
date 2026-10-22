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
<img width="1600" height="1000" alt="image" src="https://github.com/user-attachments/assets/04754ac4-a6ab-4e74-853b-dedb78ef5a04" />

 Description:<br>
•	PC0 → Switch0 → Router (FastEthernet0/0)<br>
•	PC1 → Switch1 → Router (FastEthernet0/1)<br>
(Insert screenshot of your Packet Tracer setup here)<br>
________________________________________
# IP Addressing Table
<img width="1600" height="1000" alt="image" src="https://github.com/user-attachments/assets/a9279eac-e3db-4576-a367-1f51a63c29b5" />
<img width="1600" height="1000" alt="image" src="https://github.com/user-attachments/assets/d871174a-b490-4bb9-8a09-bac7835375b7" />
<img width="1600" height="1000" alt="image" src="https://github.com/user-attachments/assets/0267f655-add4-4c1d-8273-3d8f54d98f55" />
<img width="1600" height="1000" alt="image" src="https://github.com/user-attachments/assets/4b3dda10-63eb-4cc3-84e3-d27a15b3b195" />

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
<img width="1600" height="1000" alt="image" src="https://github.com/user-attachments/assets/ac2ef519-280b-41fc-937f-e14e622121c6" />

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
<img width="1600" height="1000" alt="image" src="https://github.com/user-attachments/assets/0414204d-0ce9-4004-bc8d-d9cd4a79cd38" />
<img width="1600" height="1000" alt="image" src="https://github.com/user-attachments/assets/29dd36c9-a2a3-4fcb-8505-2fa231096b5c" />
<img width="1600" height="1000" alt="image" src="https://github.com/user-attachments/assets/8237b9ea-ba96-4b3c-af57-6838dc811cb5" />
<img width="1600" height="1000" alt="image" src="https://github.com/user-attachments/assets/45d3dd9b-6c22-49a0-9fd1-b8921eeef087" />

________________________________________
# Result
Successfully configured a router to connect two LANs. Communication between PC0 and PC1 across different networks was tested and verified.

