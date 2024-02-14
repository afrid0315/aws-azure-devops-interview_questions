# Networking Interview Questions & Answers

#### 1. What is HTTP protocol and explain PUT POST DELETE GET?
**Answer.** The HTTP (Hypertext Transfer Protocol) is a protocol used for communication between a client and a server over the internet. It facilitates the transfer of hypertext, typically in the form of HTML documents, but can also handle various data types. HTTP operates on a request-response model, where clients send requests to servers, and servers respond with the requested information along with a status code indicating the success or failure of the request.

**PUT:** Used to update or create a resource on the server. The data sent with a PUT request typically replaces the existing resource or creates a new one if it doesn't exist.

**POST:** Used to submit data to be processed to a specified resource. It is often used to create new resources, and the server assigns a URI to the new resource.

**DELETE:** Used to request the removal of a resource on the server. After a successful DELETE request, the resource is no longer available.

**GET:** Used to retrieve data from a specified resource. It should not have any side effects on the server and is considered a safe and idempotent operation, meaning multiple identical requests should have the same effect as a single request.

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

**Network Layer (Layer 3):**
Responsible for logical addressing and routing of data packets between different networks.
Uses IP addresses for communication.
Examples of protocols: IP (Internet Protocol).

**Transport Layer (Layer 4):**
Manages end-to-end communication between devices on the same network or segment.
Ensures reliable and efficient data transfer, error detection, and flow control.
Uses port numbers for communication.
Examples of protocols: TCP (Transmission Control Protocol) for reliable communication, UDP (User Datagram Protocol) for faster but less reliable communication.

#### 22. What is the port of Sonarkube, SQL, DNS and others?
**Answer.** - 
- Sonarkube starts with the port 9000, 
- SQL starts with the port 3306,
- DNS port number is 53.
- RDP port number is 3389.
- SSH port number is 22.
- HTTP port number is 80.
- HTTPS port number is 443.
- Apache Tomcat port number is 8080.
- Jenkins port number is 8080.
- FTP(File Transfer Protocol): Port 21
- DHCP(Dynamic Host Configuration Protocol): Ports 67 (server) and 68 (client)

#### 23. What is the time complexity of merge sort?
**Answer.** The time complexity of merge sort is O(n log n), where "n" is the number of elements in the array that is being sorted.

#### 24. What are the status code are available?
**Answer.** Here are some common HTTP status codes:

- 200 OK (Success)
- 404 Not Found (Resource not found)
- 500 Internal Server Error (Server error)
- 401 Unauthorized (Authentication required)
- 403 Forbidden (Access denied)
- 301 Moved Permanently (Resource has moved)
- 302 Found (Resource temporarily moved)
- 204 No Content (Request successful, no additional content)

#### 25. What is the website cookies?
**Answer.** Website cookies, or HTTP cookies, are small pieces of data sent by a website and stored on a user's device. They serve various purposes, such as remembering user preferences and maintaining user sessions, enhancing the overall browsing experience.

#### 26. How to Capture and analyse Network Traffic?
**Answer.** Use tools like 'Wireshark' or 'tcpdump' to capture network packets.

#### 27. What is the purpose of the ping command in Linux, and how do you test network connectivity to a remote host?
**Answer.** Ping command is used to test the network connectively between the local and remote hosts. It basically sends an ICMP echo request packet to the remote host and waits for the corresponding echo reply packet.

For example: If we want to check the connectivity to a remote host, we use the following command.

`ping remote_host_ip`

Here replace `remote_host_ip` with the Ip address of the host.



#### 28. What is the purpose of the netstat command in Linux, and how do you view network connections and listening ports?
**Answer.** The netstat command in Linux is used to display active network connections, routing tables, and listening ports. To view network connections and listening ports, use the netstat command with appropriate options. 

For example: If we want to display all listening TCP ports, we can use the following command.

`netstat -tuln`

#### 29. Explain DHCP DORA Process.
**Answer.**  The DHCP (Dynamic Host Configuration Protocol) DORA process is a series of steps that a device goes through when it requests and obtains an IP address from a DHCP server. DORA stands for Discover, Offer, Request, and Acknowledge, representing the four main steps in the DHCP process.

**Discover (D):**
The DHCP client (usually a computer or network device) begins the process by sending a DHCP Discover message to the local network. This message is a broadcast packet, meaning it is sent to all devices on the network.
The purpose of the Discover message is for the client to find available DHCP servers and obtain configuration information.

**Offer (O):**
When a DHCP server receives a Discover message, it responds with a DHCP Offer message. This message is a unicast packet, sent directly to the DHCP client.
The Offer message includes an IP address that the server is willing to lease to the client, along with other configuration parameters such as subnet mask, default gateway, DNS server, and lease duration.

**Request (R):**
After receiving one or more Offer messages, the DHCP client selects one of the offers and sends a DHCP Request message back to the chosen DHCP server.
The Request message indicates the client's acceptance of the offered IP address and requests the server to reserve that address for the client.

**Acknowledge (A):**
Upon receiving the Request message, the DHCP server sends a DHCP Acknowledge message to the client, confirming that the requested IP address has been reserved for the client's use.
The Acknowledge message also includes any additional configuration information and the duration of the lease.
After the Acknowledge step, the DHCP client configures its network interface with the provided IP address and other parameters. The client will use this leased IP address until the lease expires, at which point it may need to renew the lease by going through the DHCP process again.

#### 30. How do you check which ports are listening?
**Answer.** Checking Listening Ports:
- Use netstat -tulpn or ss -tulpn to display listening ports.
- Alternatively, use lsof -i to list open ports and associated processes.
- nmap can scan for open ports on a remote system.

#### 31. How do PING and TRACERT commands work?
**Answer.** PING (Packet Internet Groper) sends ICMP Echo Request packets to a destination IP address. When the target receives the packet, it responds with an ICMP Echo Reply. The round-trip time is measured, providing information about network latency and reachability.

TRACERT (Traceroute) traces the route that packets take to reach a destination. It sends packets with increasing TTL (Time To Live) values, causing routers along the path to respond with ICMP Time Exceeded messages. This helps identify the routers in the network path and measure the round-trip time to each hop, aiding in network troubleshooting.

#### 32. How to check a particular port is open or no
**Answer.** You can check if a particular port is open using the telnet command or nc (netcat) command.``telnet hostname_or_ip port_number or telnet example.com 80``

#### 33. Use of Traceroute & Nslookup command.
**Answer. Traceroute Command:**
traceroute is used to trace the route that packets take from your computer to a destination, showing the network hops in between.
It helps diagnose network connectivity issues and identify delays.

**Nslookup Command:**
nslookup is a command-line tool for querying DNS (Domain Name System) to obtain domain name or IP address information.
It is used to troubleshoot DNS-related issues, verify DNS records, and gather information about a domain.

#### 34. what type of DNS record would be queried in order to send mail to domain?
a. CNAME record       b. SMTP record
c. MX record          d. NS record
**Answer.** c. MX record

#### 35. Which iptables action will send a response back to the source host?
a. ACCEPT               b. DROP
C. ALLOW                D. REJECT

**Answer.** a. ACCEPT

#### 36. What command will I have to use to give the following permissions on a file in Linux -rw-rw-r--?
a. chown 664        b. chmod 644
c. chown 644        d. chmod 664

**Answer.** d. chmod 664

#### 37. Which of the following services ake use of the UDP procotol (Select two)
a. SSH    b. FTP   c. TFTP       d. DNS

**Answer.** c. TFTP, d. DNS

#### 38. A device ina subnet needs to send a packet to a device in a different subnet. To which device will it address the outgoing packet?
a. it'll address the packet to its configure default gateway.
b. it'll address the packet to destination IPV4 address 0.0.0.0
c. it'll address the packet to any router on the local subnet
d. it'll address the packet to the switch on the local subnet.

**Answer.** a. it'll address the packet to its configured default gateway.

#### 39. which layer of the OSI model is most is directly impacted when an Internet Service Provider is found to be blocking UDP traffic froma source host?
a. Data Link         b. Transport
c. Network           d. Session

**Answer.** b. Transport

#### 40. Your web server becomes inaccessible via the network. You run a packet capture and notice that there are thousands of new TCP connections being made from different IP addresses. What would the cause most likely be?
a. IP Flood.
b. ARP protcol
c. pING FLOOD
D. SYN flood

**Answer.** D. SYN flood

#### 41. Which two of the following network protocols do not use TCP?
a. HTTP       B. FTP     C. DHCP      D. ICMP

**Answer.** c. DHCP, d. ICMP

#### 42. Your are experiencing outbound network connectivity problems. Which devices would you crack to determine if the network settings have issues?
a. the default gateway.
b. the DNS server.
c. source host
d. all responses are correct.

**Answer.** d. all responses are correct.

#### 43. Transmission of messages between layers
**Answer.** Messages are transmitted between layers in a networking protocol stack through a process called encapsulation and decapsulation. Each layer adds its own header and possibly trailer to the data received from the upper layer before passing it down, and removes this added information upon receiving data from the lower layer.

#### 44. How is a hub, a router, and a switch different from each other? Explain in terms of broadcast domain.
**Answer.** A hub operates at the physical layer and broadcasts all incoming packets to all other ports, effectively creating a single collision and broadcast domain. A router operates at the network layer and separates broadcast domains by default, as it forwards packets between different IP subnets. A switch operates at the data link layer and maintains a separate collision domain for each port, but may have multiple ports within a single broadcast domain.

#### 45. What is the difference between Bandwidth, Delay and Latency?
**Answer.** Bandwidth refers to the maximum data transfer rate of a network connection, measured in bits per second. Delay is the time it takes for data to travel from the source to the destination, affected by factors such as network congestion and distance. Latency is the time delay between the sending and receiving of data packets, often caused by processing, queuing, and transmission delays in network devices.

#### 46. TCP/IP,BGP.
**Answer.** TCP/IP (Transmission Control Protocol/Internet Protocol) is a suite of communication protocols used to interconnect network devices on the internet. BGP (Border Gateway Protocol) is an exterior gateway protocol used to exchange routing information between different autonomous systems on the internet.

#### 47. What is BGP and describe the states - Idle, Connect, Active, Opensent, Openconfirm, Established.
**Answer.** BGP has several states including Idle, Connect, Active, Opensent, Openconfirm, and Established. In the Idle state, BGP has not established a connection with any peers. In the Connect state, BGP attempts to establish a TCP connection with a peer. In the Active state, BGP is actively trying to initiate a TCP connection. In the Opensent state, BGP has sent an OPEN message and is waiting for a response. In the Openconfirm state, BGP has received an OPEN message and sent a response. In the Established state, BGP has successfully established a neighbor relationship and can exchange routing information.

#### 48. Why the TCP/IP model used over OSI model?
**Answer.** The TCP/IP model is used more commonly in practical networking implementations than the OSI model because it is simpler, more widely adopted, and better suited to the decentralized nature of the internet.

#### 49. TCP and SSL handshake. How TCP/ IP connection is established (via 3-way handshake) and terminated?
**Answer.** The TCP/IP connection is established using a three-way handshake: SYN, SYN-ACK, and ACK. SSL (Secure Sockets Layer) handshake occurs before the TCP handshake in a secured connection. It involves a series of steps, including negotiation of encryption algorithms and exchange of cryptographic keys, to establish a secure communication channel.

#### 50. What is SSL and how does it work? How do you protect a website?
**Answer.** SSL (Secure Sockets Layer) is a cryptographic protocol used to secure communication over a computer network. It works by encrypting data transmitted between the client and server, preventing unauthorized access to sensitive information. To protect a website using SSL, an SSL certificate is installed on the web server, enabling HTTPS (HTTP Secure) protocol for secure communication between the client's browser and the server.

#### 51. How DHCP server is uniquely identified by the client?
**Answer.** A DHCP server is uniquely identified by its IP address, which is configured on the client devices as part of the network settings. When a client device needs to obtain an IP address dynamically, it sends a DHCP discover message to the network, and any DHCP server on the network with an available IP address pool can respond.

#### 52. As MSS was explained in TCP 3 way handshake, explain what is MTU and compare and contrast MSS and MTU together.
**Answer.** MSS (Maximum Segment Size) is the maximum amount of data that can be sent in a single TCP segment, while MTU (Maximum Transmission Unit) is the largest packet size that can be transmitted over a network. MSS is a parameter negotiated during TCP connection establishment, whereas MTU is determined by the underlying network technology. MSS is specific to TCP, while MTU applies to all network protocols.

#### 53. Why would you choose HTTPS over HTTP? From a technical perspective, what is HTTPS?
**Answer.** HTTPS (HTTP Secure) is preferred over HTTP (Hypertext Transfer Protocol) for secure communication over the internet. HTTPS encrypts data transmitted between the client and server, providing confidentiality, integrity, and authentication, whereas HTTP transmits data in plaintext, making it vulnerable to eavesdropping and tampering.

#### 54. What is FTP? what kind of application it used for?
**Answer.** FTP is a network protocol used for transferring files between a client and server on a computer network. It provides a standard set of commands for accessing, downloading, uploading, and managing files on a remote server. FTP is commonly used for website maintenance, file sharing, and data backup.

#### 55. How would you secure a website?/How would you make a website secure?
**Answer.** To secure a website, various measures can be taken including implementing HTTPS encryption, keeping software and plugins updated, using strong and unique passwords, restricting access to sensitive directories, enabling web application firewalls, implementing security headers, regularly scanning for malware, and performing security audits.

#### 56. How does a web page load, what happens in the background?
**Answer.** When a web page is loaded, the client's browser sends a request to the web server hosting the page. The server processes the request, retrieves the necessary files (HTML, CSS, JavaScript, images, etc.), and sends them back to the client's browser. The browser then renders the content received, displaying the web page to the user.

#### 57. What is DNS? How does DNS work?
**Answer.** DNS is a decentralized naming system used to translate domain names (e.g., www.example.com) into IP addresses (e.g., 192.0.2.1) on the internet. It enables users to access websites using human-readable domain names instead of numeric IP addresses. DNS works through a distributed hierarchy of servers, including recursive resolvers, authoritative name servers, and root servers.

#### 58. DNS resolving ( how to resolve name to IP or what happen when you vist amazon.com)
**Answer.** DNS resolution is the process of converting a domain name (e.g., www.example.com) into an IP address (e.g., 192.0.2.1) through the Domain Name System. It involves querying DNS servers recursively or iteratively until the corresponding IP address is found and returned to the client.

#### 59. Describe DNS lookup process for Domain name resolution.
**Answer.** DNS lookup process involves several steps including checking the local cache for the requested domain name, querying the recursive resolver, which in turn queries authoritative name servers, root servers, and other DNS servers as necessary to resolve the domain name to its corresponding IP address.

#### 60. What is the difference between "Connection Refused" and "Connection Timed Out"? What causes these two things to happen?
**Answer.** "Connection Refused" error occurs when the server actively rejects the connection request, often due to firewall rules or service not running on the specified port. "Connection Timed Out" error occurs when the client's request doesn't receive a response from the server within a specified time period, possibly due to network congestion, server overload, or misconfiguration.
 
#### 61. Is 1.1.1.1 routable?
**Answer.** Yes, 1.1.1.1 is a routable IP address assigned to a public DNS resolver operated by Cloudflare.

#### 62. Concept of Proxy and firewall? Stateless and stateful firewalls?
**Answer.** A proxy acts as an intermediary between clients and servers, forwarding requests and responses between them. A firewall is a network security device that monitors and controls incoming and outgoing traffic based on predetermined security rules. Stateful firewalls keep track of the state of active connections, while stateless firewalls filter packets based on individual packet attributes.

#### 63. What is the difference between example.com and example.org?
**Answer.** example.com and example.org are both generic top-level domain names used for illustrative purposes in documentation and testing. They are reserved by the Internet Assigned Numbers Authority (IANA) and are not associated with any specific organization or entity. 

#### 64. Trouble shoot slow website.
**Answer.** To troubleshoot a slow website, you can analyze factors such as server performance, network latency, website configuration, content delivery, database queries, caching mechanisms, and third-party services. Tools like web performance testing, monitoring, profiling, and analytics can help identify and resolve bottlenecks.

#### 65. How to view network stats?
**Answer.** Network statistics can be viewed using various tools and commands such as netstat, ifconfig, ip, nmap, tcpdump, wireshark, and SNMP (Simple Network Management Protocol). These tools provide information about network interfaces, connections, traffic, protocols, and performance metrics.

#### 66. What does NetStat do? Which Linux command finds routing tables?
**Answer.** NetStat (Network Statistics) command displays network connections, routing tables, interface statistics, masquerade connections, and multicast memberships. The Linux command for finding routing tables is ip route or route -n.

#### 67. Command to track and print the path traversed between different routers.
**Answer.** The traceroute command can be used to track and print the path traversed between routers. It sends packets with increasing TTL (Time-To-Live) values and displays the IP addresses of routers along the path until reaching the destination.

#### 68. What command checks the routing table in Linux?
**Answer.** The ip route command is used to check the routing table in Linux. It displays the kernel's routing table, including network destinations, gateways, interfaces, and metrics.
 
#### 69. How to setup remote desktop connection using command line in windows
**Answer.** To set up a remote desktop connection using the command line in Windows, you can use the mstsc command followed by the target remote desktop server's IP address or hostname.

#### 70. A scenario question about packet flow in NAT
**Answer.** Network Address Translation (NAT) translates private IP addresses to public IP addresses and vice versa to enable communication between devices on different networks. In a NAT scenario, packets flow from the source device's private IP address through the NAT device, which translates the source address to a public IP address before forwarding the packet to the destination.
 
#### 71. How do you find out what your IP Address is?
**Answer.** You can find out your IP address by using commands like ipconfig or ifconfig on Windows and Linux respectively, or by visiting websites that display your public IP address.

#### 72. What protocol is used and how it is used to gate out from private network.(ARP)?
**Answer.** ARP (Address Resolution Protocol) is used to map IP addresses to MAC addresses on a local network. It resolves the IP address of a device to its corresponding MAC address by broadcasting ARP request packets and receiving ARP reply packets from the target device.

#### 73. Given the following information: 10.0.0.0/8 100,000 hosts on network There is a host with an IP of 10.0.0.1 who cannot connect, why is this? Also, a lot of hosts on the network are reporting that they cannot connect, why is this?
**Answer.** If a host with an IP address of 10.0.0.1 cannot connect to the network, it may be due to incorrect network settings, misconfigured firewall rules, or network congestion. If multiple hosts on the network are experiencing connection issues, it could indicate a larger network problem such as a router or switch failure, IP address conflicts, or DNS resolution issues.

#### 74. Suppose I have a brand new laptop and I wish to connect it to the internet. What should I do, and what shall happen in background before the laptop is connected to the internet? (Ans. Manually assigning IP address or DHCP and DORA procedure. They expect you to explain in depth about DHCP and DORA)
**Answer.** To connect a laptop to the internet, you can manually assign an IP address or configure the laptop to obtain an IP address automatically using DHCP (Dynamic Host Configuration Protocol). The laptop communicates with the DHCP server using the DORA (Discover, Offer, Request, Acknowledge) process to obtain network configuration settings.

#### 75. What exactly are the requirements to make two computers communicate (they are close to each other, connected to same network) (here, also highlight the fact that how one computer will uniquely identify the other computer)
**Answer.** Two computers can communicate when they are connected to the same network and have unique IP addresses within that network. Communication between computers is facilitated by routing packets based on their destination IP addresses.
 
#### 76. Concept of public and private IPs? Can two systems connected to same network have the same public IPs? How conflict is resolved in that case?
**Answer.** Public IPs are globally unique IP addresses assigned to devices on the internet, while private IPs are used for internal communication within a local network. Two systems connected to the same network can have the same public IP address if they are behind a NAT device, which translates their private IP addresses to the single public IP address for external communication.

#### 77. Will I able to access amazon.com if I'm using private IP (say, if I'm a part of an organization). Or will I need a public IP as well to connect with it?
**Answer.** If you are using a private IP address, you may still be able to access websites on the internet through NAT (Network Address Translation) performed by your organization's gateway or router. However, some websites may restrict access based on IP addresses or require authentication.

#### 78. If one person is able to access amazon.com website, while the other person is not, what can be the possible valid reasons for the 2nd person, provided the amazon.com website is working fine. Why clearing cookies also helps in reaching to a website?
**Answer.** Possible reasons for one person being able to access a website while another cannot include network connectivity issues, DNS resolution problems, browser cache or cookie issues, firewall restrictions, IP address blacklisting, or server-side access restrictions. Clearing cookies can help resolve access issues caused by cached or corrupted data.

#### 79. My net isn't working, how do i troubleshoot?
**Answer.** To troubleshoot network connectivity issues, you can start by checking physical connections, restarting network devices, verifying network settings, testing connectivity with other devices, checking for IP address conflicts, and reviewing firewall configurations. Additionally, diagnostic tools like ping, traceroute, and netstat can help identify and resolve network problems.
