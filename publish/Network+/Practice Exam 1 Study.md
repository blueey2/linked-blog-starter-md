# **Compare and contrast the Open Systems Interconnection (OSI) model layers and encapsulation concepts. (*1.1*)**
+ Data encapsulation and decapsulation within the OSI model context
	+ Encapsulation is when we add chunks of information to network data (IP, MAC, etc)
		+ Occurs when we send data from a computer
	+ Decapsulation is when we remove chunk's of information from network data when
		+ Occurs when we receive data at a computer
	+ ![](https://gyazo.com/92c1db1bfb9a8bb14f2b08b92bbfb9eb.png)
 # **Explain the characteristics of network topologies and network types (*1.2*)**
+ What is a network topology
	+ An arrangement of nodes of a computer network
	+ Topology can be viewed as a layout of the network
+ Physical topology and logical topology
	+ Physical topology means where you place all your nodes
	+ Logical topology means how the data is going to flow from one node to another
+ Network Topologies
	+ Bus
	+ Ring
	+ Star
	+ Mesh
	+ Hybrid
+ Bus Topology
	+ All data transmitted between nodes in the network is transmitted over a common transmission medium and is able to be received by all nodes in the network simultaneously
	+ A signal containing the address of the intended receiving machine travels from a source machine in both directions to all machines connected to the bus until it finds the intended recipient
	+ Everyone will receive a copy of the data sent over the network but all others that weren't suppose to receive data will reject it
+ Advantages and Disadvantages of bus topology
	+ Advantages
		+ Only one wire- less expensive
		+ Suited for temporary network
		+ Node failures don't affect other
	+ Disadvantages
		+ Not fault tolerant (No redundancy)
		+ limited cable length
		+ No security
+ Ring topology
	+ A ring topology is a bus topology in a closed loop
	+ Peer-to-peer LAN topology
	+ Two connections one to each of its nearest neighbors
	+ Unidirectional
	+ Sending and receiving data takes place with the help of a token
+ Advantages and Disadvantages of Ring Topology
	+ Advantages
		+ Performance better than bus topology
		+ Can cause bottleneck due to weak links
		+ All nodes with equal access
	+ Disadvantages
		+ Unidirectional. Single point of failure will affect the whole network
		+ Up in load down in performance
		+ No security
+ Star topology
	+ Every node is connected to a central node called a hub ort switch
	+ Centralized management
	+ All traffic must pass through the hub or switch
+ Advantages and Disadvantages of Star topology
	+ Advantages
		+ Easy to design and implement
		+ Centralized administration
		+ Scalable
	+ Disadvantages
		+ Single point of failure affects the whole network
		+ bottlenecks due to overloaded switch/hub
		+ Increased cost due to switch/hub
+ Mesh Topology
	+ Each node is directly connected to every other node in the network
	+ Fault tolerant and reliable (High Redundancy)
+ Advantages and Disadvantages of Mesh topology
	+ Advantages
		+ Fault tolerant
		+ Reliable
	+ Disadvantages
		+ Issues with broadcasting messages
		+ Expensive and impractical for large network
 # **Compare and contrast routing technologies and bandwidth management concepts (*2.2*)**
 + Routing
	 + Dynamic routing protocols
		 + Listen for subnet information from other routers
		 + Sent from router to router
		 + Provide subnet information to other routers
		 + Determines the best path based on the gathered information
	+ RIP (Routing information protocol)
		+ A distance vector protocol based on hop count matrix
		+ When a router forward a data packet to a network segment, it is counted as a single hop
	+ Disadvantages of RIP
		+ RIP is a class full routing protocol and it does not support VLSM
		+ Broadcasts the updates to the entire network and simply creates lots of traffic
		+ Bandwidth utilization is very high as it broadcast its update every 30 seconds
		+ Supports a maximum of 15 hops meaning 16 routers can be configured in RIP
	+ OSPF (Open Shortest path first)
		+ Link state routing protocol
		+ All routers have to be in the same area
		+ Routers exchange Link state information
# *Install and configure the appropriate wireless standards and technologies (*2.4*)*
+ WPA (Wifi protected access)
	+ The replacement for seriours cryptographic weaknesses in WEP
	+ Needed a short term bridge between WEP and whatever would be the successor
	+ WPA: RC4 with TKIP
		+ Initialization vector is larger and an encrypted has
		+ Every packet gets a unique 128 bit encryption key
+ WPA2 (Wifi protected access 2)
	+ Uses a block mode of encryption called CCMP
		+ Counter mode with cipher block chaning message authentication code protocol or counter CBC-MAC protocol
	+ CCMP security services
		+ Data confidentiality with AES encryption
		+ message integrity check with CBC-MAC
+ WPA3 (Wifi protected access 3)
	+ Instead of CCMP it uses GCMP
		+ Galois/Counter mode protocol
		+ A stronger encryption than WPA2
		+ Allows us to encrypt data using AES
		+ Includes a message integrity check (MIC) with galois message authentication code
+ WPA2 PSK problem
	+ Has a brute force problem
	+ Listen to the four way handshake
	+ Capture the hash
	+ With the hash attackers can brute force the PSK
	+ Has become easier as technology improves
+ WPA3 PSK
	+ WPA3 changes the PSK authentication process
		+ Includes mutual authentication
		+ Both devices can create a shared session key without having to send the session key across the network
		+ No more four way handshakes no hashes no brutes force attacks
		+ Adds perfect forward secrecy
	+ SAE (Simultaneous authentication off equals)
		+ A Diffie-Hellman Derived key exchange with an authentication component
# *Given a scenario, use the appropriate statistics and sensors to ensure network availability. (3.1)*
+ SNMP (Simple network management protocol)
	+ A databased of data (MIB) - Management information base
	+ The database contains OIDs - Object identifiers
	+ Poll devices over udp/161
+ SNMP v1
	+ Structed tables, Sent all information across network unencrypted
+ SNMP v2
	+ Data type enhancements, bulk transfers, still unencrypted
+ SNMP v3
	+ Message integrity, authentication, encryption
+ SNMP OIDs
	+ An object identifier can be reference by a name or number
+ Interface errors or alerts
	+ Runts
		+ Frames that are less than 64 bytes
		+ May be a result of a collusion
	+ Giants
		+ Frames that are more than 1518 bytes
	+ CRC error
		+ Failed the frame check sequence
		+ May indicate a bad cable or interface
	+ Encapsulation error
		+ Inconsistent configurations between switches
# *Explain the purpose of organizational documents and polices (3.2)*
+ Common documentation
	+ Floor plans
		+ Overlay the wired and wireless network with the existing architectural layout
		+ Can be useful for patch panel labels
	+ Physical network maps
		+ Shows how all of our equipment is connected together
		+ Great way to see the flow of data as it goes through the network
	+ Distribution frames
		+ Passive cable termination
		+ Located on the wall
	+ Main distribution frame (MDF)
		+ Central point of the network
			+ Usually in a data center
		+ Termination point for WAN links
			+ Connects the inside to the outside
		+ Good test point
			+ Tests in both directions
	+ Intermediate distribution frame (IDF)
		+ Extension of the MDF
		+ Connects the users to the network
	+ Logical network diagram
		+ High level views
			+ WAN layout, application flows
		+ Useful for planning and collaboration
	+ Site surveys
		+ Determine existing wireless landscape
			+ Sample the existing wireless spectrum
		+ Identify existing  access points
		+ Work around existing frequencies
	+ Baseline configuration
		+ Point of reference
		+ Understand how the performance was in the past
		+ Useful for planning
# *Explain high availability and disaster recovery concepts and summarize which is the best solution (3.3)*
+ Redundancy and high availability (*HA*) Concepts
	+ RTO (Recovery time objective)
		+ Maximum amount of time that a process or service is allowed to be down and the consequences still considered to be acceptable
	+ RPO (Recovery point objective)
		+ The maximum time in which transactions can be lost from a major incident how much your willing to walk away from to get everything up and running again.
	+ MTTR (Mean time to repair)
		+ A maintenance metric that measures the average time required to troubleshoot and repair failed equipment
	+ MTBF (Mean time between failure)
		+ The measurement of anticipated or predicted incidents of failure of a system 
	+ Active-active vs active-passive
		+ Active-Active
			+ Independent nodes in a networked server cluster have access to their own replicated database server.
		+ Active-Passive
			+ Not all nodes are active. If there are two nodes in an active-passive cluster one node will be up and running a service while the other is on standby ready to take over if active node encounters an issue.
		+ Multiple internet service providers (ISPs)/Diverse paths
		+ Virtual router redundancy protocol (VRRP)/First hop redundancy protocol (FHRP)
			+ Creates virtual routers that act as a group. The default gateway on a host is configured to the virtual router rather then a physical router, so if the physical router fails the redundant choice is already built into the group
			+ FHRP
				+ Used to prevent network failures at the default gateway. This is achieved by configuring multiple routers with the same IP address and mac address thus presenting the illusion of a single virtual router to the host in a LAN.
	+ Cold/Warm/Hot/Cloud site
		+ Cold sites
			+ Used by organizations that can handle a disaster for a day or 2 before they get back up and running
		+ Hot sites
			+ Something that can be turned on within a few hours and get buisness running quick
		+ Warm site
			+ Has things ready but not configured and ready to go
			+ Dedicated to the company
		+ Cloud site
			+ Avalible when needed but needs configurations
			+ Controlled by a provider
# *Explain common security concepts (4.1)*
+ Authentication methods
	+ Multi-factor authentication (MFA)
		+ Something you are
		+ Something you have
		+ Something you know
		+ Something you are
		+ Something you do
			+ Can be expensive
				+ Separate Hardware tokens
				+ Specialized scanning equipment
			+ Can be inexpspensive
				+ Free smartphone app
	+ RADIUS (Remote authentication Dial-in User service)
		+ One of the more common AAA protocols
			+ Supported on a wide variety of platforms and devices
			+ Not just for dial-in
		+ Centralize authentication for users
			+ Routers, switches, firewalls
			+ Server authentication
			+ Remote VPN access
			+ 802.1x network access
		+ Most popular types of authentiaction
	+ TACACS (Terminal Access Controller access-Control system)
		+ Remote authentication Protocol
		+ Created to control access to dial-up lines to ARPANET
	+ TACACS+
		+ Latest version of TACACS
		+ More authentication requests and response codes
		+ Primarily a cisco device
	+ LDAP (Lightweight Directory access protocol)
		+ Protocol for reading and writing directories over an IP network
			+ An organized set of records, Like a phone directory
		+ X.500 standard writted by the international telecommunications union (ITU)
		+ Primarily a microsoft network
	+ Kerberos
		+ Network authentication protocol
			+ Authenticate once, trusted by the system
			+ No need to re-authenticate to everything
			+ Supports mutual authentication preventing on path attacks or replay attacks
			+ Primarily a Microsoft network
		+ SSO with Kerberos
			+ Authenticate one time
				+ Lots of backend ticketing
				+ Cryptographic tickets
			+ No constant username and password input
	+ 802.1x
		+ Port based network access control (NAC)
		+ You don't get access to the network until you authenticate
		+ EAP integrates with 802.1x
			+ Extensible authentication protocol
			+ 802.1x prevents access to the network until the authentication succeeds
	+ EAP (Extensible authentication protocol)
		+ Many different ways to authenticate based on RFC standards
			+ Manufactures can build their own EAP methods

		
# *Compare and contrast common types of attacks. (4.2)*
+ Technology based
	+ Denial of service
		+ Force a service to fail
			+ Overload the services
	+ Friendly DoS
		+ Unintentional DoSing
		+ Bandwidth DoS
			+ Downloading multigigabit Linux distributions over a DSL line
	+ On-path network attack
		+ Attacker sits in the middle of a conversation and redirects the traffic as your sending it back and forth to another device
		+ ARP poisoning (Spoofing)
			+ On-path attack on the local IP subnet
			+ ARP has no security
			+ Attacker pretends to be the device your communicating to
		+ DNS Spoofing
			+ Performing an on-path attack to devices that are not on your network
				+ Modify the DNS server
			+ Send a fake response to a valid DNS request
	+ VLAN hopping
		+ Switch Spoofing
			+ Some switches support automatic configuration
			+ There's no authentication required
				+ Pretend to be a switch
				+ Send trunk negotiation
			+ Now you've got a trunk link to a switch
				+ Send and receive from any configured VLAN
		+ Double tagging
			+ Craft a packet that includes two VLAN tags
			+ The first native VLAN tag is removed by the first switch
				+ The second fake tag is now visible to the second switch
				+ Packet is forwarded to the target
			+ One way trip
				+ Responses dont have a way back to the source host
				+ Good for DoS
	+ Rogue services
		+ Rogue DHCP server
			+ IP addresses assigned by a non-authorized server
				+ Theres no inherent security in DHCP
			+ Client is assigned an invalid or duplicate address
				+ Intermittent connectivity, no connectivity
			+ DHCP snooping
				+ Automatically finds rogue servers and prevents them from communicating
				+ Authorize DHCP servers in Active directory
		+ Rogue Access point
			+ An unauthorized wireless access point
			+ Not necessarily malicious
			+ A significant potential backdoor
			+ Very easy to plug in
			+ Consider using 802.1x (NAC)
				+ You must authenticate, regardless of the connection type
		+ Wireless evil twin
			+ Looks legitimate but actually malicious
				+ The wireless version of phishing
			+ Configure an access point to look like an exsisting network
				+ Same (or similar) SSID and security settings/captive portal
			+ Overpower the existing access points
# *Given a scenario, apply network hardening techniques. (4.3)*
+ Best practices
	+ Secure SNMP
		+ Monitor and control servers, switches, routers, firewalls, and other devices
	+ Router advertisement (RA) Guard
		+ IPv6 includes periodic router announcements
			+ Automatic configuration for network devices
	+ Port security
		+ Prevents unauthorized users from connecting to a switch interface
			+ Alert or disable the port
		+ Based on the source MAC address
			+ Even if forwarded from elsewhere
		+ Each port has its own config
		+ Port Security operation
			+ Configure a maximum number of source MAC addresses on an interface
				+ You decide how many is too many
				+ You can also configure specific MAC addresses
		+ Dynamic ARP inspection (DAI)
			+ Relies on DHCP snooping for intel
				+ Knowing every devices IP can be valuable information
			+ Intercept all ARP requests and responses 
				+ Invalid IP to MAC address bindings are dropped
				+ Only valid requests make it through
		+ Control plane policing
			+ Manages the device
				+ Performs the operational processes
			+ Protect against DoS or reconnaissance
			+ Manage traffic
				+ Prioritize management traffic
				+ Block unnecessary control plane traffic types
				+ Rate limit the control plane traffic flows
		+ Private VLANS
			+ Port isolation
				+ Restrict access between interfaces
		+ Disabling unused interfaces
			+ Enabled physical ports
			+ Administratively disable unused ports
				+ More to maintain, but more secure
			+ Network access Control (NAC)
				+ Cant communicate unless authenticated 
		+ Disable unnecessaray ports and services
			+ Every open port is a possible entry point
			+ Control access with a firewall
			+ Unused or unknown services
		+ DHCP snooping
			+ Allows us to track IP addresses and mac addresses on this layer 2 device (Switch)
			+ Switch watches for DHCP conversations
				+ Adds  a list of untrusted devices to a table
		+ Access control list (ACL)
			+ Allow or disallow traffic based on tuples
				+ Grouping of categories
				+ Source IP, Destination IP, Port number, Time of day, etc.
			+ Restrict access to network devices
				+ Limit by IP address or other identifier
			+ Firewall rules
				+ Manage access from the firewall
				+ Most firewall rules include an implicit deny
					+ If there's no explicit rule, then traffic is blocked
+ Wireless Security
	+ MAC filtering
		+ Allows you to limit what mac address are allowed on your network so all others can be filtered out
		+ Easy to find working MAC addresses through wireless LAN analysis
			+ MAC addresses can be spoofed
		+ Wireless isolation
			+ Cant communicate with each other
			+ Useful in a hotel or public area
		+ Wireless security modes
			+ Open System
				+ No authentication password is required
			+ WPA/2/3-Personal /WPA/2/3-PSK
				+ WPA2 or WPA3 with a PSK
				+ Everyone uses the same 256 bit key
			+ WPA/2/3-Enterprise /WPA/2/3-802.1x
				+ Authenticates users individually with an authentication server (i.e. raidus)
			+ EAP (Extensible authentication protocol)
				+ An authentication framework
				+ Many different ways to authenticate based on RFC standards
					+ WPA2 and WPA3 use five EAP types as authentication mechanisms
			+ Geofencing
				+ Restrict or allow features when the device is in a particular area
			+ Captive portal
				+ Authentication to a network
					+ Common on wireless networks
# *Given a scenario, troubleshoot common cable connectivity issues and select the appropriate tools. (5.2)*
+ Common tools
	+ TDR, OTDR(Time domain reflectometer/Optical time domain Reflectometer)
		+ TDR used for copper connections
		+ OTDR used for fiber connections
		+ Estimates cable lengths
		+ Identifies splice locations
		+ Cable impedance information
		+ Signal losses
		+ Certify cable installations
	+ Fusion splicer
		+ Joins two ends of a fiber cable together
	+ Spectrum analyzer
		+ View everything communicating in the wireless frequency spectrum
+ Common issues
	+ Attenuation
		+ Usually gradual
			+ Signal strength diminishes over distance
			+ Loss of signal intensity as signal moves through a medium
		+ Electrical signals through copper, light through fiber
			+ Radio waves through the air
	+ Decibels (dB)
		+ No connectivity
			+ No signal
	+ Avoiding EMI and interference
		+ Cable handling
			+ No twisting dont pull or stretch
