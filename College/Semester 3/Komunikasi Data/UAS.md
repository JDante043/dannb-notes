# IP Addresses
- IP addressing operates in the 3rd Layer of the OSI Model
- Used to address a device (connect one device to another) and determine best path
- Every device in a network is assigned an IP address
## IPv4
- Contains 4 octets (`1.2.3.4`) of 8 bit integers (0-255)
- Consists of 5 classes:
	- A
	- B
	- C
	- D
	- E
- Network portion is globally assigned while host is locally assigned

## IPv6
- Contains 8 sections of 16 bit hexadecimal digits (`2001:cdba:0000:0000:0000:0000:3257:9652`)
- a section containing 0s can be "skipped" to shorten address (`2001:cdba:0000:0000:0000:0000:3257:9652` -> `2001:cdba::3257:9652`; notice the `::` in the middle)
- Larger address pool than IPv4
- No class limitation

## Public & Private IPs
### Public
- Global
- Routable / can connect to the internet and can be called from the internet
- Assigned by ISPs to their customers
- Numbering managed by IANA through Regional Internet Registries (RIRs):
	- AFRINIC: Africa
	- APNIC: Asia-Pacific
	- ARIN: North America
	- LACNIC: Latin America & The Carribeans
	- RIPE NCC: Europe, Middle East, and Central Asia
- Always outside of Private IP ranges

### Private
- Local
- Not routable / cannot connect to the internet
- Assigned by local network administrators
- Numbering managed by local network administrators
- Predefined for each class

## Classes

| Class | First octet range |      IP Address Range       | Network (N) and Host (H) grouping | Standard Subnet Mask |    CIDR     |    Network Number    |     Host Number     |
| :---: | :---------------: | :-------------------------: | :-------------------------------: | :------------------: | :---------: | :------------------: | :-----------------: |
|   A   |       0-127       |  0.0.0.0 - 127.255.255.255  |              N.H.H.H              |      255.0.0.0       |  0.0.0.0/1  |     128 ($2^7$)      | 16,777,216 ($22^4$) |
|   B   |      128-191      | 128.0.0.0 - 191.255.255.255 |              N.N.H.H              |     255.255.0.0      | 128.0.0.0/2 |   16384 ($2^{14}$)   |  65,536 ($2^{16}$)  |
|   C   |      192-223      | 192.0.0.0 - 233.255.255.255 |              N.N.N.H              |    255.255.255.0     | 192.0.0.0/3 | 2,097,152 ($2^{21}$) |     256 ($2^8$)     |
|   D   |      224-239      |  224.0.0.0-239.255.255.255  |                 -                 |          -           |      -      |          -           |          -          |
|   E   |      240-255      |  240.0.0.0-255.255.255.255  |                 -                 |          -           |      -      |          -           |          -          |

# Twisted Pair Cables
A cable that is comprised of smaller twisted pair cables. They range in colour (Blue, Orange, Green, Brown) with each colour having their own partner, usually striped white.
## Types
- Unshielded, plain twisted pair cables
- Foiled, each twisted pair is covered with a thin protective sheath
- Shielded, plain twisted pair, but inside a protective layer
- Shielded Foiled, each twisted pair is covered AND all of them are inside a protective layer

# Switching
A switch is a multiport bridging hardware whose job is to "switch" data frames (sends data to their destination). That is to say, the forward frames.
## Advantage & Disadvantages
+ Divides a LAN into multiple collision domains
+ Reduce the likelihood of collision
+ Increase bandwidth utilization efficiency
+ Support multiple simultaneous conversations
+ Isolate data traffic between segments

- Unable to limit broadcast data

## Layer 2 & 3
Layer 2 switches operate using MAC addresses. Dividing networks into several collision domains and operating within a broadcast domain. E.g. Switch & bridges.
Layer 3 switches uses IP addresses. E.g. Layer 3 switch & routers.

## LAN Segmentation
LAN Segmentation creates a new collision domain, which reduces collisions, isolates traffic within a segment, increases bandwidth for each user, improves general network performance and response time, and bandwidth utilization.

## Switch combinations
- Switch-hub is useful to improve network efficiency and performance and operates in one broadcast address
- Switch-router is useful to integrate multiple networks

## Content Address Memory (CAM)
"RAM" untuk switch yang menyimpan alamat MAC device yang terkoneksi. Switch akan mengganakan CAM untuk meneruskan frame ke device yang tepat

## Switch Broadcasting
Broadcasting = Forward data to all ports. Happens when:
- The data is a broadcast frame (FF:FF:FF:FF:FF:FF)
- Data is intended for other networks
- Destination is not in CAM

Broadcast means sending data to all devices in a broadcast domain, which is a collection of collision domains connected by a layer 2 device.

# 3 Layer Hierarchical Model
- Access, Distribution, Core Layer
- Used to simplify network design
- Divides the functional roles of each switch in the network architecture. A switch can operate across multiple layers simultaneously.

## Internal switch structure
- Memory buffer, temporarily store data before forwarding to destination
	- Either each port has a memory (port based) or a shared memory
- Packet loss, switch drops packets when memory is full
- Call Blocking, a condition in which data cannot be delivered to the destination because no available path exists between the input port and the output port.

## Forwarding types
- Store & Forward, receives the entire data frame fully before forwarding
- Cut Through, immediately forwards the entire data without buffering / loading the entire frame
- Fragment Free, waits to receive the first 64 bytes before forwarding, reduces the chance of forwarding corrupted or collision fragments

# VLAN
- A Virtual LAN is a virtual logical segmentation of devices. The default VLAN is VLAN1, and there must be a single device in VLAN1 (usually the router itself).
- A VLAN is equal to a broadcast domain.
- A device in a VLAN cannot communicate with devices in another VLAN without the router
- VLANs are assigned either using ports on a switch, mac addresses of devices, or protocols used
- VLANs are great for increasing the flexibility and scalability of networks, controlling broadcast traffic, and improving communication security within the network
- Static VLANs are port-centric, easier to configure and monitor setup. Dynamic VLANs are database-driven, more complex type of VLAN that allows fine grained control over membership and allows easy maintenance once it is correctly setup
- Trunk links are used for connecting network nodes together (Routers with Switches, Switches with switches)
- Access links are used for connecting end devices with network nodes
- VLANs can either be "End-to-end", where each VLAN corresponds to a category and does not depend on physical connection. This type of VLAN follows the 80/20 rule and allows a single VLAN to apply a security policy to its members. Rr "Geographic / local VLANs", where each VLAN corresponds to a physical connection and uses the 20/80 rule. Users can easily switch VLANs by moving locations.
# Routing
Routing is a process carried out by a router to deliver data packets to their destination.

Routing information:
- Destination address
- Source information
- Possible Routes
- Best Route
- Routing Information & Verification

## Routing Table
A table that contains a list of all routes to existing networks.
Information in Routing Table:
Protocol Type
C = Directly Connected Network.
S = Static Route.
R = Routing Information Protocol (RIP).
I = Interior Gateway Routing Protocol (IGRP).
E = Enhanced Interior Gateway Routing Protocol
(EIGRP).
O = Open Shortest Path First (OSPF).
Next Hop Association
Administrative Distance
Routing Metric
Outbond Interfac
### Static Routing
- Manually configured by the network admin
- Router stores configuration in routing table
- Router uses routes in routing table to route packets
- will fail if configuration is deleted or the next hop address is down
- can serve as backup route
- can send data to an address if routing protocol fails to generate
- used as a route to a stub network
- default gateway / last resort
- faster to configure

### Dynamic routing
- Uses a routing protocol
- Network admin only needs to configure the router used
- Any changes made to the route is configured automatically
- high level of scalability
- may cause routing loops if exchanged information is incorrect

### Default route
- gateway of last resort
- only used when no other matching routes
- if default route isn't configured, the packet is dropped

## Trunking
A mechanism that combines physical and logical connections, allowing traffic to be carried across the network between two switches or between a switch and a router.

Purpose:
- To combine multiple virtual links into a single physical link.
- To save port usage when creating links between several devices, where each device consists of multiple VLANs.
# Routing Protocol
- Operates at 3rd layer of the OSI Model
- Handles data packet format and delivery mechanism
- Is a communication tool between routers to exchange information
- Incluse Link-state and Distance vector routing protocol

## Distance Vector Routing Protocol
- Uses the Bellmand-Ford Algorithm
- Determines route based on distance and direction
- uses a routing table
- sends the entire content of the routing table
- sends routing updates to directly controlled devices
- sends routing updates periodically
- Features: Routing table
- Example:
	- Routing Information Protocol (RIP)
	- Interior Gateway Routing Protocol (IGRP)
	- Border Gateway Protocol (BGP)
	- Routing Table Maintenance Protocol (RTMP)
	- DEC's DNA Phase 4

## Link-State Routing Protocol
- Uses the Djikstra Algorithm / SPF (Shortest Path First) Algorithm
- Responds quickly to changes in the network
- Triggered updates
- Sends Link State Advertisement (LSA) periodically
- sends only a part of its routing table
- sends routing update to all routers in the network
- Features: LSA, Topological Database, SPF Algorithm, SPF Tree, Routing Table
- Example:
	- Open Shortest Path First (OSPF)
	- Intermediate System to Intermediate System (ISIS)

+ Fast Convergence
+ Supports classless addressing
+ Supports summarization
- High memory and processor requirements
- Requires large bandwidth during initialization

# RIP
- Uses distance vector routing protocol
- uses hop count to determine best route
- max hop is 15
- sends routing updates via broadcast every 30 seconds
- timers:
	- hold-down: 180 seconds
	- invalid: 180 seconds
	- flush: 240 seconds
- default administrative distance of 120
- classfull addressing only
- supports up to 6 equal cost loading balancing paths, default is 4
# IGRP
- Cisco proprietary protocol
- administrative distance of 100
- timers:
	- update: 90 seconds
	- hold-down: 280 seconds
	- invalid: 270 seconds
	- flush: 630 seconds
- Uses an autonomous system number during configuration.
- Uses metrics such as bandwidth and delay (static metrics) and load, reliability, and cost (dynamic metrics).
- Supports 6 unequal-cost load balancing paths.
- Supports only classful addressing.
- It is a distance vector and an Interior Gateway Protocol (IGP).
- Sends updates only to directly connected routers.
- Sends the entire contents of its routing table.
- 