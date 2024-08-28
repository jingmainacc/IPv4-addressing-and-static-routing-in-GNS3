<h1>IPv4-addressing-and-static-routing-in-GNS3</h1>

<h2>Code of the GNS3 Network Configuration</h2>

- Configuration scripts and network topology setup for addressing and static routing using GNS3
- Utilized IP addressing plan based on a calculated network prefix derived from the student's unique identifier
- Configured router interfaces, assigned IP addresses, and set up static routes across multiple subnets
<br />


<h2>Description</h2>
Developed and configured a network simulation using GNS3 to practice and demonstrate IPv4 addressing and static routing techniques. The project involved creating a network topology with multiple subnets, routers, and PCs, simulating a real-world network scenario. The network was divided into specific address blocks, and static routes were configured to ensure connectivity between different subnets. Successfully validated network functionality through rigorous testing, including pings between subnets, verification of routing tables, and setting up default gateways.

<br />


<h2>Technologies Used:</h2>

- Simulation Tools: GNS3
- Networking Concepts: IPv4 Addressing, Subnetting, Static Routing, Default Gateways
- Protocol: ICMP (for testing connectivity with ping)

<h2>Environments Used </h2>

- <b>GNS3 (Graphical Network Simulator)</b> 

<h2>Program walk-through:</h2>

<p align="center">
<br />
The entire network was divided into multiple subnets, each allocated for specific purposes such as Campus A, Campus B, reserved subnets, and point-to-point links. The partitioning followed a structured approach to ensure efficient IP utilization and future scalability.  <br/>
<br/>
<img src="https://i.imgur.com/1dY7wNn.png" alt="Disk Sanitization Steps"/>
<br />
<br/>
The network was visually represented in GNS3, showing the connections between routers, PCs, and subnets. This topology map illustrates the entire setup, including the main routers (R1, R2) connecting different campuses and the designated IP ranges for each subnet.: <br/>
<br/>
<img src="https://imgur.com/BS2ovHr.png" alt="Disk Sanitization Steps"/>
<br />
<br/>
Each PC within the network was assigned an IP address according to the pre-planned subnetting scheme. This step ensured that each device could communicate within its designated subnet and prepared the network for further routing configurations.
<br/>
<br/>
<img src="https://imgur.com/zFvyLRs.png"/>
<br />
<br/>
Each router's interface was configured with the appropriate IP addresses corresponding to their connected subnets. This step involved assigning IP addresses to the interfaces, ensuring that each subnet had a reachable router interface, which is crucial for intra- and inter-subnet communication.
<br/>
<br/>
<img src="https://imgur.com/FcpI1no.png"/>
<br />
<br/>
Static routes were configured on the routers to enable communication between different subnets. This involved specifying the next-hop addresses and route summaries to ensure efficient data routing across the network. These static routes allowed devices in one subnet to communicate with devices in another subnet within the same campus.
<br/>
<br/>
<img src="https://imgur.com/PJvl05Y.png"/>
<br />
<br/>
Each PC was configured with a default gateway, pointing to the router's interface in the same subnet. This configuration enabled the PCs to send traffic destined for other subnets to the router, facilitating inter-subnet communication.
<br/>
<br/>
<img src="https://imgur.com/3wqjJqJ.png"/>
<br />
<br/>
Additional static routes were configured on the VyOS router to manage inter-campus communication. This included setting up summarized routes for efficient traffic management and ensuring that each campus could communicate with the other through properly configured default routes.
<br/>
<br/>
<img src="https://imgur.com/WY4RCIh.png"/>
<br />
<br/>
After configuring static routes and default gateways, a final test was conducted to verify connectivity. The results showed that devices could now ping any other device, even those outside the immediate campus network. This confirmed that the routing configurations were correctly implemented, allowing full network communication across and beyond the campuses.
<br/>
<br/>
<img src="https://imgur.com/GMriKA6.png"/>
<br />
<br/>



<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
