
# Week | 4 Internetworking  
## Task 1. View Routing Table
Command: Get-NetRoute  
![Image](./images/RouteTable.PNG)  

### Description  
- For sending to all devices in same network i.e local, send direct is used  
- For sending special multicast addresses that starts with 224.0.0.0/4
- Fot sending to all devices on the network 10.162.32.0, i.e. directed broadcast, send
direct.
- For sending to the device 10.162.32.74, send direct.
- For sending to anyone on the network 10.162.32.0, send direct.
- For sending to anyone in the internet, 10.162.32.1 will be used


## Task 2. IP Network Design (Partner Name: Santosh Poudel 12212716)
Small network with the following requirements is drawn below:-
1. A switched Ethernet LAN with three computers.  
2. Another switched Ethernet LAN with two computers.  
3. The two switched Ethernet LANs connected together via a 1 Gb/s Ethernet point-to-point WAN link.  
4. All three IP networks are using IPv4 with a /24 network mask.  
5. The equipment available is: 2 x 8-port Gigabit Ethernet switches; 2 x 2-port routers; 5 x PCs;
multiple LAN cables.  

| Devices       | IP            |
| ------------- | ------------- |
| Router        | 192.168.3.0   |
| LAN1-PC1      | 34.36.1.1     |  
| LAN1-PC2      | 34.36.1.2     |  
| LAN1-PC3      | 34.36.1.3     |  
| LAN2-PC1      | 27.16.1.1     |  
| LAN2-PC2      | 27.16.1.2     |  

![Image](./images/lab4task2my.png)  

c) The routing tables for each device are:-
For LAN1-PC1:
| Destination   | Next          |
| ------------- | ------------- |
| LAN1-PC3      | direct        |  
| LAN2-PC1      | Router        |  
| LAN2-PC2      | Router        |  

For LAN1-PC2:
| Destination   | Next          |
| ------------- | ------------- |
| LAN1-PC1      | direct        |  
| LAN1-PC3      | direct        |  
| LAN2-PC1      | Router        |  
| LAN2-PC2      | Router        |  

For LAN1-PC3:
| Destination   | Next          |
| ------------- | ------------- |
| LAN1-PC1      | direct        |  
| LAN1-PC2      | direct        |  
| LAN2-PC1      | Router        |  
| LAN2-PC2      | Router        |  

For LAN2-PC1:
| Destination   | Next          |
| ------------- | ------------- |
| LAN1-PC1      | Router        |  
| LAN1-PC2      | Router        |  
| LAN1-PC3      | Router        |  
| LAN2-PC2      | direct        |  

For LAN2-PC1:
| Destination   | Next          |
| ------------- | ------------- |
| LAN1-PC1      | Router        |  
| LAN1-PC2      | Router        |  
| LAN1-PC3      | Router        |  
| LAN2-PC1      | direct        |  

d) If a host on one LAN sent an ICMP packet (e.g. ping request) to a host on the other LAN, and that
packet was captured at a router, then he packet ICMP/IP will be:-  

| Ethernet Header   |
| ----------------- | 
| IP Header         |   
| ICMP Header       |  
| ICMP Data         | 

 Source and destination mac address would be in the Ethernet frame of the packet. Suppose host mac address will be source and destination will be router mac address.

## Task 3. IP Address Lookup
Using an online IP address lookup website i.e “what is my IP address” following information are captured.
![Image](./images/T4Task3.png)  


