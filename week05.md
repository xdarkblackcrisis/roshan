# Week | 5 Internet Applications  
## Task 1. Create Web Pages in OpenWRT
![Image](./images/lab5task1ui.PNG) 
![Image](./images/lab5task1index.PNG) 
![Image](./images/lab5task1id.PNG) 
![Image](./images/lab5task1css.PNG)   

## Task 2. Capture HTTP Packets  
![Image](./images/lab5task2packet.PNG)

## Task 3. Analyse HTTP Packet Capture  
a) The explanation for the HTTP request/response is provided below:

After the user opened the webpage on the web server, the first request is triggered. Initial response was requested for root directory and the response was an HTTP response with the 200 status code, showcasing expected outcome.  
The triggering of second request was done when the user browser tried to retrieve the mystyle.css (stylesheet) in previous request. HTTP 304 Not Modified status code was responded by server as there was no modification in the requested resource since the last request.
The triggering of third request was done when the user tried to retrieve mystyle.css stylesheet. HTTP response with a status code of 200 was the response observed showcasing successful response.
The fourth request was observed for the newly created web page and the triggering occured when the user browser requested the page. HTTP 200 OK status code was the response provided by server which indicated successful response.

b) The five address values which identify the application, transport protocol, and host for the first HTTP request/response are:

Applicaton: HTTP
Transport Protocol: TCP
Hosts: 192.168.56.1 (source) and 192.168.56.2 (destination)

c) The outcome depends on the button implementation. The browser doesn't need to send a request to web server if the button is programmed to retrieve the information regarding date and time from the client side (i.e., JavaScript running on browser) while there is need for the browser to send the request to web server if the programming is done for the button to retrieve date and time information from the server side.

d) For the newly created web page(e.g., 12212716.html), the packet diagram might look like below:

HTTP Request Packet:
---------------------
- Source Address: 192.168.56.1
- Destination Address: 192.168.56.2
- Source Port: 1234
- Destination Port: 80
- HTTP Method: GET
- Request URI: /12212716.html
- HTTP Version: 1.1
- Host: 192.168.56.2
- User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/94.0.4606.61 Safari/537.36
- Accept: */*
- Accept-Encoding: gzip, deflate, br
- Connection: keep-alive
- Referer: http://192.168.56.2/
- Cookie: (optional)
- Content-Length: 0 (optional)

The size of request URi and the length of the headers will determine the size of the HTTP request packet. For example, if the headers are 200 bytes long and the request URI is 50 bytes long, then the total size of the HTTP request packet would be 250 bytes.

![Network](./images/packetdiagram.jpg)

e) The URL of the web page linked to the requested resource is identified by the value of the referrer header in the HTTP request. "http://192.168.56.2/" is the referrer header in this case which identifies web server root directory. The flow of traffic to their respective websites can be tracker based on this information by the web servers.

f) By examining the user-agent header in the request, the information used to make HTTP request by the web browser can be learned by server. Mozilla is the user-agent string in the provided case.

g) HTTP version used cannot be determined from the captured packets as the information is contained in the HTTP protocol header which was not captured in this case. However, it is observed that TCP is the transport protocol used.

h) Three-way handshake packets are the packets involved in the connection setup which ensures reliable connection between the server and client before any data transfer takes place. These packets are:

Packet 1: SYN packet sent from the client to the server, with the SYN flag set and an initial sequence number.
Packet 2: SYN-ACK packet sent from the server to the client, with both the SYN and ACK flags set, as well as an acknowledgment number and a new sequence number.
Packet 3: ACK packet sent from the client to the server, with the ACK flag set and an acknowledgment number.
The time taken between the start of connection setup and the data transfer starting is the time between the timestamp of the SYN packet (packet 1) and the timestamp of the first HTTP request packet (packet 10).

i) Acknowledgements (ACK packets) are sent by the receiver to acknowledge receipt of data packets sent by the sender. In TCP, acknowledgements are typically sent for every other packet received, so that the receiver can signal that it has received all packets up to that point and is ready to receive the next packet. In the captured packets, we can see ACK packets sent by the receiver after each packet sent by the sender, indicating that the receiver has successfully received the packet.
  
## Task 4. View Your Cookies  
I visit www.github.com site regularly. I have included partial screenshot. It stores several information about user and browser. A cookie is a small data file that is sent from a website to the device, and stored on its browser. It stores unique user id or device id, color mode of browser, location of the user, user session, logged in status, username, cookies setting etc.
![Image](./images/cookie.PNG)   
