ROUTING PROTOCOLS (RIP & OSPF) 

1. Introduction 

Routing is the process of selecting the best path for transmitting data packets from a source device to a destination device across interconnected networks. In computer networks, routers perform this function by maintaining routing tables and using routing protocols. 

Routing protocols help routers communicate with each other and exchange information about network paths. These protocols dynamically update routing tables when network topology changes. Routing protocols are mainly classified into two types: 

Distance Vector Routing Protocols 

Link State Routing Protocols 

Two widely used routing protocols are Routing Information Protocol (RIP) and Open Shortest Path First (OSPF). 

These protocols help determine efficient routes in a network by using different algorithms and routing strategies. 

2. Routing in Computer Networks 

 

Routing is an essential function of the Network Layer in the OSI model. It determines how packets move across networks to reach their destination. 

Functions of Routing 

Discover available routes 

Select the best path 

Maintain routing tables 

Update network topology changes 

 
 ![image alt](https://github.com/mathankailashs/COMMUNICATION-NETWORK-SA-2/blob/31c08e274de13c1af8e44d9ec248dfe417ace707/What_is_a_Router-Diagram.jpg)
 

Types of Routing 

Static Routing 

Dynamic Routing 

Static Routing 

In static routing, the routing table is manually configured by the network administrator. It does not change automatically when network conditions change. 

Advantages: 

Simple to implement 

Secure 

Disadvantages: 

Not scalable 

Requires manual updates 

Dynamic Routing 

Dynamic routing automatically updates routing tables using routing protocols. 

Advantages: 

Automatically adapts to network changes 

Suitable for large networks 

Disadvantages: 

More complex 

Uses more bandwidth and CPU resources 

Dynamic routing protocols include RIP, OSPF, EIGRP, and BGP. 

3. Routing Information Protocol (RIP) 

Overview 

Routing Information Protocol (RIP) is one of the oldest and simplest dynamic routing protocols used in computer networks. It is based on the Distance Vector Routing algorithm. 

In RIP, routers exchange routing information with their neighboring routers at regular intervals. Each router shares its entire routing table with its neighbors. 

 
![image alt](https://github.com/mathankailashs/COMMUNICATION-NETWORK-SA-2/blob/52c0290e7685ca540754a072f5acf9975f308da7/what-is-rip-routing-information-protocol-example-0b0fad96363f15fc.jpg)
 

Working Principle of RIP 

RIP determines the best route based on hop count, which represents the number of routers a packet must pass through to reach the destination. 

Maximum hop count = 15 

Hop count 16 = unreachable 

Each router periodically sends its routing table to neighboring routers. 

Steps: 

Router sends routing table to neighbors 

Neighbor updates its routing table 

Best route with minimum hop count is selected 

Routing tables are updated every 30 seconds 

Characteristics of RIP 

Distance Vector routing protocol 

Uses hop count metric 

Maximum network diameter: 15 hops 

Periodic routing updates 

Slow convergence 

RIP Message Format 

RIP messages contain the following fields: 

Command field 

Version number 

Address family identifier 

IP address 

Metric (hop count) 

These messages are exchanged between routers to update routing tables. 

RIP Timers 

RIP uses several timers to manage routing updates. 

Update Timer – sends updates every 30 seconds 

Invalid Timer – marks route invalid after 180 seconds 

Hold-down Timer – prevents incorrect updates 

Flush Timer – removes route from table 

Problems with RIP 

RIP suffers from several limitations. 

1. Slow Convergence 

When network topology changes, it takes time for all routers to update their routing tables. 

2. Routing Loops 

Incorrect routing updates may create loops. 

3. Limited Network Size 

Maximum hop count limit restricts network size. 

Techniques to Improve RIP Stability 

Several techniques are used to reduce routing problems. 

Split Horizon 

Prevents a router from advertising routes back to the interface from which they were learned. 

Poison Reverse 

Advertises unreachable routes with infinite metric. 

Triggered Updates 

Updates are sent immediately when network changes occur. 

These techniques help reduce routing instability in RIP. 

4. Open Shortest Path First (OSPF) 

Overview 

Open Shortest Path First (OSPF) is a Link State Routing Protocol used in large enterprise networks. It is designed to overcome the limitations of RIP. 

OSPF uses the Dijkstra shortest path algorithm to calculate the most efficient route. 

Key Features of OSPF 

Link-state routing protocol 

Faster convergence 

Supports large networks 

Uses cost as metric 

Hierarchical network design 

OSPF routers share information about the state of their links with all routers in the network area. 

![image alt](https://github.com/mathankailashs/COMMUNICATION-NETWORK-SA-2/blob/d825be5704c920878537b9c7da088c6182851c45/ospf-operation-basic-advanced-concepts-ospf-areas-roles-theory-overview1.png)

Working of OSPF 

The OSPF routing process works as follows: 

Routers discover neighbors 

Routers exchange link-state information 

Each router builds a network topology database 

Shortest path tree is calculated using Dijkstra algorithm 

Routing table is updated 

OSPF Areas 

To improve scalability, OSPF divides the network into areas. 

An Autonomous System (AS) is divided into multiple areas. 

Types of routers in OSPF: 

Internal Router 

Backbone Router 

Area Border Router 

Autonomous System Boundary Router 

OSPF areas reduce routing traffic and improve performance. 

OSPF Link Types 

OSPF defines several link types. 

Point-to-point link 

Transient link 

Stub link 

Virtual link 

A stub link is connected to only one router, and packets enter and leave through the same router. 

OSPF Messages 

OSPF uses several types of messages: 

Hello Message 

Database Description Message 

Link State Request 

Link State Update 

Link State Acknowledgement 

These messages help routers maintain an updated view of the network. 

5. Advantages of RIP 

Easy to configure 

Requires less memory 

Suitable for small networks 

Simple implementation 

6. Advantages of OSPF 

Faster convergence 

Supports large networks 

Efficient bandwidth usage 

Hierarchical design 

Better scalability 

7. Applications of Routing Protocols 

Routing protocols are used in: 

Internet backbone networks 

Enterprise networks 

Data centers 

Telecommunications networks 

Cloud networking 

8. Future of Routing Protocols 

Modern networking technologies continue to evolve routing protocols for better scalability, security, and efficiency. Advanced protocols like BGP and software-defined networking are improving network management and routing performance. 

9.Routing – Real Time Analogy (Google Maps Navigation) 

https://support-cdn.route4me.com/2024/11/5cfca6fb-routes-map-overview.jpg 

 

Analogy 

Routing in computer networks is similar to Google Maps finding the best route to a destination. 

Explanation 

Your starting location → Source computer 

Destination location → Destination computer 

Roads → Network links 

Traffic signals / road conditions → Network metrics 

Google Maps → Router 

Google Maps analyzes all possible roads and selects the fastest or shortest route, just like routers choose the best path for data packets. 

 

10. OSPF – Real Time Analogy (City Traffic Control System) 

 

 

 

Analogy 

OSPF is similar to a city traffic control system. 

Explanation 

In a modern city: 

Traffic cameras monitor road conditions. 

Data is shared with a central control system. 

The system calculates the fastest route for vehicles. 

Similarly, OSPF routers share information about the state of network links and calculate the shortest path using Dijkstra’s algorithm. 

11. Conclusion 

Routing protocols are essential for efficient communication in computer networks. RIP and OSPF are two widely used dynamic routing protocols with different approaches to routing. 

RIP is simple and suitable for small networks, while OSPF is more advanced and designed for large and complex networks. Understanding these protocols helps network engineers design scalable and efficient networks. 

 

 ![image alt](https://github.com/mathankailashs/COMMUNICATION-NETWORK-SA-2/blob/31c08e274de13c1af8e44d9ec248dfe417ace707/What_is_a_Router-Diagram.jpg)
