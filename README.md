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

- HTTP Methods: (8/21)
  -> GET - get's information from the web server.
  -> POST - for submitting data and potentially creating new records from the web server.
  -> PUT - update any information in the web server.
  -> DELETE - Delete (ya know.. from the web server).

- HTTP Status Codes (8/27):
  -> Ranges: 200 (Success), 300 (Redirection), 400 (Client Error), 500 (Server Error)
    -> Notable: 201 (New successful creation), 404 (Page not found), & 401 (Not authorized).

#   (12/11/25)

Different Types of Request Headers (from Client to server): 
  1) Host- specific websidt if web server hosts multiple websites
  2) User-Agent: your browser software and version number.
  3) Content Length
  4) Accept-Encoding: compression methods supported
  5) Cookie- data sent to the server to remember your info.

Common Response Headers:
  1) Set-Cookie
  2) Cache-Control: how long to store cach before reuqesting again.
  3) Content-Type: Type of data being returned (HTML, CSS, PDF, Video, etc)
  4) Content-Encoding: as above

Note: HTTP is stateless (does not keep track of previous requests).

Cookies are mainly used for web authentication (though they have many purposes).

Q: Want to know what cookies are being sen to the server? Use the developer tools, click "Network" tab and look at each tab labeled "Cookies."

# Simulation: w/ PUT, GET, POST, and DELETE requests with HTTPS in the URL Bar with parameters.


# How Websites Work:

When visting a website, your browser makes a requests to a web server.
  This web server is a dedicated computer somewhere else that handles the requests.

Classic Setup of Websites:
  1) Front-end (Client-side): the way your browser renders a website. (render is just display/convert code to visuals/things)
  2) Back-end (Server-side): a serve that processes requests and returns a response.

HTML Structure overview.
  - View any HTML by right clicking -> View/Show Page Source.

JavaScript overview.
  - <script></script> tags
  - remotely with the src attribute.
  - "onclick" and "onhover"

Sensative Data Exposure: 
  * If a developer does not remove login credentials, then this data may be viewed in the page source HTML elements simply.
  * Checking this should be ONE OF THE FIRST THINGS you do when assessing a web app for security.

# Simulation: Using 'View Page Source' to find test login credentials in the source code of a page.

HTML Injection:
  - a vulnerability that happens when unfiltered user input is displayed on the page.
  - Fix: Sanitize (filter) anything the user inputs.
    -  Never trust the user input.
   
  # Simulation: Inject a malicous link into a website using HTML on a input that doesn't sanitize user input.

Load Balancers- are used to
  1) ensure high traffic websites can handle the load
  2) provide a failover in case a server becomes unresponsive.
  - uses algorithms like round-robin (sends to each server in turn) or weighted (checks how many requests a server is currently dealing with.
  3) perform health checks, make sure things are ruinning smoothly.

CDNs - Content Delivery Networks
  - host static files from your website and host them across thousands of servers ArOuNd tHe WoRlD.
      - when a user requests one of the hosted files, the CDN works out the nearest server by physical location and sends the request there inside of the using a server on the other side of the world.
   
Databases - way of storing information for their users.
  - Web servers communicate with them.

WAF - Web Application Firewall
  1) used to protect webserver from attacks or hacking.
  2) analyses web requests for common attack techniques.
  3) uses rate limiting, checking if an excessive amount of web requests are being sent, requests from IP per sec.
    - if suspicious, the requests are dropped and never sent.

Web Server - a software that listens for incoming connections and then uses HTTP protocols to send web content back to the user.
  - web server software like Apache, Nginx, NodeJS, IIS.
  - delivers files from the root directiory, /var/www/html for Linux and C:\inetpub\wwwroot for Windows.

Virtual Hosts
  - text- based configuration files
  - web servers can host multiple websites (no limit?)

Static and Dynamic Content - either never changes or can change with different requests. 
  - The changes are processed in the backend.
    - The result is seen in the front end.
   
Scripting and Backend Languages - The sky is the limit.
  - can interact with databases, call external serives, processs data from user, and more.

* Difference between Scripting and OOP languages? Scripting is how code runs (fast development and automation), backend is where the code runs powering service logic and data handling, and OOP is how you organize complex programs that can be easily reused.
    -Languages like Python and Java have multiple masks.
    - Python is scripting plus backend plus object, oriented programming, for example example. 


# Linux Fundamentals

Created a 1991 by Linus Torvalds, a Finnish CS student. 
Based on UNIX operating system.
Open source, variants UBUNTU and DEBIAN.
  - Open source just means free to the public, can be modified distributed used, and viewed without problems.











