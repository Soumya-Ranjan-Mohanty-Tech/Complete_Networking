# Complete_Networking
Notes
**Network** is the collection of devices that are connected together. When devices can talk to each other then it is a network.
**IP address** is a address of a device on a network IPv4 or IPv6 (WE ARE RUNNING OUT OF IPv4)
**1)** **Devices**(Anything with a chip and a connection)-Laptop has IP address like phone, server. Next comes Cables or WiFi Signals. Then Data travelling the network. 
Device. Switch(Connects device in local network). Router (Connects network and decides the route). Internet (The global highway-WAN). Server (The destination has a IP address too).
**Attacks**= **Data Breaches**( DATA STOLEN THROUGH OPEN NETWORK **PORTS*). **Ransomware** (SPREADS ACROSS **NETWORK TO ENCRYPT FILES*). **Phihsing** (EXPLOITS **EMIAL AND WEB PROTOCOL*). **Man in the Middle** (INTERCEPTS **UNENCRYPTED TRAFFIC*). DDoS Attacks (FLOODS **NETWORK BANDWIDTH* WITH GARBAGE). **Port Scanning** (Maps your **network's open doors*).
**2)** **Ports** are the logical endpoint. Port 80- Door for web traffic (HTTP). Port 443 - Secure web door (HTTPS). Port 25 is email (SMTP). Port 22 - SSH(Secure Shell)(Remote Access-Remote command line access). Port 53 - DNS - Domain Name System (Maps domain name to IP Address- Converts name to readable IP numbers for the computer)
**Protocol** - It is a set of rules thats sets the communication. HTTP (Rules for loading web pages- request+response). DNS (Rules for converting domain names to IP Address). TCP (Transfer Control Protocal - Rules for reliable, ordered data delivery).
**Types of Networks**
**PAN** (Personal Area Network- Range<10 meters- Bluetooth to earbuds). **LAN** (Local Area Network- Range is Building/Campus - Home WiFi(WLAN-Home WiFi uses 802.11 standards)/Office network) Security- Once inside LAN, attackers can see all other devices. Defence- Network Segmentation-  deivide LAN into isolated zones. **MAN** (Metropolitan Area Network- Range is City wide- University campus network). **WAN** (Wide Area Network- Range:Country/global- The internet Itself) - Data passes through ISPs, routers, data centres, undersea cables. [An ISP (Internet Service Provider) is a company or organization that provides individuals, households, and businesses with access to the internet and related services.Acting as the bridge between your local network (LAN) and the vast global network (WAN/Internet), they are the "gateway" that allows your devices to send and receive data.What Do ISPs Do?Provide Internet Access: They offer connectivity through various technologies, including fiber-optic cables, cable modems, DSL, and satellite.Data Transport: They own or lease the infrastructure—routers, data centers, and cables—needed to carry our internet traffic across the globe.Provide IP Addresses: When you connect, the ISP assigns your device a unique IP address to identify it on the network.Additional Services: Many ISPs also provide email services, domain registration, and web hosting.] Security: WAN traffic passes through many unknown hands. Defence: ENCRYPTION is essential for data travelling over a WAN. **VPN** (Virtual Private Network- Encrypted tunnel throgh a public network)
**Router**: Connects different network and creates traffic between them- Reads IP Address on each packet to decide where to send it. Everyhome has one-its OUR gateway to the internet. Work at Layer 3 of the OSI Model of Network Layer. Security: Compromised router means attackers controls all traffic. Defence: Strong Password.
**Switch**: Connects different devices within the same network. Smarter than "hub"- sends each message only to its target device. [Tracks MAC address to know which device is on which port]. Works on Layer 2 of the OSI model of Data Link Layer.  A HUB Broadcasts to everyone - a SWITCH is targetted and efficient. Security: MAC FLOODING forces a switch to act like a dumb hub. Attackers than see ALL TRAFFIC meant for everyone on that segment.
**Firewal**: Monitors and [controls network traffic] based on the rules.Can filter traffic by: IP address, port, protocol, content pattern(cache). Types: Stateless (packet filter), Stateful, Application-Layer (WAF). Security: Every enterprise has firewalls- they are the first line of defence. But attackers can bypass firewall_ defence in depth is essential.**1**  [Stateless Firewall] (Packet Filtering) Stateless firewalls, often called packet filtering firewalls, are the most basic, traditional type of firewall.How They Work: They [examine packets in isolation, evaluating them individually based on static information in the header], such as [source/destination IP address, port numbers, and protocol types].Key Characteristics: They do not keep track of active network connections or the "state" of a conversation between internal and external computers.Pros/Cons: They are faster, highly efficient, and require less memory but are less secure because they cannot identify complex attacks that span multiple packets.**2** [Stateful Firewall] (Stateful Inspection) Stateful firewalls provide more sophisticated security by [understanding the context of the network traffic].How They Work: [They monitor the state of active network connections and store this information in a "state table"]. When a packet arrives, the firewall checks its state table to determine if it is part of an **established, legitimate session**.Key Characteristics: They can recognize if an incoming packet is a legitimate response to an internal request, blocking unsolicited traffic.Pros/Cons: More secure and intelligent than stateless firewalls, making them the standard for enterprise perimeters, though they are more resource-intensive. **3** [Application-Layer Firewall] (WAF)These firewalls operate at the highest level of the OSI model (Layer 7), [focusing on specific application traffic].How They Work: [They inspect the actual payload of the data packet, not just the header information].**Web Application Firewall(WAF)** A specific type of application-layer firewall designed to protect web applications by filtering HTTP/HTTPS traffic. They prevent attacks like [SQL injection, cross-site scripting (XSS), and file inclusion], which target application vulnerabilities rather than network ports.Key Characteristics: They are "[application-aware]," understanding the specific web applications they protect.**Summary of Differences Stateless: Filters based on header, header info only (isolated packets). Stateful: Filters based on packet header + connection state (context-aware).Application-Layer (WAF): Filters based on data content (payload) + application logic(URLs, login forms, search boxes, cookies, user input, sessions, HTTP requests/responses).** While firewalls are essential as the first line of defense, modern threats require defense in depth—combining firewalls with other measures like **endpoint security, IDS/IPS, and user training** to prevent attackers from bypassing the perimeter. [1. Application Logic Security] Application logic security focuses on protecting the software itself from vulnerabilities that reside in its code or design rather than the network traffic.What it does: Ensures the application functions as intended, even under attack. It prevents attackers from manipulating the "business logic" of a website or app (e.g., changing prices in a shopping cart, bypassing login steps, or accessing another user's data).Why it's needed: Firewalls often allow HTTP/HTTPS traffic (port 80/443), which hackers use to send malicious requests to the application.Examples: Using Web Application Firewalls (WAF), secure coding practices (OWASP Top 10), and vulnerability testing.[2. Endpoint Security] Endpoint security, or endpoint protection, protects individual devices—such as laptops, workstations, servers, and IoT devices—that connect to a network.What it does: Secures the entry points (devices) from malware, ransomware, and unauthorized access. Modern endpoint protection moves beyond simple antivirus to include **Endpoint Detection and Response (EDR)**, which monitors for suspicious behavior.Why it's needed: As remote work increases, devices are often outside the corporate firewall's direct protection, making them primary targets. Examples: Antivirus, EDR, AI-powered analytics, and disk encryption.
**What is an IDS (Intrusion Detection System)?** An IDS is a passive monitoring system that inspects network traffic for signs of malicious activity, policy violations, or suspicious behavior.Function: It acts like a security camera; it records and detects but does not take direct action.Response: When it detects a potential threat (e.g., malware signature or anomalous traffic), it sends an alert to network administrators.Use Case: Ideal for monitoring and investigating network behavior without risking legitimate traffic disruption. Integration: Modern Next-Generation Firewalls (NGFW) often incorporate IDS/IPS capabilities**What is an IPS (Intrusion Prevention System)?** An IPS is an active, inline security system that not only detects threats but also takes immediate action to prevent them from reaching their destination.Function: It acts like a security guard; it sits in the direct flow of traffic (inline) and inspects every packet in real-time.Response: If a malicious packet is identified, the IPS drops the packet, resets the connection, or blocks the attacker's IP address automatically.Use Case: Essential for proactive protection against known threats and exploits.
**WAP**:**Wireless Access Point** is what creates WiFi network. It broadcasts a wireless signal that devices can connect to. Home router usually has a built in wireless access point. In larger buildings they have dedicated access points mounted in the celling to provide Wifi Coverage. Security: Wireless networks are inherently more vulnerable than wired ones. Data is being broadcast through the air. Anyone within the range can attempt to capture. Thats why WiFi encryption Like WPA2 or WPA3 matters so much.**Network interface card**- Every device that connects to the network has NIC, a network interface card. Its the hardware componenet in each device that handles network communication. It could be a physical Ethernet port (It is used to connect a device to a router or a modem via Ethernet cable) or a WiFi radio built into laptop. Every NIC has a UNIQUE Identifier called MAC Address.
**NIC** (Layer 1 -Network interface card- Hardware inside very device)- **WAP-Wireless Access Point** (Layer1-2 -Creates WiFi signals for wireless device connection)- **Firewall** (Layer 3-7 Inspects and controls traffic based on security rules)- **Switch** (Layer 2 -Connects device within a single network-LAN )- **Router** (layer 3 -Connects Networks and routes packets between them).
**Packets** Data travels as small packets through different routes than reassemble at the destination. Each packet contains piece of DATA, Source IP, Destination of IP, Information about how to reassemble at the destination, error checking information. Security: Packets SNIFFERS capture these- if unencrypted, everything is readable. 

**Networking Headers & Encapsulation**

**1)** **Etnernet Frame Header-Data Link**- Outer Envelop (**Source and destination MAC Adress, Ether type** - **Layer 2**)- It often ends with frame check sequnce(FCS) trailer to check for any physical transmission errors, A 4 byte cyclic redundancy check(CRC) at the very end of the frame - the reciever uses it to detect if bits were corrupted during physical transit- Max size 1500 byte. **Focuses on local delivery between physical hardware (hop to hop)**. Ethertype: A 2 byte field inside the header. Identifies the inner protocol(usually ARP, IPv4 OR IPv6) in other words it indicates which network layer protocol is encapsulated inside the payload, **Preamble**: A 7 byte pattern of alltering 1s and 0s followed by a 1 byte Start Frame Delimiter. Syncs physical timing between network interfaces(Physical and virtual hardware componenets like NIC or WiFi card that connects a computer elctrical, optical, or radio signals into digital frames). Ethernet MTU: Standard Ethernet maximum payload: 1500 bytes. 
**2)** **IP HEADER-Network**-Inner envelop(SourceIP+Destination IP, TTL, Protocol - LAYER 3) **Focuses on Global routing across different networks(end to end device delivery).** Its use Time To Live(TTL- A 8 bit field in IPv4 headers that sets the maximum lifespan of a packet to prevent it from looping infinitely - Hop counter is the mechanism behind TTL. Every router that forwards the packet decrements the TTL value by 1. If the number 0, the the router drops the packet and sends an ICMP error back) field to prevent packets from looping forever. Encapsulation: It treats the transport layer segment (TCP/UDP) as its own Payload. Protocol: Identifies the inner Layer 4 protocol (TCP/UDP). Protocol Field: Identifies the encapsulated Layer 4 protocol: TCP, UDP, ICMP [(Internet Control Message Protocol) Routers and devices use ICMP to communicate problems such as: Destination unreachable, TTL expired, Network congestion, Connectivity status. ICMP does not carry application data like HTTP or email.b Delivery status/error notifications] 
**3)** **TCP HEADER-Transport**- Internal delivery note  (Source and destination Port Numbers, SEQUENCE NUMBERS, FLAGS (ACK/SYN), Checksum- Layer 4). **Focuses on managing connections and primarily directing data to the correct software application using port number(process to process delivery).** Is Complex(20 Bytes)-It provides reliable delivery through sequence numbers and acknowledgement. Sequence number: A 32 Bit TCP field mapping the exact order/sequence of transmitted data bytes. It allows the reciever to reassemble fragmented or out of order packets correctly. Acknowledgement number: A 32 Bit  TCP field that indicates the next expected data byte sequence number. It confirms to the sender that all previous bytes were recieved successfully. Connection Flags: A 1 bit indicators in the TCP Header used to mange connection states. FLAGS(ACK/SYN): Specific connection flags. SYN(Synchronise) initiates a 3 way handshake to establish a connection. ACK(Acknowledgement) confirms recipt of the valid data or connection steps. 
**3.5)** **UDP HEADER-Transport** (Source and destination Port Numbers, Lenghth, Checksum- Layer 4) Focuses on directing data to the correct application using port number(process to process delivery). Simple(8Bytes) Offers best effort delivery with minimal overhead, ideal for speed-sensitive tasks like streaming. UDP Specifics: Simple checksum and basic length field. Simple checksum: Basic error validation-it lacks tracking flags of TCP. Length field: Total bytes of header plus the Data. Streaming, Gaming, VoIP, DNS. 
**4)** **DATA PAYLOAD-Application**-Actual content (My actual content(HTTP Request, email text)- Layer 7) It focuses on the actual information being trasferred, such as HTTP files, a DNS query, or a VoIP audio clip. Size: Varies based on the maximum Transmission Unit(MTU- The largest frame or packet size that a network can transmit without fragmenting it into smaller pieces). Example: HTTP request, Email text, DNS query, VoIP audio. **Calculation**: For a 1500 Ethernet MTU, after substracting 20 bytes for the IP header and 20 Bytes for the TCP Header, The maximum payload size is typically 1460 bytes.

**Client Server Model VS Pier to Pier Models(P2P)**
**Client Server Model**: In the client server models there are two distict roles. Clients are devices who request a things. Example: Web browser_When i type a URL it sends a request. Servers are devices that responds to those requests. A web server recieves my request and sends back the page. My phone is a client_Youtube, NETFLIX, Google they are servers. Servers are centralised. It has control, It has the data. Security: Servers are juicy (High value) targets for attackers. They hold the data of millions of clients. Attacking the server gets the attacker access to everyone's information at once.
**Pier to Pier Models(P2P)**: There is no central server(No Central Authority-Decentralised), every device is BOTH client AND server. Example: Bit Torrent file sharing. Security: It Is harder to monitor and control. Malware sometimes uses P2P style connection to avoid detection - to spread from device to device without a central C2 Server()Central command server that could be shut down. 
**BANDWIDTH AND LATENCY**
**BANDWIDTH**: Bandwidth is the max amount of data that can be transferred through a network per unit of time. Maximum data transfered in a second. Measured in Mbps or Gbps-gigabits. Bandwidth is the number of lanes in the high way. Like the number of lanes. More lanes= More data transfered simultaneously. 100Mbps=100 megabits every second. Security: DDoS attacks SATURATE bandwidth. Legitimate users can't get through. Defence: Monitoring bandwidth and latenct anomalies is a key part of intrusion detection. 
**LATENCY**: Latency is the time it takes the data to travel from source to destination. Time delay for data to reach the destination. Measured in milliseconds (ms)- Lower is better. Like the speed of the car drive not lane count. Affected by distance, routing, congestion. High latency= slow, laggy connection. Security: Sudden latency spike can signal an attack.
**OSI Model**
The Problem its solves: Back in the early days of networking every company made its own hardware and software. IBP computers were able to talk only IBM computers- DC nly talked with DC. Nothing worked together, it was chaos. So, in the 1980s the ISO that's the internation organisation for standardisation created the OSI that stands for open system interconnection. The OSI model is a conceptual framework, a way to describe how network communication should work. it devided into seven layers. Each layer has a specific job- communicates within the layers above or below. This separation helps vendors create to build differnt  pieces and as long as as each piece does its job correctly, everything works together. Makes troubleshooting easy- Example: Is this a Layer 3 or Layer 7 problem? Security: Every layer has its own attack surface and defence mechanisms. OSI=Open System Interconnection- created by ISO

**All 7 layer**

**1)** **Physical Bits**: [PDU(Protocol Data Unit. A PDU is the specific name for data at each layer of the OSI model): Bit]. Copper, Fiber, Radio waves, Connections(Physical transmission media and signaling). This layer handles: [Raw electrical signal transmission, Optical, Radio signal transmission]. **It is responsible for physically moving bits across media** Main Responsibilities: **Electrical signaling, Voltage levels, Timing, Connectors, Cable standards, Wireless frequencies, Data transmission speed**. Physical Media: **a)** **Copper Cable** Uses electrical signals. Examples: Ethernet cables (Cat5e, Cat6). Advantages: Cheap and Easy to install. Disadvantages: Electromagnetic interference, Shorter range. Main Responsibilities: **Electrical signaling, Voltage levels, Timing, Connectors, Cable standards, Data transmission speed**
**b)** **Fiber Optic Cable** [Uses light pulses]. Advantages: Very fast, Long-distance communication, Immune to electromagnetic interference. Disadvantages: More expensive, Fragile. Main Responsibilities: **Timing, Connectors, Cable standards, Data transmission speed**
**c)** **Radio Waves**: [Used in wireless communication]. Examples: Wi-Fi, Bluetooth, Cellular networks. Uses: [Electromagnetic radio frequencies]. Devices at Layer 1: Hubs, Repeaters, Cables, Connectors, NIC physical transceivers. Main Responsibilities: **Timing, Connectors, Cable standards, Wireless frequencies, Data transmission speed**
[**IP address = Logical identity
MAC address = Physical local identity
ARP = Translator between them**]
**2)** **DATA Link FRAME**: PDU:Frame. ethernet, WiFi(802.11), MAC(Media Access Control). Data Link Layer. PDU: Frame. **The Data Link layer packages packets into: Frames.** **Purpose: Local network delivery (hop-to-hop)**. Main Responsibilities: **MAC addressing, Error detection, Framing, Media access control(Ethernet collision handling
-Carrier Sense Multiple Access with Collision Detection (CSMA/CD),Wi-Fi channel access-Carrier Sense Multiple Access with Collision Avoidance (CSMA/CA)), Local delivery**. [Ethernet (Invented: 1973 at Xerox PARC. Standardized by: IEEE as IEEE 802.3 (1983). Typical speeds: 10 Mbps → 400 Gbps (and beyond). Transmission medium: Twisted-pair copper or fiber-optic cabling. Protocol: **Carrier Sense Multiple Access with Collision Detection** (CSMA/CD)). Ethernet operates at the physical BITS (Layer 1) and data-link FRAME (Layer 2) levels of the OSI model. **Devices share a medium using CSMA/CD, which minimizes data collisions by having each node “listen” before transmitting. Data is sent as frames, each containing source and destination MAC addresses, payload data, and error-checking codes. Modern switched Ethernet largely eliminates collisions by giving each link a dedicated path**.] Ethernet: Most common wired LAN technology. Ethernet frame contains: Source MAC, Destination MAC, EtherType [EtherType is a 2-octet (16-bit) field in an Ethernet II frame header that indicates which protocol is encapsulated in the payload. Used at the Data Link Layer (Layer 2), it tells the receiving device how to process the frame, acting as a demultiplexer for network protocols like IPv4 or ARP(Address Resolution Protocol).], Payload, FCS (CRC error checking). [Wi-Fi (802.11)]: IEEE 802.11, Wireless equivalent of Ethernet. Adds: Wireless authentication, Signal management, Radio coordination. [MAC Address] A hardware address assigned to network interfaces. Format: 00:1A:2B:3C:4D:5E, 48-bit hexadecimal value. Purpose: Local device identification, Error Detection. Uses: CRC(cYCLIC REDUNCEY CHECK)/FCS(fRAME CHECK SEQUENCE). Detects: Corrupted frames during transmission. 
[**1. DNS resolves google.com -> IP
2. ARP resolves local gateway IP -> MAC
3. Ethernet frame sent using MAC**
**4. Router forwards packet to internet**]
**3)** **NETWORK PACKET**: PDU: Packet. IP, ICMP, ARP(Layer 2.5 protocol-ARP operates between Layer 2 and Layer 3.). Network Layer-PDU: Packet. Responsible for: Logical addressing, Routing, End-to-end delivery across networks, IP (Internet Protocol), Internet Protocol. Provides: Source IP, Destination IP, Routing information. Examples: IPv4, IPv6, Routing. Routers examine: Destination IP Then decide:Best next hop/path. [TTL (Time To Live)-An 8-bit field. Purpose: Prevent infinite loops. Every router:Decrements TTL by 1. If TTL = 0: Packet dropped and ICMP Time Exceeded returned.] ICMP (Internet Control Message Protocol) Used for: Diagnostics, Error reporting. Examples: Ping, Traceroute. Common messages: Echo Request, Echo Reply, Destination Unreachable, Time Exceeded. 
**ARP (Layer 2.5)**: Because ARP bridges: Layer 2 (MAC) and Layer 3 (IP). Address Resolution Protocol. Converts: IP address → MAC address. Needed because:Ethernet delivers using MAC. Applications use IP. ARP Process- ARP Request. Who has 192.168.1.10? -Broadcast to all devices - ARP Reply - 192.168.1.10 is AA:BB:CC:DD:EE:FF Returned by target device. 

**TRANSPORT SEGMENT/DATAGRAM (Layer 4)**: PDU: Segment. TCP → Segment, UDP → Datagram. **Transport Layer**. PDU: TCP → Segment, UDP → Datagram. Purpose: Process-to process communication. Uses: Port numbers. TCP (Transmission Control Protocol): Reliable, connection-oriented protocol. Features: Sequencing
Acknowledgement, Retransmission, Flow control, TCP 3-Way Handshake (SYN → SYN-ACK → ACK),  TCP Connection Termination(FIN = "Let's end politely, "RST = "End now!"), Establishes connection. **Sequence Numbers Track**: Exact byte order. Allows: Reassembly of out-of-order packets. **ACK Numbers Confirm**: Successfully received bytes.
**UDP (Layer 4)**: User Datagram Protocol: Fast but unreliable. Features: No handshake, No retransmission, Minimal overhead. Used for: Streaming, Gaming, VoIP calls, DNS Queries. 

**SESSION Data (Layer 5)**: PDU: Data. **NetBIOS**(Network Basic Input/Output System)-Session communication in Windows networks, **RPC**(Remote Procedure Call)-RPC Allows One computer to execute functions on another computer, **SIP**(Session Initiation Protocol)-SIP is used for establishing, managing, and terminating VoIP sessions - Starting a WhatsApp or Zoom voice call. 
Session Layer. PDU: Data. Manages: Session establishment, Maintenance, Termination. Controls: Dialogs/conversations between systems. NetBIOS Provides: Session communication, Name services - Historically common in Windows networking, File and printer sharing. RPC (Remote Procedure CalL)- Allows: One computer to execute functions on another computer. Used heavily in: Distributed systems. SIP (Session Initiation Protocol) Used for: VoIP call setup - Responsible for: Starting, Managing
Ending calls.

**Presentation Data (Layer 6)**: PDU: Data. **TLS/SSL(Transport Layer Security)** - Encryption and secure communication. The lock icon in browsers indicates TLS encryption, **JPEG**-Image compression format, **MPEG**-Video/audio compression format, **ASCII**-Character encoding standard. It ensures: Data from one system can be understood by another. 
Presentation Layer. PDU: Data. Responsible for: Translation, Encryption, Compression, Formatting. **TLS/SSL**: Transport Layer Security. Provides: Encryption, Authentication, Confidentiality. Used by: HTTPS. **JPEG**: Image compression format. Purpose: Reduce image size. **MPEG**: Video/audio compression standard. Used for: Video streaming, Multimedia. **ASCII**: Character encoding standard. Converts:Characters ↔ Binary. Example: A = 65. 
**1. DNS resolves domain -> IP
2. TCP establishes connection
3. TLS encrypts communication (HTTPS)
4. HTTP transfers webpage data
5. Browser displays content**
**APPLICATION DATA (Layer 7)**: It provides: Network services directly to user applications. PDU: Data. **HTTP**(HyperText Transfer Protocol - Port 80) - Web communication, **HTTPS**(HTTPS is HTTP + TLS(Transfer layer security)/SSL (Secure Sockets Layer) - Port 443) Secure Web communication, **DNS** - (Domain Name System) - Domain name resolution, FTP (File transfer Protocol) - Domain names -> IP addresses, **SMTP**((Simple Mail Transfer Protocol))- Sending email, SSH(Secure Shell-port -22)-Secure remote access. 
Application Layer. PDU: Data. Closest layer to the user. Provides: Network services directly to applications. HTTP - Hypertext Transfer Protocol - Used for: Web communication. Default port: 80.  HTTPS (HTTP + TLS/SSL) Provides:  HTTP running inside TLS encryption - Secure encrypted web traffic. Default port: 443. DNS (Domain Name System) Converts: Domain names → IP addresses. Example: google.com → 142.250.x.x. FTP (File Transfer Protocol) Used for: File transfers. SMTP (Simple Mail Transfer Protocol).Used for: Sending email. SSH(Secure Shell) Provides: Secure remote login, Remote Command execution, Secure Tunneling, Encrypted communication between systems. Alternative to: Telnet
**HTTP Data
↓
TCP Segment
↓
IP Packet
↓
Ethernet Frame
↓
Bits on cable**


Network ID
Host ID
CIDR
Subnet mask
Private vs public IP
Default gateway

























































