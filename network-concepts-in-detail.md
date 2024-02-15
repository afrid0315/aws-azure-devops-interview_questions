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
