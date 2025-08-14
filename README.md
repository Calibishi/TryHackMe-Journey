# TryHackMe-Journey
A record of my hands-on cybersecurity learning through TryHackMe labs, tools, and challenges.

# July 10th - Hacking First Website.
- I hacked my first website today (a fake bank account website).
- Reflection: Nothing quite like using the terminal. Now, it has been put to good use.

- Tools used: GoBuster, Terminal/Command Line.

# Detected Malicious IP Address & Blocked It.

# 7/17 - Spoofing a MAC Address to Access Internet. IP and Mac Addresses.

Networks:
- 1989, Tim Berners-Lee, World Wide Web, WWW.
- Devices have a name (which can be changed) and a fingerprint (typically can't be changed).
  -> IP Address, Internet Protocol, 4 Octects.
  -> MAC Address, Media Access Control, 12 character hexadecimal.
- Public and Private networks.
- IPv6 and IPv4.

- Spoofing simulation. What is Spoofing? - Disguising a program to identify as something else in order to access other files/data.
  
- Reflection/ Research: Privacy and Protection deep dive - Researched VPN, How private browsers only clear the local device (wow), and more about System Services (Specifically Significant locations), more on how Google tracks information, turning off personalized ads (to reduce attraction to ads and reduce wasted time), "Anonymity Tools" can be used for good reasons like journalists hiding from oppressive regimes, whistleblowers protecting identites, etc.

# 7/19 Ping (Packet InterNet Groper)
- Uses ICMP (Internet Control Message Protocol) packets to see how well a connection is holding up between devices.

# 7/20 Ping(ing) a Mac IP.
- Command: ping 4.5.6.7
- IP Address Ping Speed vs. Router Ping Speed.
- How do they keep Mac Addresses from overlapping when creating devices in a factory?
  -> Managed by the IEEE (Institute of electrical and electronics engineers), global org based in the US.
    -+  companies request a certain amount of Mac addresses for a price.
  -> Owning bulk Mac Addresses as a potential digital real estate.
  -> 1 OUI (Organizationally Unique Identifier) ~ $2800 USD rn, include 16,777,216 unique Mac Addresses.

# Introduction to LAN Room! (7/25/25)

- Local Area Network. Topology (the lay of the network land or design).
-> Star Topology - all devices connect to a centralized networking device. Most common. More expensive (more cabling/equipment/maintenance). Reliable and Scaleable, but not cheap.
  
-> Bus Topology - think databus, or like the leaves off the branches of a tree. There's one main line (backbone) that run laterally and each device branches off of it. Difficult fixes since different data has to travel down the same main line. Cost-effective tho. If main line breaks, no bueno for anyone.

-> Ring Topology - like it sounds. Wierd because devices only send received data if they themselves don't have something to send. There is good sense of order in this. Less cabling, so less money to start, but one chain. If it breaks, the entire network breaks.

Switches - they're like power strips for internet connections. Smarter than hubs and repeaters. They're like mailboxes in the neighborhood. but the routers are like the main front gate, connecting to the internet.

Routers - connects networks and passes data between them. give devices access to the internet. 

- Rabbit hole dive with home internet, modems, routers, switches and routers, and different pathways.

# A Preview of Subnetting (7/26)

Qs: What is subnetting?
    What is ARP?
    What is DHCP?

- Splitting up a big network into smaller ones.
- Splitting up the number of hosts, subnet masks (32 bit like IP addresses), subnetting for places with many devices.
    -> Ex: Coffee shop with Guest_Wifi & Staff_Wifi.
- Network Address - identity of the start of a network
- Host Address - address used to identify devices on a network.
- Default Gateway (Address) - special addy to a device on the same network with the ability to send data to other networks.

# ARP (Address Resolution Protocol) (8/2)

- tech that lets devices (IP Address) find the MAC Address of other devices.
- cache: a ledger to store information on. In ARP context, it's a ledger of IP to MAC info for quick lookups.
- ARP Request and Reply to identify devices on a network.

# DHCP (Dynamic Host Configuration Protocol)

- IP Address are set/named manually or automatically by DHCP.
- DCHP Discover, DHCP Offer, DCHP Request, DCHP ACK.


[Intro to Lan Room Complete]

# OSI Room! (8/6) 

[OSI Room Start]

Qs: What is the name of the piece of hardware that all networked devices come with?
    What does OSPF and RIP mean in terms of the Network layer?
    What is the difference between TCP and UDP? Which is faster?
    What does DNS stand for?

- Open Systems Interconnects Model, framework for how networked devices send, recieve, and interpret data for each other.
- There is 7 layers to the OSI model,
- Encapsulation.
    1. Physical- (ethernet cables, etc.)
    2. Data Link- (IP, MAC [Media Access Control], and NIC [Network Interface Card, Answer])
    3. Network- (Open Shortest Path First, Routing Information Protocol, Routers, sending packets [small pieces of data]).
    4. Transport- transmitting packets across a network via Transmission Control Protocol vs User Datagram Protocol.
       -> TCP is reliable, is slower, must have an established connection. UDP is fast, doesnt' care about full recieval, and does not need an established connection
       -> For file downloads, sending emails, and file transfers we would use TCP.
    6. Session- established when all the packets are translated and formateed correctly to be sent over. All sessions are unique, data cannot travel over multiple sessions at one time.
    7. Presentation - acts as a translator for different devices.
    8. Application - layer that provides the GUI and other protocols like DNS (Domain Name System).

[OSI Room Complete]


# Packets and Frames Room (8/13)

[P & F Room Start]

Qs: What is piece of data that does have IP addressing? What about if it does not contain IP addressing?
    What is the process of the 3-Way Handshake?
    What ensures the integrity of the data in a TCP Packet.

- Packets, a sliver of data containing header and info like Internet Protocol Addressing and payload (actual data), Layer 3 (Network).
- Frame, the envelope that the packet gets sent in. Refers to encapsulating information. Layer 2 (Data Link).
- The 3-Way Handshake, SYNchronize -> SYNchronize/ACKnowledge -> ACKnowledge.
- CheckSum, a header that checks the integrity of the data, a calculation done on both devices that must be equal or else something went wrong.

- UDP is a stateless protocol that does not require a constant connection. Many headers are the same as TCP.
  -> Good for applications that can afford some data being lost (voice chat or video streaming).

- Ports are places where data can be exchanged. They are specific to whatever information can be passed through that port. Port 80 is where all web browsers send data over.
- Other notable protocols, FTP [File Transfer Protocol], HTTP, HTTPS, SMB [Server Message Block], SSH [Secure Shell], RDP [Remote Desktop Protocol].

Tools: "nc" , Netcat to connect to specificed IP and port, in the terminal.

[Room Complete]


# Extending Your Network Room (cont.)

[E_Y_N Room Start]

Qs: What device configures Port Forwarding?
    What are Firewalls? And how are they different to Port Forwarding?
    What are VPNs and what is the strongest type?
    How are Routers different from Switches?
    Explain the difference between a Layer 2 switch and Layer 3 switch.

- Port Forwarding, allows devices on different networks to connect to applications and services (like web servers), connecting to the Internet, configured on router.
- Without it, only local devices on the same network can use the applications and services (intranet).
  -> We see this a lot with companies who have specific software that is shared only between devices on the same network of the company.
- Port forwarding is not the same as firewall tech which controls the traffic across the port forwarding path.

- Firewalls.
- Will permit or deny entry traffic of info, performs Packet Inspection: "Who are you? Where are you going? Where are you from? What protocols do you use?"
- Operate at Network and Transport layers of OSI (3 & 4)
- Act as Border Patrol between ports and connections.
- Main types are Stateful and Stateless, looking at behaviour of the entire connection (consumes many resources) vs. individual packets (not as useful).

Practical: Configured a firewall to stop an attack of malicious packets from reaching the webserver 203.0.110.1

Virtual Private Networks (VPNs)
- securely established connections between devices on different networks called tunnels, forming their own private network.
  -> Some VPN tech today: PPP [Point to Point {/Tunneling} Protocol], IPSec [Internet Protocol Security] - strong encryption but hardest to establish.

- Routers, connect different networks and pass data between them via "routing."
  -> Very different from swtiches.

- VLAN, Virtual Local Access Network.

- Swtiches, allow devices to forward frames to the connected devices (like routers) using their MAC address [Layer 2].
  -> Layer 3 switches can forward frames and route packets to other devices via IP.


# DNS in Detail (8/14)

[DNS Room Start]

Qs: What is DNS and what does it represent?

- Domain Name System takes place of the complicated IP address number each device gets when connecting to the internet used to reach a webiste or server on the internet.
  -> usually provided by router (internal IP address), then the ISP gives a public IP address to communicate on the over internet (over HHTPS for ex).

- Domain Heiarchy, TLD [Top Level Domain], Second Level Domain, Subdomain
  -> less than 253 characters, no underscores.
  -> Two types: gTLD [Generic Top Level Domains], ccTLD [Country Code TLD].
    -+ Ex: .com [commercial uses], .edu [educational], .org / .us, .ca, .co.uk



  
