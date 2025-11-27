# NetworkProject
Project for networks

# Plan
Building: 3 floors
offices per floors: 10 per floor
Departments: Admin, Sales, Engineering
Wireless Clients: max 5, supported
Servers: centralized (Star topology)
	1 server per floor (3 in total)
	3 vlans

# Hosting and Internet Users
Firewalls and DMZ
Internet Support: LAN/Ethernet
Shared Res: PC 30, Phone 30, Printer 6, Server 3

# Network Upgrade Plan
This plan evaluates a hypothetical small business with 30 employees across one 10,000 sq ft single-story building (100x100 ft dimensions, open office layout with concrete walls), currently using a bare-minimum consumer-grade router and daisy-chained 100Mbps switches. The desired state supports scalable growth to 50 users, reliable 1Gbps wired/wireless access, and enhanced security via centralized servers and firewalls.​

# Physical Structures
Status Quo: Single building, one floor, no structured cabling; devices connected via outdated Cat5 cables prone to failures.​
Desired: Install Cat6 cabling with patch panels for 48 ports, covering all areas including conference rooms; add cable management for future expansion.​
This resolves signal loss over distance and prepares for multi-building growth if needed.​

# Offices and LAN Clients
Status Quo: 30 offices/workstations loosely connected, segmented by departments: Sales (10 desktops), Engineering (12 laptops), Admin/HR (8 mixed). Daisy-chaining causes slow performance and loops.​
Desired: Fully connected star topology with managed Gigabit switches; 40 wired ports total.​
Upgrade eliminates congestion for department-specific VLANs (e.g., Engineering for high-bandwidth tasks).​

# Wireless Clients
Status Quo: Single consumer access point supports 20 wireless clients max; no guest separation, leading to interference and dead zones from walls.​
Desired: 3 enterprise Wi-Fi 6 access points (up to 150 concurrent clients); separate employee/guest SSIDs, no public hotspot.​
This fixes coverage gaps and secures against unauthorized access.​

# Servers
Status Quo: Peer-to-peer file sharing; no dedicated servers, causing access bottlenecks.​
Desired: Centralized model with 2 servers: 1 file/print server (NAS/Synology), 1 domain controller/DNS (Windows Server); add backup server.​
Centralization improves resource sharing and management scalability.​

# Hosting and Internet Users
Status Quo: Domain hosted externally; email via provider (e.g., Office 365); no internal mail server; FTP unsupported; private resources inaccessible externally.​
Desired: Hybrid hosting with internal file server; external email; enable secure FTP via VPN; remote access through VPN for private network.​
VPN ensures safe internet user access without exposing internals.​

# Firewalls and DMZ
Status Quo: Basic router NAT, no DMZ or zoning; vulnerable to threats.​
Desired: Enterprise firewall (e.g., pfSense) with DMZ zone for public web/email servers; internal trusted zone; perimeter filtering.​
Public servers accessible via port forwarding; dual firewalls for high security.​

# Internet Support
Status Quo: Shared ISP modem/router; employees access via basic Wi-Fi/Ethernet, throttled during peaks.​
Desired: Dedicated fiber ISP (500Mbps+); QoS rules prioritize business traffic.​
Segregates traffic for reliable VoIP/web access.​

# Shared Resources
Status Quo: 2 printers, ad-hoc file shares; unreliable access.​
Desired: Centralized printers (3 networked), file server, NAS for backups; VoIP conference system.​
Network Needs and High-Level Resolutions:

Slow speeds/congestion: Replace switches, add bandwidth.​

Wi-Fi dead zones: Deploy multiple APs.​

Security gaps: Implement VLANs/DMZ/firewall.​

No scalability: Modular hardware for growth.​

Cable issues: Structured Cat6 wiring.