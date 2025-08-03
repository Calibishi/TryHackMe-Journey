# TryHackMe-Journey
A record of my hands-on cybersecurity learning through TryHackMe labs, tools, and challenges.

# July 10th - The start of it all. Hacking First Website.
- I hacked my first website today (a fake bank account website).
- Reflection: It was pretty cool. Nothing quite like using the terminal. Now, it has been put to good use.

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

- Spoofing simulation.
  
- Reflection/ Research: Privacy and Protection deep dive - Researched VPN, How private browsers only clear the local device (wow), and more about System Services (Specifically Significant locations), more on how Google tracks information, turning off personalized ads (to reduce attraction to ads and reduce wasted time), "Anonymity Tools" can be used for good reasons like journalists hiding from oppressive regimes, whistleblowers protecting identites, etc.

# 7/19 Ping (Packet InterNet Groper)
- Uses ICMP (Internet Control Message Protocol) packets to see how well a connection is holding up between devices.

# 7/20 Ping(ing) a Mac IP.
- Command: ping 4.5.6.7
- IP Address Ping Speed vs. Router Ping Speed.
- How do they keep Mac Addresses from overlapping when creating devices in a factory?
  -> Managed by the IEEE (Institute of electrical and electronics engineers), global org based in the US.
    -+  companies request a certain amount of Mac addresses for a price.
  -> Owning bulk Mac Address as a potential digital real estate.
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

# OSI Room!


