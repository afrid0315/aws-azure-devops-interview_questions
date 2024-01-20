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

#### 27. 
**Answer.** 

#### 28. 


1.Delivery vs deployment 
2.What is cicd
3.Jenkins build declarative file
4.Alb ,nlb
5.Ansible cloud modules
6.Ansible facts module
7.Terraform stages
8.Terraform commands
9.Git rebase vs git merge
10.Diff b/w ec2 and s3
11.Internet gateway,NAT gateway
12.Vpc
13.She’ll script $ symbol purpose
14.How to input file in shell script
15.Data types in python
16.How to secure keys 
17.Hashicorp vault ,kms 
18.How to integrate sonarkube in declarative pipeline
19.Webhooks 
20.how to create a ec2 instance in ansible play book 
21.What is task in ansible
22.How to add multiple tasks in ansible playbook
23.What is playbook 
24.Which deployment model used in your organisation
25.How to deploy a deployment yaml file
26.How to encrypt and decrypt secret keys
27.How to pass a credentials in pipeline
28.What is pipeline
29.Which bug tracking tool is used
30.Are you used jira tool
31.What are the components required to create ec2 instance
32.How to rollout a update in kubernetes
33.S3 cli commands
34.Sticky sessions
35.Terraform backends 
36.Meta data vs user data 
37.What is helmcharts and it’s use
38.If I lose the state files in terraform how can I recover that
39.How to increase ec2 instance storage without stoping the instance
40.Terraform validate 
41.How to debug the pods 
42.Rollout and rollback
43.Kubectl describe 
44.What is namespace
45.What is listeners
46.Vpc endpoint types
47.Route table
48.Public subnet ,private subnet
49.Security groups
50.Ip tables
51.Internet gateway
52.Nat gateway
53.Cluster ip
54.Micro services 
55.Micro services advantages and disadvantages
56.What is cloud native applications 
And it’s used and advantage
57.Linux file permissions types
58.How to mount a volume in Linux
59.Why it’s using v1/apps in service file in kubernetes
60.Load balancer waiting time
61.AWS code deploy 
62.Nginx config file locations
63.How to attach NAT , internet gateways 
64.Pod.yaml file
65.Service.yaml file 
66.How to debug the Linux is performance issue
67.How to modify Terraform state files
68.Ad hoc command ansible
69.Docker file for httpd
70.Terraform resource file 
71.Ansible syntax check command
72.How to restrict user in s3 bucket - ip restrictions
73.Acl policies
74.Ec2 instance types and difference 
75.EBS vs EFS
76.Redirect and rewrite in cloudfront
77.Diff b/w on demand instance,spot instances,reserved instance 
78.Instance type c4.X-Large and m4.X-Large 
79.Autoscaling groups ,how to add spot,on demand instances in Autoscaling
80.Node is not booted how to debug that node
81.Ansible host ping is success but I am not execute playbooks why?
82.I am trying to connect an ec2 instance but I am facing issues how to debug?
83.Disk usage checking command
84.Diff b/w Postgres and MySQL 
