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

#### 22. What is the port of Sonarkube, SQL, DNS?
**Answer.** Sonarkube starts with the port 9000, SQL starts with the port 3306, DNS port number is 53.

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











Docker
What version of docker you have used? Specific reason to use that particular version?
Can we have multiple CMD in Dockerfile?
Have you worked on docker swarm and docker compose?
difference between docker attach and docker exec?

Kubernetes
Can we have multiple conatiners in a pod? Can we have similar conatiners in a pod? Lets say i have 4 conatiners, one of them has failed how would you check which container has failed?
What is liveness and readiness probe? Why we need them?
Have you worked on kubernetes monitoring? Which tools you have used?
Can we deploy a pod on particular node?


Connection draining in load balancer
Routing polices in route53
What encryption method u used for s3 bucket
 Auto scaling polices
Work load in kubernates
Terraform state file and terraform how to create particular resource
 Disadvantage of ami
What is kublet
Container runtime
S3 object lock and how to give permission to particular user to bucket
 Replication

 How can u create read replica in rds
 How you scale read replica
 What is weightied police in route 53
 How to create slaves in jenkins
High level about DR
 Who to create HA in jenkins
 How to start and stop the pod
 Cost optimisation
 Kuberntes cost optimisation

 Jenkins shard library

How to increase node in eks

Sticky session

Connection draining in load balancer

Routing polices in route53

What encryption method u used for s3 bucket

Auto scaling polices

Work load in kubernates

Terraform state file and terraform how to create particular resource

Disadvantage of ami

What is kublet

Container runtime

S3 object lock and how to give permission to particular user to bucket

Replication

How can u create read replica in rds

How you scale read replica

What is weightied police in route 53

How to create slaves in jenkins

High level about DR

Who to create HA in jenkins

How to start and stop the pod

Cost optimisation

Kuberntes cost optimisation

Basic Questions about Kubernetes:-
1. What is Kubernetes networking, and how does it work?
2. What is a service in Kubernetes, and how is it related to networking?
3. What is a cluster IP, and how is it used in Kubernetes networking?
4. How does a pod communicate with other pods in a Kubernetes cluster?
5. What is a pod IP, and how is it used in Kubernetes networking?
6. What is a node port, and how is it used in Kubernetes networking?
7. How does Kubernetes handle load balancing for services?
8. What is an ingress controller, and how is it used in Kubernetes networking?
9. What is a network policy, and how is it used in Kubernetes networking?
10. What is the difference between a Kubernetes Service and a Kubernetes Ingress?
11. What is a Kubernetes ExternalName service, and how is it used in networking?
12. What is the difference between a Layer 4 load balancer and a Layer 7 load balancer, and which one is better for Kubernetes?
13. How does Kubernetes integrate with cloud-based load balancers, such as AWS ELB or Google Cloud Load Balancing?
14. What is the difference between a Kubernetes ClusterIP service and a Kubernetes NodePort service?
15. What is a Kubernetes Headless service, and how is it used in networking?

16. Interview Questions of Docker & Dockerfile:-

1. How will you run multiple Docker containers in one single host? 
Answer: Docker Compose is the best way to run multiple containers as a single service by defining them in a docker-compose.yml file.

2. If you delete a running container, what happens to the data stored in that container? 
Answer: When a running container is deleted, all data in its file system also goes away. However, we can use Docker Data Volumes to persist data even if the container is deleted.

3. How do you manage sensitive security data like passwords in Docker? 
Answer: Docker Secrets and Docker Environment Variables can be used to manage sensitive data.

4. What is the difference between Docker Image and a Docker Container? 
Answer: Docker Image is a template that contains the application, libraries, and dependencies required to run an application, whereas a Docker Container is the running instance of a Docker Image.

5. How do you handle persistent storage in Docker? 
Answer: Docker Volumes and Docker Bind Mounts are used to handle persistent storage in Docker.

6. What is the process to create a Docker Container from a Dockerfile? 
Answer: Docker Build command is used to create Docker images from a Dockerfile and then Docker Run command is used to create Containers from Docker images.

7. How will you scale Docker containers based on traffic to your application? 
Answer: Docker Swarm or Kubernetes can be used to auto-scale Docker Containers based on traffic load.

8. When RUN and CMD instructions will be executed?
Answer: RUN instruction will be executed while building the Docker Image. CMD instruction will be executed while starting the Container.

9. What’s the different between COPY and ADD instructions?
Answer: Using COPY instruction,We can copy local files and folders from docker build context to Docker Image. These files and folders will be copied while creating a Docker Image.
ADD instruction works similar to COPY instruction but the only different is that we can download files from remote locations(Git GitHub, S3, URL) that’s from Internet while creating a Docker Image.

10. What’s the different between CMD and ENTRYPOINT instructions?
Answer: CMD instruction will be used to start the process or application inside the Container.
ENTRYPOINT instruction also works similar to CMD instruction. ENTRYPOINT instruction will also be executed while creating a container. CMD instruction can be overridden while creating a Container where as ENTRYPOINT instruction cannot be overridden while creating a Container.

11. When we have both CMD and ENTRYPOINT instructions in a Dockerfile?
Answer: CMD instruction will not be executed and CMD instruction will be passed as an argument for ENTRYPOINT.
