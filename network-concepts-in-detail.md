## Computer Network concepts in detail


Routers and switches are both integral components of computer networks, but they serve different purposes and operate at different layers of the OSI model. Here are their definitions and key differences:

#### Router:

A router is a networking device that forwards data packets between computer networks. It operates at the network layer (Layer 3) of the OSI model.
Routers use logical addressing (such as IP addresses) to determine the best path for forwarding packets from the source to the destination across multiple networks.
They make decisions based on routing tables, which contain information about network addresses and the best paths to reach them.
Routers are capable of performing functions such as packet forwarding, routing, and network address translation (NAT).
They are essential for connecting multiple networks, such as LANs, WANs, or the internet, and ensuring that data reaches its intended destination efficiently.

#### Switch:

A switch is a networking device that connects devices within a single local area network (LAN). It operates at the data link layer (Layer 2) of the OSI model.
Switches use MAC addresses to forward data packets within a LAN. They maintain a MAC address table (also known as a forwarding table or CAM table) that maps MAC addresses to the physical ports on the switch.
When a switch receives a data packet, it examines the destination MAC address and forwards the packet only to the port associated with that address, rather than broadcasting it to all ports like a hub.
Switches are designed to increase network performance and efficiency by reducing network congestion and improving bandwidth utilization within a LAN.
They are commonly used in Ethernet-based networks to connect devices such as computers, printers, servers, and other networking equipment.

#### Key Differences:

Functionality: Routers forward data between different networks, while switches forward data within a single network.
Layer of Operation: Routers operate at the network layer (Layer 3), whereas switches operate at the data link layer (Layer 2).
Addressing: Routers use logical addressing (e.g., IP addresses), while switches use MAC addresses.
Scope: Routers connect multiple networks and determine the best path for data transmission, while switches connect devices within a single network and facilitate communication between them.
In summary, routers and switches play complementary roles in computer networks, with routers handling inter-network communication and switches managing intra-network communication. Understanding the differences between these devices is essential for designing and maintaining efficient network infrastructures.

**MAC address:**

**A MAC address, or Media Access Control address**, is a unique identifier assigned to a network interface controller (NIC) for communication on a network. It's a hardware address that is assigned by the manufacturer and is stored in the device's firmware.

Here are some key points about MAC addresses:

Uniqueness: Each MAC address is globally unique. This means that no two devices should have the same MAC address. The uniqueness of MAC addresses is ensured by the IEEE (Institute of Electrical and Electronics Engineers), which assigns blocks of MAC addresses to manufacturers.

Structure: A MAC address is typically represented as a 12-digit hexadecimal number (e.g., 00:1A:2B:3C:4D:5E). The first six digits represent the manufacturer's unique identifier (OUI - Organizationally Unique Identifier), while the remaining digits are specific to the individual device.

Locally Administered Addresses vs. Universally Administered Addresses: MAC addresses can be either locally administered or universally administered. Universally administered addresses are assigned by the manufacturer, while locally administered addresses can be manually assigned by the network administrator.

Role in Networking: MAC addresses are used in the data link layer (Layer 2) of the OSI model to uniquely identify devices within a local network. When data is sent over a network, it is encapsulated in a frame that includes the source and destination MAC addresses. Switches and other network devices use these MAC addresses to forward the data to the appropriate destination.

Examples of Usage: MAC addresses are commonly used in Ethernet networks to facilitate communication between devices, such as computers, printers, routers, switches, and other networking equipment. They are also used in wireless networks (Wi-Fi) for similar purposes.

Overall, MAC addresses play a crucial role in network communication by providing a means to uniquely identify devices on a network, enabling efficient and accurate data transmission.

#### Broadcast domain:

A broadcast domain is a logical division of a computer network, in which all devices can directly send broadcast messages to each other. These messages are typically intended for all devices within the same network segment. In simpler terms, a broadcast domain is the area of a network where broadcast traffic is confined.

Here are some key points about broadcast domains:

Scope: A broadcast domain usually corresponds to a single subnet or VLAN (Virtual Local Area Network). All devices within the same broadcast domain can send broadcast messages to each other.

Broadcast Messages: Broadcast messages are special types of network packets that are sent to all devices within a broadcast domain. They are typically used for purposes such as address resolution (ARP - Address Resolution Protocol), service discovery (Bonjour, SSDP), or network management.

Traffic Isolation: Devices in different broadcast domains cannot directly send broadcast messages to each other. Broadcast traffic is contained within the boundaries of the broadcast domain, which helps prevent unnecessary network congestion and improves network performance.

Routing Boundaries: Routers are used to separate broadcast domains. They operate at the network layer (Layer 3) of the OSI model and forward traffic between different broadcast domains based on routing tables. By default, routers do not forward broadcast traffic between different network segments.

Impact on Network Design: Understanding broadcast domains is essential for designing efficient and scalable networks. By carefully planning the allocation of subnets and VLANs, network administrators can control the size of broadcast domains and optimize network performance.

VLANs: Virtual Local Area Networks (VLANs) are often used to segment a physical network into multiple broadcast domains. Each VLAN acts as a separate broadcast domain, allowing network administrators to logically group devices based on their functional requirements or security policies.

In summary, a broadcast domain defines the scope within which broadcast messages can be sent and received by devices on a network. Understanding and properly managing broadcast domains is crucial for maintaining network performance and scalability.

#### What exactly broadcast domain does?
A broadcast domain serves several important functions in a computer network:

Address Resolution: One of the primary functions of broadcast messages is address resolution. For example, in IPv4 networks, the Address Resolution Protocol (ARP) is used to map IP addresses to MAC addresses. When a device needs to communicate with another device on the same network and knows only the IP address, it sends out an ARP request as a broadcast message to all devices within the broadcast domain. The device with the corresponding IP address responds with its MAC address, allowing communication to proceed.

Service Discovery: Broadcast messages are often used for service discovery within a network. For instance, protocols like Bonjour (used in Apple devices) and SSDP (Simple Service Discovery Protocol) allow devices to announce their presence and discover services offered by other devices on the network. These announcements are typically sent as broadcast messages within the broadcast domain, enabling devices to discover and interact with each other seamlessly.

Network Management: Broadcast messages can also be used for network management purposes. For example, network monitoring tools may use broadcast messages to collect information about network devices or to broadcast alerts or status updates to all devices within the network segment. This helps network administrators monitor and manage the health and performance of the network more effectively.

Dynamic Host Configuration: Broadcast messages play a role in dynamic host configuration protocols such as DHCP (Dynamic Host Configuration Protocol). When a client device connects to a network and needs to obtain an IP address, it sends a DHCP discovery request as a broadcast message. DHCP servers within the broadcast domain respond to these requests, offering IP addresses and other configuration parameters to the client device.

In essence, a broadcast domain facilitates communication and interaction between devices within the same network segment by allowing them to send broadcast messages to each other. These messages serve various purposes, including address resolution, service discovery, network management, and dynamic host configuration, contributing to the efficient operation of the network.

#### DNS:

DNS stands for Domain Name System. It is a decentralized naming system for computers, services, or any resource connected to the Internet or a private network. DNS is essentially like a phone book for the internet, translating human-readable domain names (like www.example.com) into IP addresses (like 192.0.2.1) that computers use to identify each other on the network.

Here's how DNS works and why it's important:

Domain Names: Domain names are the familiar, easy-to-remember names for websites and other internet services. They consist of two main parts: the top-level domain (TLD), such as .com, .org, .net, and the second-level domain (SLD), which is the unique name chosen by the website owner (e.g., example.com).

IP Addresses: Every device connected to the internet, including web servers, computers, routers, and smartphones, has a unique numerical address called an IP address. IP addresses are used by computers to communicate with each other over the internet. For example, when you type a domain name into your web browser, your computer uses DNS to look up the corresponding IP address so it can connect to the website's server.

DNS Servers: DNS operates through a distributed network of servers called DNS servers. These servers store databases of domain names and their corresponding IP addresses. When you request a website by its domain name, your computer sends a query to a DNS server, which then looks up the IP address associated with that domain name and returns it to your computer. If the DNS server doesn't have the information cached, it will recursively query other DNS servers until it finds the correct IP address.

Hierarchy: DNS operates in a hierarchical structure, with different levels of servers responsible for different parts of the domain name system. At the top of the hierarchy are the root DNS servers, which store information about the top-level domains (TLDs). Below them are authoritative DNS servers, which are responsible for specific domains or subdomains. Finally, there are caching DNS servers, which temporarily store DNS records to speed up future queries.

Resolution Process: The process of translating a domain name into an IP address is called DNS resolution. It involves multiple steps, including querying DNS servers, caching results, and resolving domain names to their corresponding IP addresses. DNS resolution happens automatically whenever you access a website or other internet service by its domain name.

Overall, DNS is a fundamental component of the internet infrastructure, enabling users to access websites and services using easy-to-remember domain names instead of complex numerical IP addresses. Without DNS, the internet as we know it would not be possible.

#### TCP (Transmission Control Protocol) and UDP (User Datagram Protocol):

TCP (Transmission Control Protocol) and UDP (User Datagram Protocol) are two of the main transport layer protocols used in computer networks. They provide the means for applications to communicate with each other over a network, but they have different characteristics and are suitable for different types of communication.

Here's an overview of TCP and UDP:

**TCP (Transmission Control Protocol):**

Connection-Oriented: TCP is a connection-oriented protocol, which means it establishes a logical connection between the sender and receiver before data exchange. This connection is maintained throughout the entire communication session.
Reliable: TCP ensures reliable delivery of data by using acknowledgment mechanisms, sequence numbers, and retransmission of lost or corrupted packets. It guarantees that data arrives in the same order it was sent and without errors.
Flow Control and Congestion Control: TCP incorporates flow control and congestion control mechanisms to manage the rate of data transmission and prevent network congestion.
Examples of TCP Applications: TCP is used for applications that require reliable, ordered delivery of data, such as web browsing, email, file transfer (FTP), remote terminal access (SSH), and online gaming.

**UDP (User Datagram Protocol):**

Connectionless: UDP is a connectionless protocol, meaning it does not establish a dedicated connection between the sender and receiver before transmitting data. Each packet is treated independently and may take different paths through the network.
Unreliable: Unlike TCP, UDP does not provide reliability or error-checking mechanisms. It does not guarantee delivery, order, or error correction. Packets may arrive out of order, duplicated, or not at all.
Low Overhead: UDP has lower overhead compared to TCP because it lacks the overhead of connection establishment, acknowledgment, and flow control mechanisms. This makes UDP faster and more efficient for certain types of communication.
Examples of UDP Applications: UDP is used for applications where real-time communication and low latency are more important than reliability, such as streaming media (audio and video), voice over IP (VoIP), online multiplayer gaming, and Domain Name System (DNS) queries.
In summary, TCP and UDP are both important transport layer protocols used for communication over computer networks, but they have different characteristics and are suitable for different types of applications. TCP provides reliable, ordered delivery of data with connection-oriented communication, while UDP offers faster, connectionless communication with lower overhead but no reliability guarantees. The choice between TCP and UDP depends on the specific requirements of the application and the trade-offs between reliability, latency, and efficiency.

#### What is MSS/MTU:

MSS (Maximum Segment Size) and MTU (Maximum Transmission Unit) are both terms used in networking, particularly in the context of TCP/IP (Transmission Control Protocol/Internet Protocol) communications. They relate to the maximum size of data packets that can be transmitted over a network.

MTU (Maximum Transmission Unit):

MTU refers to the maximum size of an IP packet that can be transmitted over a specific network link without fragmentation.
It represents the largest amount of data that can be encapsulated in a single frame or packet at the data link layer (Layer 2 of the OSI model).
MTU is typically measured in bytes.
When a device sends data across a network, it breaks the data into packets. The MTU determines the maximum size of these packets. If the data to be transmitted exceeds the MTU of a network segment, the data must be fragmented into smaller packets to fit within the MTU limit.
MSS (Maximum Segment Size):

MSS is a parameter in TCP that specifies the largest amount of data that a device can receive in a single TCP segment.
It represents the maximum size of the payload data in a TCP segment, excluding the TCP header and IP header.
MSS is negotiated during the TCP handshake process when establishing a TCP connection between two devices. It is determined based on the minimum MTU value along the path between the two devices minus the size of the IP and TCP headers.
MSS helps to optimize TCP performance by ensuring that TCP segments fit within the MTU of the underlying network, reducing the need for fragmentation and improving efficiency.
In summary, MTU specifies the maximum size of IP packets that can be transmitted over a network link, while MSS specifies the maximum size of payload data in TCP segments exchanged between devices. Both parameters play important roles in determining the efficient transmission of data over a network, minimizing fragmentation and optimizing performance.

#### OSI model with complete details and protocols on each layer:

The OSI (Open Systems Interconnection) model is a conceptual framework that standardizes the functions of a telecommunication or computing system into seven abstraction layers. These layers help to understand how different protocols and technologies interact to enable communication between devices on a network. Here's an overview of the OSI model:

Physical Layer (Layer 1):

The physical layer is responsible for transmitting raw data bits over a communication channel. It defines the electrical, mechanical, and procedural aspects of the physical connection between devices.
Examples: Ethernet, Wi-Fi, fiber optics, electrical signals.
Data Link Layer (Layer 2):

The data link layer provides reliable data transfer across a physical link and detects and corrects errors that may occur in the physical layer.
It also manages access to the physical medium and controls the flow of data.
Examples: Ethernet (MAC sublayer), Wi-Fi (MAC sublayer), HDLC (High-Level Data Link Control).
Network Layer (Layer 3):

The network layer is responsible for addressing, routing, and forwarding data packets between different networks.
It determines the best path for data packets to reach their destination based on network topology and congestion.
Examples: IP (Internet Protocol), ICMP (Internet Control Message Protocol), ARP (Address Resolution Protocol).
Transport Layer (Layer 4):

The transport layer provides end-to-end communication between devices on different hosts and ensures that data is reliably delivered, ordered, and error-checked.
It also manages flow control and congestion control to optimize the transmission of data.
Examples: TCP (Transmission Control Protocol), UDP (User Datagram Protocol), SCTP (Stream Control Transmission Protocol).
Session Layer (Layer 5):

The session layer establishes, maintains, and terminates communication sessions between applications on different devices.
It handles synchronization, checkpointing, and recovery of data exchange sessions.
Examples: NetBIOS, RPC (Remote Procedure Call).
Presentation Layer (Layer 6):

The presentation layer is responsible for data translation, encryption, and compression to ensure that data exchanged between applications is in a format that the receiving application can understand.
It abstracts the differences in data formats and ensures interoperability between different systems.
Examples: SSL/TLS (Secure Sockets Layer/Transport Layer Security), ASCII, JPEG.
Application Layer (Layer 7):

The application layer provides network services directly to end-users and application processes.
It includes protocols and services for tasks such as file transfer, email, remote login, and web browsing.
Examples: HTTP (Hypertext Transfer Protocol), FTP (File Transfer Protocol), SMTP (Simple Mail Transfer Protocol), DNS (Domain Name System).
The OSI model serves as a reference framework for understanding how communication protocols and technologies interact within a network environment. Each layer performs specific functions, and data passes through these layers from the application layer down to the physical layer during transmission, and vice versa during reception.

#### SSL Handshake:

The SSL (Secure Sockets Layer) handshake is a process that occurs between a client and a server when establishing a secure connection for encrypted communication. The SSL handshake involves several steps to negotiate the parameters of the secure connection and authenticate both parties. Here's an overview of the SSL handshake process:

Client Hello:

The SSL handshake begins with the client sending a "Client Hello" message to the server.
This message includes the client's SSL version, a list of supported cipher suites (encryption algorithms), and a random number called the "Client Random."
The client also includes any other parameters required for the handshake, such as supported compression methods or session ID for session resumption.

Server Hello:

Upon receiving the Client Hello message, the server responds with a "Server Hello" message.
The Server Hello message includes the chosen SSL version, a selected cipher suite from the client's list of supported suites, and a random number called the "Server Random."
If the server supports session resumption and the client provided a session ID, the server may include a session ID in the Server Hello message.

Server Certificate:

After the Server Hello message, the server sends its digital certificate to the client.
The certificate contains the server's public key, along with information about the server's identity (such as its domain name) and the digital signature of the certificate authority (CA) that issued the certificate.
The client verifies the certificate's authenticity by checking the digital signature against its list of trusted root CAs.

Key Exchange:

Once the client has validated the server's certificate, it generates a "Pre-Master Secret" (a random value) and encrypts it with the server's public key from the certificate.
The client sends the encrypted Pre-Master Secret to the server.
Both the client and server use the Pre-Master Secret, along with the Client Random and Server Random values exchanged earlier, to derive the "Master Secret" for the session.

Client Finished:

The client sends a "Client Finished" message, which includes a hash of all the exchanged handshake messages so far, encrypted using the negotiated encryption parameters.
This message verifies to the server that the client has successfully processed the handshake messages and is ready to begin encrypted communication.
Server Finished:

The server sends a "Server Finished" message, which includes a hash of all the exchanged handshake messages (including the Client Finished message) so far, encrypted using the negotiated encryption parameters.
This message verifies to the client that the server has successfully processed the handshake messages and is ready to begin encrypted communication.
Established Secure Connection:

Once both the client and server have exchanged Finished messages and verified each other's authenticity, they have established a secure, encrypted connection.
All subsequent data transmitted between the client and server is encrypted and protected from eavesdropping or tampering.
The SSL handshake process ensures that both the client and server agree on the parameters of the secure connection, authenticate each other's identities, and establish a secure channel for encrypted communication.

##### Flow/Error Control:

Flow control and error control are essential mechanisms used in data communication to ensure reliable and efficient transmission of data between devices. Let's delve into each concept:

Flow Control:

Definition: Flow control regulates the flow of data between sender and receiver to prevent the receiver from being overwhelmed by a faster sender. It ensures that the receiver can process incoming data at a rate it can handle.
Purpose: Flow control prevents buffer overflow at the receiver and avoids data loss or corruption due to congestion.
Techniques:
Buffering: Buffers are used to temporarily store data at the receiver until it can be processed.
Sliding Window Protocol: This protocol allows the sender to transmit multiple frames before receiving acknowledgment from the receiver, optimizing network efficiency.
Rate-based Flow Control: In rate-based flow control, the sender adjusts its transmission rate based on feedback from the receiver, such as acknowledgments or flow control signals.
Examples: TCP (Transmission Control Protocol) utilizes flow control mechanisms such as TCP window size and the sliding window protocol to regulate data flow between sender and receiver.

Error Control:

Definition: Error control ensures that data transmitted between devices is received accurately and without corruption. It detects and corrects errors that may occur during transmission.
Purpose: Error control ensures data integrity and reliability by identifying and correcting errors caused by noise, interference, or transmission issues.
Techniques:
Error Detection: Techniques such as checksums, CRC (Cyclic Redundancy Check), and parity bits are used to detect errors in transmitted data.
Error Correction: Forward Error Correction (FEC) codes, such as Hamming codes or Reed-Solomon codes, are used to correct errors in the received data without the need for retransmission.
Automatic Repeat reQuest (ARQ): ARQ protocols request retransmission of corrupted or lost data segments, ensuring reliable delivery.
Examples: In TCP/IP, error control is primarily handled by TCP through mechanisms such as checksums, sequence numbers, acknowledgments, and selective repeat or Go-Back-N ARQ protocols.
Both flow control and error control are integral components of reliable data communication protocols. They work together to ensure that data is transmitted accurately, efficiently, and with minimal disruption, even in challenging network conditions. These mechanisms are essential for maintaining the integrity and performance of modern communication networks.

#### DNS query process:

The DNS (Domain Name System) query process involves several steps to resolve a domain name to its corresponding IP address. Here's an overview of the DNS query process:

**DNS Resolver Request:**

When a user or application initiates a DNS query by entering a domain name (e.g., www.example.com) into a web browser or other network application, the DNS resolver on the user's device sends a DNS query request to a DNS server.

**Local DNS Cache Check:**

The DNS resolver first checks its local cache to see if it already has the IP address corresponding to the requested domain name. If the IP address is found in the cache and is still valid (not expired), the resolver returns the IP address to the requesting application, and the query process ends.

**Recursive Query to DNS Server:**

If the IP address is not found in the local cache or has expired, the DNS resolver sends a recursive query to a DNS server.
The recursive query is sent to the user's configured DNS server, typically provided by the Internet Service Provider (ISP) or a public DNS service like Google DNS or OpenDNS.

**Root DNS Server Resolution:**

If the user's DNS server does not have the IP address in its cache, it initiates the DNS resolution process by querying the root DNS servers.
The root DNS servers are the top-level servers in the DNS hierarchy and maintain information about the authoritative DNS servers responsible for top-level domains (TLDs) such as .com, .org, .net, etc.

**TLD DNS Server Resolution:**

The root DNS servers respond to the DNS resolver's query with the IP addresses of the authoritative DNS servers responsible for the requested TLD.
The resolver then queries one of the authoritative DNS servers for the TLD (e.g., the .com DNS server) to obtain information about the next-level domain.

**Authoritative DNS Server Resolution:**

The authoritative DNS server for the requested domain name responds to the resolver's query with the IP address(es) associated with the domain name.
If multiple IP addresses are returned (e.g., for load balancing or redundancy), the resolver typically selects one of the IP addresses for further use.

**Caching of DNS Response:**

The DNS resolver caches the IP address obtained from the authoritative DNS server in its local cache for future use, along with the corresponding time-to-live (TTL) value provided by the authoritative DNS server.
The TTL value specifies how long the resolver should consider the cached IP address valid before it expires and needs to be refreshed with a new query.

**Return IP Address to Application:**

Finally, the DNS resolver returns the IP address obtained from the authoritative DNS server to the requesting application or user's device.
The application can then use the IP address to establish a connection with the desired web server or other network resource associated with the domain name.
Overall, the DNS query process involves a series of hierarchical queries from the local resolver to root DNS servers, TLD DNS servers, and authoritative DNS servers to obtain the IP address corresponding to a given domain name. Caching of DNS responses at various stages helps improve efficiency and reduce the load on DNS infrastructure by minimizing redundant queries for frequently accessed domain names.
