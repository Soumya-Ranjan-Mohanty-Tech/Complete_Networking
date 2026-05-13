# Complete_Networking
Notes
Network is the collection of devices that are connected together.
IP address is a address of a device on a network IPv4 or IPv6 (WE ARE RUNNING OUT OF IPv4)
**1)** **Devices**(Anything with a chip and a connection)-Laptop has IP address like phone, server. Cables or WiFi Signals. Data travelling the network. 
Device. Switch(Connects device in local network). Router (Connects network and decides the route). Internet (The global highway-WAN). Server (The destination has a IP address too).
**Attacks**= **Data Breaches**(STOLEN THROUGH OPEN NETWORK **PORTS*). **Ransomware** (SPREADS ACROSS **NETWORK TO ENCRYPT FILES*). **Phihsing** (EXPLOITS **EMIL AND WEB PROTOCOL*). **Man in the Middle** (INTERCEPTS **UNENCRYPTED TRAFFIC*). DDoS Attacks (FLOODS **NETWORK BANDWIDTH* WITH GARBAGE). **Port Scanning** (Maps your **network's open doors*).
**2)** **Ports** are the logical endpoint. Port 80- Door for web traffic (HTTP). Port 443 - Secure web door (HTTPS). Port 25 is email (SMTP). Port 22 - SSH(Secure Shell)(Remote Access-Remote command line access). Port 53 - DNS - Domain Name System (Maps domain name to IP Address- Converts name to readable numbers for the computer)
**Protocol** - It is a set of rules thats ets the communication. HTTP (Rules for loading web pages- request+response). DNS (Rules for converting domain names to IP Address). TCP (Transfer Control Protocal - Rules for reliable, ordered data delivery).
**Types of Networks**
**PAN** (Personal Area Network- Range<10 meters- Bluetooth to earbuds). **LAN** (Local Area Network- Range is Building/Campus - Home WiFi(WLAN-Home WiFi uses 802.11 standards)/Office network) Security- Once inside LAN, attackers can see all other devices. Defence- Network Segmentation-  deivide LAN into isolated zones. **MAN** (Metropolitan Area Network- Range is City wide- University campus network). **WAN** (Wide Area Network- Range:Country/global- The internet Itself) - Data passes through ISPs, routers, data centres, undersea cables. Security: WAN traffic passes through many unknown hands. Defence: ENCRYPTION is essential for data travelling over a WAN. **VPN** (Virtual Private Network- Encrypted tunnel throgh a public network)
**Router**: Connects different network and creates traffic between them- Reads IP Address on each packet to decide where to send it. Everyhome has one-its your gateway to the internet. Work at Layer 3 of the OSI Model of Network Layer. Security: Compromised router means attackers controls all traffic. Defence: Strong Password.
**Switch**: Connects different devices within the same network. Smarter than "hub"- sends each message only to its target device. Tracks MAC address to know which device is on which port. Works on Layer 2 of the OSI model of Data Link Layer.  A HUB Broadcasts to everyone - a SWITCH is targetted and efficient. Security: MAC FLOODING forces a switch to act like a dumb hub. Attackers than see ALL TRAFFIC meant for everyone on that segment.
**Firewal**: Monitors and controls network traffic based on the rules.Can filter traffic by: IP address, port, protocol, content pattern(cache). Types: Stateless (packet filter), Stateful, Application-Layer (WAF). Security: Every enterprise has firewalls- they are the first line of defence. But attackers can bypass firewall_ defence in depth is essential.
**WAP**: Wireless Access Point is what creates WiFi network. It broadcasts a wireless signal that devices can connect to. Home router usually has a built in access point. In larger buildings they have dedicated access points mounted in the celling to provide Wifi Coverage. Security: Wireless networks are inherently more vulnerable than wired ones. Data is being broadcast through the air. Anyone within the range can attempt to capture. Thats why WiFi is encryption Like WPA2 or WPA3 matters so much.**Network interface card**- Every device that connects to the network has NIC, a network interface card. Its the hardware componenet in each device that handles network communication. It could be a physical Ethernet port (It is used to connect a device to a router or a modem via Ethernet cable) or a WiFi radio built into laptop. Every NIC has a UNIQUE Identifier called MAC Address.
**NIC** (Layer 1 -Network interface card- Hardware inside very device)- **Access Point** (Layer1-2 -Creates WiFi signals for wireless device connection)- **Firewall** (Layer 3-7 Inspects and controls traffic based on security rules)- **Switch** (Layer 2 -Connects device within a single network-LAN )- **Router** (layer 3 -Connects Networks and routes packets between them).
**Packets** Data travels as small packets through different routes than reassemble at the destination. Each packet contains piece of DATA, Source IP, Destination of IP, Information about how to reassemble at the destination, error checking information. Security: Packets SNIFFERS capture these- if unencrypted, everything is readable. **Etnernet Frame Header-Data Link**- Outer Envelop (Source and destination MAC Adress, Ether type - Layer 2)- It often ends with frame check sequnce(FCS) trailer to check for any physical transmission errors, A 4 byte cyclic redundancy check(CRC) at the very end of the frame- the reciever uses it to detect if bits were corrupted during physical transit- Max size 1500 byte. Focuses on local delivery between physical hardware (hop to hop). Ethertype: A 2 byte field inside the header. Identifies the inner protocol(usually ARP, IPv4 OR IPv6) in other words it indicates which network layer protocol is encapsulated inside the payload, Preamble: A 7 byte pattern of alltering 1s and 0s followed by a 1 byte Start Frame Delimiter. Syncs physical timing between network interfaces(Physical and virtual hardware componenets like NIC or WiFi card that connects a computer elctrical, optical, or radio signals into digital frames). **IP HEADER-Network**-Inner envelop(SourceIP+Destination IP, TTL, Protocol - LAYER 3) Focuses on Global routing across different networks(end to end device delivery). Its use Time To Live(TTL- A 8 bit field in IPv4 headers that sets the maximum lifespan of a packet to prevent it from looping infinitely - Hop counter is the mechanism behind TTL. Every router that forwards the packet decrements the TTL value by 1. If the number 0, the the router drops the packet and sends an erroe back) field to prevent packets from looping forever. Encapsulation: It treats the transport layer segment (TCP/UDP) as its own Payload. Protocol: Identifies the inner Layer 4 protocol (TCP/UDP). **TCP HEADER-Transport**- Internal delivery note  (Source and destination Port Numbers, SEQUENCE NUMBERS, FLAGS (ACK/SYN), Checksum- Layer 4). Focuses on managing connections and primarily directing data to the correct software application using port number(process to process delivery). Is Complex(20 Bytes)-It provides reliable delivery through sequence numbers and acknowledgement. Sequence number: A 32 Bit TCP field mapping the exact order/sequence of transmitted data bytes. It allows the reciever to reassemble fragmented or out of order packets correctly. Acknowledgement number: A 32 Bit  TCP field that indicates the next expected data byte sequence number. It confirms to the sender that all previous bytes were recieved successfully. Connection Flags: A 1 bit indicators in the TCP Header used to mange connection states. FLAGS(ACK/SYN): Specific connection flags. SYN(Synchronise) initiates a 3 way handshake to establish a connection. ACK(Acknowledgement) confirms recipt of the valid data or connection steps. **UDP HEADER-Transport** (Source and destination Port Numbers, Lenghth, Checksum- Layer 4) Focuses on directing data to the correct application using port number(process to process delivery). Simple(8Bytes) Offers best effort delivery with minimal overhead, ideal for speed-sensitive tasks like streaming. UDP Specifics: Simple checksum and basic length field. Simple checksum: Basic error validation-it lacks tracking flags of TCP. Length field: Total bytes of header plus the Data **DATA PAYLOAD-Application**-Actual content (My actual content(HTTP Request, email text)- Layer 7) It focuses on the actual information being trasferred, such as HTTP files, a DNS query, or a VoIP audio clip. Size: Varies based on the maximum Transmission Unit(MTU- The largest frame or packet size that a network can transmit without fragmenting it into smaller pieces) **Calculation**: For a 1500 Ethernet MTU, after substracting 20 bytes for the IP header and 20 Bytes for the TCP Header, The maximum payload size is typically 1460 bytes.
































































