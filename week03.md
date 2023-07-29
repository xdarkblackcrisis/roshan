# Week 3 | Network Technologies
## Task 1. View ARP Table
ARP table  
![Image](./images/arptable.PNG)

Ping Neighbour Computer  
![Image](./images/ping_neghbour.PNG)

Neighbour Computer Mac Address  
arp -a  
![Image](./images/neg_mac.PNG)  

## Task 3. Design a Small Network (Partner Name: Santosh Poudel)
### Network Diagram  
![Image](./images/w3q3.drawio.png)

### Explanation of the design
This is simple network design for installing security cameras of two types with old power input of 4 Cameras 720p, 10fps with  100 Mb/s Ethernet NICs and PoE 6 Cameras 1080p, 25 fps with  100 Mb/s Ethernet NICs. This Camera setting can store videos and handle adminstration. Two different types of switches are selected to configure two varities of camera. One router to connect internet and remote access is added.

### Table listing equipment to be purchased
1. Personal Computer 
2. Storage Device
3. Router
4. Switch
5. PoE Switch
6. Ethernet Cable
7. 4 Cameras 720p, 10fps with  100 Mb/s Ethernet NICs
8. 6 Cameras 1080p, 25 fps with  100 Mb/s Ethernet NICs


### For calculating the throughput requirement for the video streams, we have to find the bandwidth required for each camera and sum the total.

For the new cameras bandwidth requirement is as follows:

Required Bandwidth for one new camera = Bitrate x Compression Ratio = 6.75 Mb/s

Total bandwidth for six new cameras = 6 x 6.75 Mb/s = 40.5 Mb/s

Similarly, Bandwidth required for one old camera = Bitrate x Compression Ratio = 1.5 Mb/s

Total bandwidth for four older cameras = 1.5 Mb/s x 4 = 6 Mb/s

Thus, overall requirement of throughput for video streams = 40.5 Mb/s + 6 Mb/s = 46.5 Mb/s.  

## Reflection
From this tutorial I learnt about drawing the network diagram, use of router, switch and calculate the throughput.
