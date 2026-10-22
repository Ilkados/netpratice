This project has been created as part of the 42 curriculum by <moboulir>.
NetPractice
Description
NetPractice introduces the fundamentals of computer networking through 10 practical exercises. Each level presents a simulated network with communication problems. The goal is to configure its IP addresses, subnet masks, gateways, and routes until all required connections work.

The project develops an understanding of how devices communicate within a subnet and across different networks. It also teaches how to follow a packet's path, identify an incorrect configuration, and check that a reply can return to its source.
Instructions
Running the training interface
Download the training package from the NetPractice project page on the 42 Intranet and extract it. Open a terminal in the extracted directory containing run.sh, then run:
bash run.sh
Open the address displayed by the launcher if the browser does not open automatically. Use the setup instructions included with your package if its launch procedure differs. No project source code needs to be compiled.

Enter your 42 login in the interface to begin training. For each level, read the objectives and adjust the editable network settings. Use Check again to test your configuration and read the logs to understand any remaining errors.
Exporting and submitting
After completing a level, click Get my config to download its configuration before moving to the next level. Repeat this for all 10 levels.

Place 10 exported configuration files, one per level, directly at the root of your Git repository, alongside this README.md. Keep each export clearly associated with its level and follow any filename requirements in your project subject.

Before submission, verify that all levels were exported with your login entered, then commit and push the files to the assigned repository. 

What I Studied The starting point was IPv4 addressing: understanding how an IP address and subnet mask identify a device's network. From there, subnetting introduced CIDR notation, network and broadcast addresses, and usable host ranges.

For example, 192.168.1.130/26 belongs to the network 192.168.1.128/26. 
Its broadcast address is 192.168.1.191, 
leaving 192.168.1.129 through 192.168.1.190 for ordinary hosts.

The next step was understanding communication between networks. A switch forwards frames within a local network, while a router forwards packets between networks. 
A host uses a default gateway when no more specific route matches its destination. 
Routing tables determine the next hop, and successful communication needs both a forward route and a return route.

The OSI model helped place these concepts in context:
    Layer	                                    Role
7 — Application  :   Defines application messages and services, such as HTTP and DNS
6 — Presentation :	 Describes data representation, encoding, compression, and encryption
5 — Session	     :   Describes establishing and coordinating dialogues
4 — Transport	 :   Handles transport between application endpoints using protocols such as TCP and UDP
3 — Network	     :   Handles IP addressing and routing
2 — Data Link	 :   Transfers frames over local links
1 — Physical	 :   Carries signals through a physical medium


To connect networking with programming, I also explored sockets and ports. An application creates a socket and supplies the destination address and port. 
For TCP, it then initiates a connection. 
TCP provides an ordered byte stream with retransmission, while UDP sends datagrams without built-in guarantees of delivery or order.

OSI describes responsibilities rather than mandatory programming steps. 
In typical Internet applications, session management and data representation are handled by application code and libraries rather than separate OSI components.
Resources

The networking concepts studied include TCP/IP addressing, IPv4, subnet masks, CIDR, default gateways, routing tables, routers and switches, OSI layers, sockets, ports, TCP, and UDP.
- 42 NetPractice subject and training package — project instructions, interface usage, and submission requirements, available through the 42 Intranet.
- Network Engineer Roadmap — a guide for organizing further networking study.
- RFC 791 — Internet Protocol — IPv4 and packet delivery.
- RFC 4632 — CIDR — network prefixes and classless addressing.
- RFC 1812 — IPv4 Routers — routing and packet forwarding.
- RFC 9293 — TCP and RFC 768 — UDP — transport protocols.
- Python Socket Documentation — the programming interface for network communication.
AI Use
I used ChatGPT to explain networking concepts through simple examples, discuss subnetting and routing problems, 
and understand connectivity errors, including missing return routes. 
Our discussions also covered sockets, ports, TCP and UDP, OSI layers, 
and the distinction between an application session and a TCP connection.
