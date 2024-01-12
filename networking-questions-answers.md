# Networking Interview Questions & Answers

#### 1. What is HTTP protocol?
**Answer.** The HTTP (Hypertext Transfer Protocol) is a protocol used for communication between a client and a server over the internet. It facilitates the transfer of hypertext, typically in the form of HTML documents, but can also handle various data types. HTTP operates on a request-response model, where clients send requests to servers, and servers respond with the requested information along with a status code indicating the success or failure of the request.

#### 2. Difference between router, switch?
**Answer.** A router operates at the network layer (Layer 3) and connects different networks, making routing decisions based on IP addresses. It directs traffic between networks.

A switch operates at the data link layer (Layer 2) and connects devices within the same network using MAC addresses. It forwards traffic within a local network and operates more efficiently than a hub.

#### 3. What is a Broadcast Domain?
**Answer.** A broadcast domain is a network segment where broadcast traffic is shared. Devices within the same broadcast domain can directly communicate with each other using broadcast messages. Routers typically separate broadcast domains, limiting the scope of broadcast traffic and enhancing network efficiency.

#### 4. What is DNS and TCP/UDP?
**Answer.** DNS, or Domain Name System, translates human-readable domain names into IP addresses. It operates over both TCP (Transmission Control Protocol) and UDP (User Datagram Protocol). DNS primarily uses UDP for normal query-response communication due to its lower overhead and faster performance. However, TCP is used for large responses or tasks like zone transfers where reliability is crucial.

#### 5. What is MSS/MTU?
**Answer.** MSS (Maximum Segment Size) and MTU (Maximum Transmission Unit) refer to the size of data packets in networking. MTU is the maximum size of a network layer packet, while MSS is the maximum size of a TCP segment. Adjusting MSS helps prevent fragmentation, ensuring efficient data transmission across networks with varying MTUs.

#### 6. OSI model with complete details and protocols on each layer?
**Answer.** The OSI (Open Systems Interconnection) model is a conceptual framework for understanding network interactions, divided into seven layers:
- Physical Layer: Deals with physical connection and transmission media. Protocols: Ethernet, USB, HDMI.
- Data Link Layer: Manages data framing and error detection. Protocols: Ethernet, PPP.
- Network Layer: Handles logical addressing and routing. Protocols: IP, ICMP, OSPF.
- Transport Layer: Ensures end-to-end communication and data flow control. Protocols: TCP, UDP.
- Session Layer: Manages sessions and dialog control. Protocols: NetBIOS, RPC.
- Presentation Layer: Translates data formats and ensures compatibility. Protocols: SSL/TLS, JPEG, ASCII.
- Application Layer: Provides user interfaces and network services. Protocols: HTTP, SMTP, DNS.

#### 7.TCP and SSL handshake?
**Answer.** TCP (Transmission Control Protocol) and SSL (Secure Sockets Layer, now known as TLS or Transport Layer Security) handshakes are protocols for establishing a secure communication channel:

**TCP Handshake:**
Initiation: Client sends a SYN packet to the server.
Acknowledgment: Server responds with a SYN-ACK packet.
Confirmation: Client sends an ACK packet, establishing a connection.

**SSL/TLS Handshake:**
ClientHello: Initiates the handshake by proposing supported cryptographic algorithms.
ServerHello: Server selects a compatible cipher suite and responds.
Key Exchange: Exchange of cryptographic information (public keys, etc.).
Finished: Both parties confirm the establishment of a secure connection.
These handshakes ensure a reliable, encrypted channel for data transmission.

#### 8. Difference between TCP/UDP, examples?
**Answer.** TCP (Transmission Control Protocol) is a connection-oriented protocol that provides reliable and ordered data delivery with error checking. Examples include HTTP (web browsing) and FTP (file transfer).

UDP (User Datagram Protocol) is a connectionless protocol that offers faster, but unreliable, data delivery without error checking. Examples include DNS (Domain Name System) and video streaming.

#### 9. Flow/error control?
**Answer.** Flow control manages the rate of data transmission to prevent overwhelm, ensuring efficient communication. Error control detects and corrects errors in transmitted data, maintaining data integrity. Both mechanisms are crucial for reliable and effective communication in network protocols.

#### 10. What is a firewall, why do you need it?
**Answer.** A firewall is a network security device that monitors and controls incoming and outgoing network traffic based on predetermined security rules. It acts as a barrier between a trusted internal network and untrusted external networks, helping to prevent unauthorized access, secure sensitive data, and mitigate potential cyber threats.

#### 11. What is APIPA?
**Answer.** APIPA (Automatic Private IP Addressing) is a feature in some operating systems that automatically assigns a temporary and self-configured IP address to a device when it cannot obtain one from a DHCP server. The assigned IP address is in the range 169.254.0.1 to 169.254.255.254.

#### 12. Which messages are Broadcast and Unicast in DORA? Why?
**Answer.** In the DHCP DORA process, the Discover and Request messages are broadcast because the client doesn't yet have an IP address and needs to discover available DHCP servers on the network. The Offer and Acknowledge messages are unicast because they are responses from a specific DHCP server to the client that initiated the request.

#### 13. Different types of IP Address allocations in DHCP?
**Answer.** In DHCP, there are three types of IP address allocations:

Static Allocation: IP addresses are manually assigned to specific devices based on their MAC addresses. This ensures consistency but requires manual configuration.

Dynamic Allocation: IP addresses are automatically assigned to devices from a pool managed by the DHCP server. Addresses are leased for a specific duration and may change over time.

Automatic Allocation: IP addresses are permanently assigned to devices based on their MAC addresses. The assignment is automatic, similar to dynamic allocation, but the IP addresses remain constant.

#### 14. Will my computer get the same IP address allocated every time?
**Answer.** It depends on the type of IP address allocation. In dynamic allocation, the IP address may change each time a device connects to the network. In static and automatic allocation, the device typically receives the same IP address consistently.

#### 15. Role of the Router in the separation of Broadcast Domains?
**Answer.** The router plays a key role in separating broadcast domains by forwarding traffic between different network segments. As a layer 3 device, it operates at the network layer and uses IP addresses to determine the destination of packets. Routers filter and control the flow of broadcast traffic, effectively isolating broadcast domains and reducing unnecessary network traffic.

#### 16. DNS Query Process?
**Answer.** The DNS query process involves the following steps:

- Query Initiation: The client initiates a DNS query by requesting the resolution of a domain name into an IP address.
- Local DNS Cache Check: The client checks its local DNS cache to see if the mapping is already available.
- Recursive Query: If not found, the client sends a recursive query to its configured DNS server, typically provided by the ISP.
- DNS Server Resolution: The DNS server recursively queries authoritative DNS servers until it obtains the IP address for the requested domain.
- Response: The resolved IP address is sent back through the recursive path to the client, and the result is stored in the client's local DNS cache for future use.

#### 17. What are ports and port numbers?
**Answer.** Ports are virtual endpoints for communication in a computer network. Port numbers are unique identifiers assigned to different services or processes on a device. They help direct network traffic to the correct application, facilitating communication between devices on a network.

#### 18. Do different tabs making queries in the browser use different port numbers?
**Answer.** No, different tabs in a browser typically use the same port number (usually port 80 for HTTP or port 443 for HTTPS) for making queries. Port numbers are more relevant at the transport layer, while tabs within a browser operate at the application layer and share the same network connection established by the browser.

#### 19. Packet Tracing?
**Answer.** Packet tracing involves capturing and analyzing network packets to understand the flow of data between devices. It helps diagnose network issues, optimize performance, and troubleshoot communication problems by examining the content and behavior of individual packets in a network.

#### 20. How do we check IP address and Gateway and DNS Server addresses of our device?
**Answer.** By giving 'ifconfig' command.

#### 21. Difference between network layer and transport layer?
**Answer.** The main difference between the network layer and transport layer lies in their functionalities within the OSI model:

Network Layer (Layer 3):

Responsible for logical addressing and routing of data packets between different networks.
Uses IP addresses for communication.
Examples of protocols: IP (Internet Protocol).
Transport Layer (Layer 4):

Manages end-to-end communication between devices on the same network or segment.
Ensures reliable and efficient data transfer, error detection, and flow control.
Uses port numbers for communication.
Examples of protocols: TCP (Transmission Control Protocol) for reliable communication, UDP (User Datagram Protocol) for faster but less reliable communication.




What are the HTTP method are? PUT POST DELETE GET
● What is the time complexity of merge sort?
● What are the status code are available?
● What is the difference between PUT and POST?
● What is the website cookies?
● How to check IO Usage for machine? SAR Utilities
● How to Capture and analyse Network Traffic? Tcpdump
● How to check boot logs in linux? journalctl -b
● What is the significance of SIGKILL?
● Which single will be send to OS when you run kill -9 PID command in linux? SIGKILL
How would you check whether the user has to execute permission or not?
● How do you call the HTTP request method without a browser or curl?
● What are the parameter available in the curl command?
● A different alternative and flavor for curl command?
● What happen we you run the cat command on terminal internal workflow?
● What if I got an error cat command not found what could be the possible issue?
● What if I can’t able to SSH into the remote machine? What is the possible step would
● Practical coding round java code snippet was given
Basic Networking commands like nslookup, dig, ping, traceroute.
1) Jenkins pipeline to build and run container nginx 
2) How to copy 6gb zip file from local to s3 bucket?
3) what is the maximum limit of s3 storage ?
4) s3 glacier
5) there is small team requesting u to create infrastructure of 25, So how will you define vpc cidr block?
6) 10.0.0.0/16 - how many ip address we get? How to calculate this ip addresses?
7) Write python script for aws lambda?
8) In autoscaling we have minimum capacity, max capacity and desired capacity. Is desired value is optional or mandatory to provide?
9) Why we have desired capacity option in load balancer? We have min and max capacities, So, what is the use-case to have desired capacity?
10) About AWS Lambda? Where you used in your project?
11) About Cloud formation? AWS Kinesis?
12) Daily activities and tasks?
13) About JIRA or other tools you are using in your project?

Write a program to list the function
2.to list even and odd numbers
3.to print functions
4.dict fun
5.linux environment all commands
6.as a sre what's ur roles and responsibilities
7.if iam in banglore and my datacenters are in different places how comfortable you will feel to solve this virtual machine problem??
8.terraform have u created any services??
9.what is sre??
10.which are the tools used in sre?
What actually work you will do to secure our company data??
11.what are the projects you did as a sre and what challenges you faced??
12.have you worked on cloud era and do you have knowledge on any programming language and how much u rate yourself??
