# CompTIA Security+ Exam (SY0-501): Technologies and Tools

- This domain accounts for 22% of the questions on the real exam

We'll be focusing on 

- installing and configuring network components to support enterprise security
- using tools to assess the security posture of an organization
- trouble shooting common security issues
- analyzing and interpreting output from security technologies
- deploying mobile devices securely
- and implementing secure protocols. 



## 1. TCP/IP Suite

### 1.1 Introducing TCP/IP

Transmission Control Protocol/Internet Protocol

TCP and IP are two of the main protocols that make up all modern networks. 

#### Internet Protocol

- Routes information across networks
- Provides an addressing scheme
- Delivers packets from source to destination
- Serves as a network layer protocol

It supports other transport layer protocols that have higher-level responsibilities. The two main transport layer protocols are **Transmission Control Protocol (TCP)** and **User Datagram Protocol (UDP)**

#### TCP

- Is a connection-oriented protocol
- Guarantees delivery through acknowledgement
- Is widely used for critical applications

TCP is responsible for the majority of Internet traffic. It is a connection-oriented protocol, meaning that it establishes connections between two systems before transferring data. TCP is also a reliable protocol that guarantees delivery by having the destination system acknowledge receipt of every packet. TCP's reliability makes it widely used for applications that require this guaranteed delivery, such as email and websites. 

##### TCP Flags

- SYN: opens a connection
- FIN: closes a connection
- ACK: acknowledges a SYN or FIN

##### TCP Handshake

![TCP_handshake](https://github.com/Jingy1Ma/CompTIA-Security-Exam-SY0-501/blob/main/Images/2_Technologies_and_Tools/01_01_TCP_Handshake.PNG?raw=true)

In the first step, the system originating the connection sends a packet with a SYN flag set. This indicates that it would like to open a connection to the destination system. The destination system receives this packet and replies with another packet that does two things: It acknowledges the original connection request and then asks to open a reciprocal connection in the other direction. This packet has both the SYN and ACK flags set, and is known as the SYN/ACK packet. Finally, the original system receives the SYN/ACK packet, and sends a final ACK to the destination system, completing the reciprocal connection. Once the three-packet sequence completes, the connection is open and the systems may begin exchanging data. 

#### UDP

- Is a lightweight, connectionless protocol
- Doesn't send acknowledgements or guarantee delivery
- Is used for voice and video applications

#### OSI Model

![OSI_Model](https://github.com/Jingy1Ma/CompTIA-Security-Exam-SY0-501/blob/main/Images/2_Technologies_and_Tools/01_01_OSI_Model.png?raw=true)

1st layer: sends bits over the network using wires, radio waves, fiber optics, and other means

2nd layer: transfers data between two nodes connected to the same physical network

3rd layer: expands networks to many different nodes. The Internet Protocol works at this layer. 

4th layer: creates connections between systems and transfers data in a reliable manner. TCP and UDP are examples of transport layer protocols. 

5th layer: manages the exchange of communications between systems. 

6th layer: translates data so that it may be transmitted on a network. This layer describes how to represent a character in terms of bits, and performs both encryption and decryption. 

7th layer: determines how users interact with data using web browsers and other client applications. 

#### !EXAM TIPS

- Know the 7 layers of the OSI model



### 1.2 IP addresses

**IP Addresses** Uniquely identify systems

#### Dotted Quad Notation

192.168.1.100

#### Why the Range 0-255?

- 8-bit binary numbers
- $2^8=256$ possible values
- Start counting at 0
- Range: 0-255 (256 values)

#### IP addresses

- Uniquely identify systems on a network
- Must not be reused on Internet-connected systems
- May be reused if on private networks

#### Subnets

- Network address
- Host address

IP addresses are divided in two parts. The network portion of the address identifies the network a system is connected to. Your company for example, may have its own network address. The second portion of the address, the host address, uniquely identifies a system on that network. 

In this example, the network address is 192.168 and the host address is 1.100. The dividing line is right in the middle of the address, but it doesn't have to be. 

#### Source and Destination

![Src_Dst](https://github.com/Jingy1Ma/CompTIA-Security-Exam-SY0-501/blob/main/Images/2_Technologies_and_Tools/01_02_Src_Dst.PNG?raw=true)



The source address indicates the system's sending information, and the destination address indicates the system's receiving information. As two systems communicate back and forth, the source and destination addresses will swap places, depending upon who sends each packet. 

#### IPv6

- Replaces Ipv4 due to address exhaustion
- Uses 128 bits (compared to 32 for IPv4)
- Consists of 8 groups of 4 hexadecimal numbers
- Example: fd02:24c1:b942:01f3:ead2:123a:c3d2:cf2f



### 1.3 Domain and name service

#### DNS Servers

- Translate domain names into IP addresses
- www.lynda.com -> 192.229.162.23
- DNS functions over UDP port 53

Every time you connect to a network that network provides your computer with the IP address of a local DNS server that it can use to look up IP addresses. 

#### DNS Functioning

1. User types domain name into browser
2. Computer sends a DNS query to the local DNS server
3. DNS server responds with an IP address
4. Computer contacts the server at that IP address

If the local DNS server doesn't know the answer to your question, it contacts other DNS servers to determine the correct answer, and then responds to you. 

#### A Hierarchical System

- Organizations designate servers that are authoritative for their domains

When a local DNS server needs to perform a DNS lookup, it asks a series of questions that eventually lead it to the definitive answer from the DNS server that is authoritative for a domain. 

#### Dig

Most of the time, DNS queries happen behind the scenes and computer users never see them. However, we can use a tool called Dig to perform DNS lookups manually. 

```bash
dig www.lynda.com

; <<>> DiG 9.11.3-1ubuntu1.7-Ubuntu <<>> www.lynda.com
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 59389
;; flags: qr rd ra; QUERY: 1, ANSWER: 3, AUTHORITY: 0, ADDITIONAL: 1

;; OPT PSEUDOSECTION:
; EDNS: version: 0, flags:; udp: 4096
;; QUESTION SECTION:
;www.lynda.com.                 IN      A

;; ANSWER SECTION:
www.lynda.com.          263     IN      CNAME   www.lynda.com.cdn.cloudflare.net.
www.lynda.com.cdn.cloudflare.net. 263 IN A      104.18.1.28
www.lynda.com.cdn.cloudflare.net. 263 IN A      104.18.0.28

;; Query time: 11 msec
;; SERVER: 192.168.1.254#53(192.168.1.254)
;; WHEN: Tue Mar 23 03:16:26 PDT 2021
;; MSG SIZE  rcvd: 120
```

8.8.8.8 is actually a web server belonging to the Google public DNS service and anybody can use this server to perform DNS lookups. 



**Some content filters alter DNS query results** to prevent users from accessing undesirable websites. 

Those filters work by simply providing incorrect answers to DNS queries for those undesirable sites. If your organization uses this content filtering approach, you also need to make sure that you block outbound DNS requests sent to other organization's DNS servers. 



### 1.4 Network port

**Network ports, like apartment numbers, guide traffic to the correct final destination.**

#### Network Port Numbers

- 16-bit binary numbers
- $2^{16}$, or 65,536 possible values
- Start counting at 0
- Allowable range of 0-65,535

#### Port Ranges

- 0-1,023: well known ports
- 1,024-49,151: registered ports
- 49,152-65,535: dynamic ports

#### !EXAM TIPS

Memorize the list of common ports before taking the Security+ exam.

#### Administrative Services

- Port 21: File Transfer Protocol (FTP)
- Port 22: Secure Shell (SSH)
- Port 3389: Remote Desktop Protocol (RDP)
- Ports 137, 138, and 139: NetBIOS (Windows for network communications)
- Port 53: Domain Name System (DNS)

#### Mail Services

- Port 25: Simple Mail Transfer Protocol (SMTP): exchanges emails between servers
- Port 110: Post Office Protocol (POP): allow clients to retrieve mail
- Port 143: Internet Message Access Protocol (IMAP)

#### Web Services

- Port 50: Hypertext Transfer Protocol (HTTP)
- Port 443: Secure HTTP (HTTPS)

#### Memorize These Ports!

| Service | Port(s) | Service | Port(s) | Service | Port(s) |
| ------- | ------- | ------- | ------- | ------- | ------- |
| FTP     | 21      | SMTP    | 25      | HTTP    | 80      |
| SSH     | 22      | POP     | 101     | HTTPS   | 443     |
| RDP     | 3389    | IMAP    | 143     |         |         |
| NetBIOS | 137-139 |         |         |         |         |
| DNS     | 53      |         |         |         |         |



### 1.5 ICMP

The Internet Control Message Protocol, ICMP, is the housekeeping protocol of the internet. It performs a variety of important administrative functions. 

#### Ping Command

![Ping](https://github.com/Jingy1Ma/CompTIA-Security-Exam-SY0-501/blob/main/Images/2_Technologies_and_Tools/01_05_Ping.PNG?raw=true)



#### Traceroute

- Identifies network paths

Traceroute performs more detailed troubleshooting by not only showing you whether a system is alive on the network, but also showing the path over the network between two systems. 

#### Other ICMP Functions

- Destination unreachable
- Redirects
- Time exceeded
- Addresses mask requests and replies

The Internet Control Message Protocol plays an important role in maintaining a robust, healthy network and troubleshooting network connectivity issues.



### Chapter Quiz

1. What TCP flag indicates that a packet is requesting a new connection?

   A. RST

   B. PSH

   C. URG

   D. SYN

2. What technology provides the translation that assigns public IP addresses to privately addressed systems that wish to communicate on the Internet?

   A. TLS

   B. SSL

   C. HTTP

   D. NAT

3. Which one of the following ports is not normally used by email systems?

   A. 25

   B. 110

   C. 139

   D. 143

4. What command sends ICMP Echo Request packets?

   A. ssh

   B. ftp

   C. telnet

   D. ping



Answers:

1. SYN
2. NAT
3. 139
4. ping



## 2. Network Security Devices

### 2.1 Routers, switches, and bridges

#### Switches

- Switches reside in wiring closets and connect the computers in a building together.

- Ethernet jacks are at the other end of network cables connected to switches.
- Wireless access points (WAPs) connect to switches and create Wi-Fi networks.
- Switches generally work at Layer 2.
- Some switches do have Layer 3 capabilities

Switches do create networks, but they're limited to creating local networks. Switches generally operate at Layer 2 of the OSI model, the Data Link layer, where they work with Mac addresses only. Some switches have the capability to perform limited functions at Layer 3 of the OSI model, the Network layer, where they can interpret IP addresses. In those cases, switches are beginning to take on the functions of routers.

#### Routers

- connect networks together
- Router access control lists (ACLs) generally perform stateless inspections

Routers play a higher-level role, connecting networks together by serving as a central aggregation point for network traffic heading to or from a large network. The router serves as the air traffic controller of the network, making decisions about the best paths for traffic to follow as it travels to its final destination. Routers also perform some security functions using access control lists to limit the traffic that may enter or leave a network based upon the organization's security policies. This type of filtering using access control lists does not pay attention to connection state, and is known as stateless inspection.

#### Bridges

- Connect two networks together at Layer 2 using MAC addresses

Bridges, like switches, are Layer 2 devices, but they perform a very limited function. Bridges connect two networks together. They learn the MAC addresses present on each network, and then forward traffic between the networks as appropriate. 

#### Media Gateways

- Connect different telecommunications networks together

Media gateways perform a similar function, interconnecting networks that use different standards. You'll most often hear the term media gateway in connection with telecommunications networks such as 3G, 4G, LTE, PBX, and Voice over IP communication systems. Together, routers, switches, bridges, and media gateways make possible the interconnected nature of modern networking.

https://afteracademy.com/blog/what-are-routers-hubs-switches-bridges



### 2.2 Firewalls

If routers and switches are the connectivity building blocks of a network, firewalls are the security workhorses. 

**Firewalls act as security guards, blocking unwanted network traffic.**

#### Firewalls on the Network

Firewalls often sit at the network perimeter in between an organization's routers and the internet. From this network location, they can easily see all inbound and outbound connections. Traffic on the internal network may flow between trusted systems unimpeded but anything crossing the perimeter to or from the internet, must be evaluated by the firewall. 

![Firewall_1](https://github.com/Jingy1Ma/CompTIA-Security-Exam-SY0-501/blob/main/Images/2_Technologies_and_Tools/02_01_Firewall1.PNG?raw=true)

#### Firewalls Connect Three Networks

Firewalls often connect three networks together: the internet, an internal network, and a special purpose network known as the demilitarized zone or DMZ. 

![Firewall_2](https://github.com/Jingy1Ma/CompTIA-Security-Exam-SY0-501/blob/main/Images/2_Technologies_and_Tools/02_01_Firewall2.PNG?raw=true)

#### Demilitarized Zone (DMZ)

- Contains systems that must accept direct external connections
- Isolates those systems due to risk of compromise
- Protects internal network from compromised DMS systems

#### Stateful Inspection

- Tracks open connections

For example, when a user on the internal network requests a webpage from a server, the firewall notes that request and then allows the web server to respond and the two systems to communicate back and forth for the duration of the connection without reevaluating the request each time a new packet appears at the firewall. When the firewall encounters a new connection request it evaluates it against a set of rules created by system administrators. 

#### Firewall Rule Contents

- Source system addresses
- Destination system addresses
- Destination port and protocol
- Action (allow or deny)

![Firewall_Rules](https://github.com/Jingy1Ma/CompTIA-Security-Exam-SY0-501/blob/main/Images/2_Technologies_and_Tools/02_01_Firewall_Rules.PNG?raw=true)

| Attributes  | Values      |
| ----------- | ----------- |
| Action      | Allow       |
| Source      | Any         |
| Destination | 10.15.100.1 |
| Port        | 80          |
| Protocol    | TCP         |

For example, imagine that we have a web server located in our DMZ with the IP address 10.15.100.1. If we want users on the internet to access that system we must write a firewall rule that permits access from the internet into the DMZ. This is a rule that permits access so we set the action to allow. In this case the connection request would be coming from an unknown internet system to the web server. Since we do want anyone to have access to the website we set the source address on this rule to any. We do want to limit this access to the web server only so we set the destination IP address to 10.15.100.1. The IP address of our web server. We also want to limit access to resources on that system to the HTTP protocol which uses port 80, so we set the destination port as 80 and protocol as TCP. 

#### !EXAM TIPS

#### Implicit Deny Principle

If the firewall receives traffic not explicitly allowed by a firewall rule, then that traffic must be blocked. (This is a very important concept that is often tested on the security plus exam.)

#### Web Application Firewalls

Specifically protect web applications by using applications awareness to peer deep into the application layer and block web attacks. (They understand how the HTTP protocol works and peer deep into those application connections looking for signs of SQL injections, cross site scripting and other web application attacks.)



### 2.3 Proxies

#### Proxy Server

![Proxy_Server](https://github.com/Jingy1Ma/CompTIA-Security-Exam-SY0-501/blob/main/Images/2_Technologies_and_Tools/02_03_Proxy_Server.PNG?raw=true)

Proxy servers are specialized servers that browse websites on behalf of end users. They serve as proxies, or intermediaries, that prevent users from directly connecting to websites. Normally, when a user connects to a website, the user system is in direct contact with the server, sending information back and forth. In a proxy situation, the proxy server sits in the middle of the connection. The user connects to the proxy server and the proxy server connects to the web server. All traffic then passes through the proxy server. 

#### Proxy Server Benefits

- Anonymization
- Performance Boasting
- Content Filtering

First, proxying provides anonymity. The web server never learns the network address of the actual user. Its logs only contain the address of the proxy server. Second, proxying provides performance benefits by caching. The proxy server can store copies of frequently requested pages and answer some user requests with those stored or cached copies, reducing the demand for network bandwidth. Finally, proxy servers can perform security tests, checking, for example, that users are not visiting websites containing malicious software. 

**Forward Proxies** work on behalf of clients.

**Reverse proxies** work on behalf of servers.

**Transparent proxies** work without the client or server's knowledge

Also known as in-line proxies, or forced proxies, these transparent proxy servers sit on the client's network, physically in between the client and the Internet. They intercept requests for web services and proxy them on behalf of the client. Now, this approach can cause numerous issues on the network, and doesn't work well with SSL or TLS encrypted communications. I

**Proxies can handle many applications, not just web traffic.**

It is possible to proxy any application, and proxy servers may be set up as multi-purpose proxies that handle a wide variety of different network applications. Proxy servers play a valuable role in securing network communications.



### 2.4 Load balancers

Load balancers help web servers scale by distributing the workload among multiple servers.

#### Web Server

![Web_Server](https://github.com/Jingy1Ma/CompTIA-Security-Exam-SY0-501/blob/main/Images/2_Technologies_and_Tools/02_04_Web_Server.PNG?raw=true)

Basic web server configurations look something like this. Assigning an IP address to a web server located on a DMZ network. Network administrators then create a DNS entry that ties registered domain name for the server let's say www.myserver.com to the IP address of that server. Then when users type myserver.com into their web browser they connect to that web server located in the DMZ. This works well as long as the web server can keep up with those requests from users. Eventually, if the website grows the demand for the content will exceed the capacity of the server. Administrators might respond by making the server bigger but eventually the demand may grow again requiring a bigger and bigger server. This approach is not scalable because eventually administrators won't be able to purchase a bigger server and it'll also be left with a big pile of unused smaller servers gathering dust. 

#### Load Balancing

![Load_Balancer](https://github.com/Jingy1Ma/CompTIA-Security-Exam-SY0-501/blob/main/Images/2_Technologies_and_Tools/02_04_Load_Balancing.PNG?raw=true)

The more efficient way to grow server capacity is to use a technique known as load balancing where several servers share the load. They all sit behind a device known as the load balancer that determines which server will answer each user request. The DNS entry for the web domain doesn't point directly to a web server but instead points to the load balancer. This address is known as a virtual IP address and is published to the world as the IP address corresponding to the website but it is actually answered by the load balancer. As demand increases, administrators can simply add more servers sometimes automatically using a technique called auto scaling. 

#### Load Balancer Security Functions

- SSL certificate management
- URL filtering
- Other web application security tasks

#### Scheduling Algorithms

**Round-robin scheduling** Each server gets an equal number of requests.

While this approach is simple and may seem fair, it's not always efficient. If one server is more powerful than the others it can handle a greater load. Also, if a server gets a particularly intense request that requires more CPU time, it may not be able to handle as many other requests at the same time. 

**Advanced scheduling algorithms choose servers based upon performance and available capacity.**

#### Session persistence

- Routes an individual user's requests to the same server

Some applications require that users return to the same server for future requests to maintain information about session state.

#### 2 Modes

Load balancers play an important role on networks but they also serve as a single point of failure. Therefore organizations that adopt load balancers should maintain them in a high availability mode. This involves having two or more load balancers set up in one of two topologies. 

- Active-Active: two or more load balancers actively handle network traffic and continue to function with diminished capacity if one device fails
- Active-Passive: One load balancer handles all traffic while a second monitors activity and assumes responsibility if the primary load balancer fails

In the 2nd approach you have no loss of capacity during a failure or event, but most of the time the passive load balancer sits unused. 

Load balancing is an important way to scale applications by distributing the load among multiple servers.



### 2.5 VPNs and VPN concentrators

- Site-to-Site VPNs: Connect remote offices to each other and headquarters
- Remote Access VPNs: provide remote access to corporate networks for mobile users

#### Virtual Private Networks

![VPN](https://github.com/Jingy1Ma/CompTIA-Security-Exam-SY0-501/blob/main/Images/2_Technologies_and_Tools/02_05_VPN.PNG?raw=true)

VPNs work by using encryption to create a virtual tunnel between two systems over the internet. Everything that enters one end of the tunnel is encrypted and then it is decrypted when it exits the other end of the tunnel. From the user's perspective, the network appears to function normally. But if an attacker gains access to traffic between the two secure end points, all they see is encrypted information that they can't read.

#### VPN Endpoints

- Firewalls
- Routers
- Servers
- VPN concentrators

All of these approaches provide secure VPN connections but organizations that have high volumes of VPN use often choose to use a dedicated VPN concentrator because these devices are very efficient at VPN connections and can manage high bandwidth traffic with ease. 

If you don't have a high volume of VPN traffic, you might choose to use the firewall, router or server approach. If you do go that way, be warned that VPN traffic requires resource intensive encryption and unlike VPN concentrators, firewalls, routers and servers usually don't contain specialized hardware that accelerates encryption. Using these devices as VPN endpoints can cause performance issues. 

#### Two VPN Protocols

##### IPSec

- Network layer VPN protocol commonly used for site-to-site VPNs but difficult to configure

For many years most VPN use a protocol called IPSec, short for Internet Protocol Security to create these encrypted tunnels. IPSEC works at the network layer of the OSI model and provides robust, secure transport, but it is often difficult to configure and maybe blocked by firewalls. For that reason IPSec is often used for static, site to site VPN tunnels, but it is becoming less common for remote user VPNs. 

##### SSL/TLS

- Application layer VPN protocol commonly used for remote access VPNS and easier to configure

Remote user VPNs now often rely upon SSL or TLS VPNs that work at the application layer. These VPNs work on any system with a web browser and use port 443 for communications. A network that is typically allowed through almost every firewall. 

#### Two Tunnels

##### Full-Tunnel VPN

- All network traffic leaving the connected device is routed through the VPN tunnel, regardless of its final destination

##### Split-Tunnel VPN

- Only traffic destined for the corporate network is sent through the VPN tunnel. Other traffic is routed directly over the network

In most cases, administrators configure the split tunnel to send traffic headed for corporate systems through the VPN, while allowing regular internet traffic to go directly to the destination over the local network. This approach is often set up to reduce the burden on VPNs and conserve bandwidth. 

**Split-tunnel VPNS provide users with a false sense of security.**

Today most security experts recommend against the use of split-tunnel VPNs. End users generally don't understand the difference between split-tunneling and full-tunneling and they assume, incorrectly, that if they connect to a VPN, all of their network traffic is secure. 

#### Always-on VPN

- Connects automatically

In this strategy, all corporate mobile devices are configured to automatically connect to the VPN whenever they are powered on. This takes control away from the end user and ensures that traffic leaving the device is always protected by strong encryption. 

Virtual Private Networks provide administrators with the ability to secure an otherwise insecure communications mechanism and create private networks using inexpensive internet connections.



### 2.6 IPsec

When the developers of network technology created the TCP/IP protocol suite, they honestly didn't pay too much attention to security. This has created a dilemma for cyber security professionals ever since. We have a set of protocols that we rely upon every day that were designed without security in mind, and we now need to retrofit them to add on security capabilities. 

#### Internet Protocol Security

- Adds security to TCP/IP
- IPSec secures the entire packet payload

IPSec framework, is a set of protocols designed to add security capabilities to TCP/IP networking. Unlike TLS, IPSec reaches deep into the protocol stack and provides security for the entire payload of encrypted communications. 

#### Two Protocols

##### Encapsulating Security Payload (ESP)

- Provides confidentiality and integrity protection for packet payloads

##### Authentication Headers (AH)

- Provides integrity protection for packet headers and payloads

**You can combine ESP and AH.**

A single communication may combine both ESP and AH to achieve confidentiality for packet payloads in conjunction with integrity verification for the entire packet, including the header.

#### Security Associations (SAs)

- Identify cryptographic algorithms

Each system participating in IPSec makes available a list of cryptographic protocols and hash functions that it is configured to support. Each pair of cryptographic protocol and hash function is known as a security association. Systems that wish to communicate with each other compare their lists of security associations to find the strongest security association that they have in common, and then they communicate using those algorithms. 

#### Support VPN

IPSec may be used to support virtual private network, or VPN connections of two different types. 

##### Site-to-Site VPNs

- Encrypted tunnels connecting two networks together in a manner that is transparent to users

First, administrators may create IPSec tunnels to connect two different sites together. In this approach, the connection is transparent to end users. From the user's perspective, the two sites are simply connected to each other and may be contacted directly over the network. However, when traffic moves between the two sites, is travels through the encrypted IPSec tunnel, which protects the traffic so that it may safely travel over a public network without worrying about confidentiality. This is known as **tunnel mode**. 

##### End-User VPNs

- Provides encrypted remote network access for individual systems

The second option is that end users may use IPSec VPN clients to connect individual computers to a remote network. This is known as **transport mode**. 

IPSec based VPNs were once quite common, but are now falling out of use in favor of easier to use TLS spaced VPNs.



### 2.7 Network intrusion detection and prevention

#### Intrusion Detection Systems

- Monitor network traffic
- Alert administrators to suspicious activity, such as 
  - SQL injection (request for a web server)
  - Malformed Packets (attempting to create a DoS)
  - Unusual Logins
  - Botnet Traffic
- Require someone to monitor and take appropriate action

#### Intrusion Prevention Systems

- Block suspicious activity automatically

#### Two Types of Mistakes

##### False Positive Error

- IDS/PIS triggers an alert when an attack did not take place.

##### False Negative Error

- IDS/IPS fails to trigger an alert when an actual attack occurs.

#### Two Types of IDS

##### Signature Detection Systems

- Contain databases with rules describing malicious activity
- Alert administrators to traffic matching signatures
- Fail to detect brand new attacks
- Reduce false positive rates

##### Anomaly Detection Systems

- Build models of "normal" activity
- Alert administrators to activity not matching the model
- Detect previously unknown attacks
- Increased false positive rates

#### ! EXAM TIPS

**Anomaly detection, behavior-based detection, and heuristic detection are the same thing.**

#### IPS Development Modes

##### 1. In-band (inline) deployments

- Device sits in the path of network communications.
- Device can block suspicious traffic from entering the network.

While this approach allows an active response, it also adds the risk that an issue with the IPS can disrupt all network communications because the in-band IPS is a single point of failure. 

##### 2. Out-of-band (passive) deployments

- Device connects to a SPAN port on a switch.
- Device can react **after** suspicious traffic enters the network.

The IPS can still react by sending commands to block future traffic from offending systems. But, it cannot stop the initial attack from entering the network because it only learns about that traffic after it has been sent.



### 2.8 Unified threat management

We've talked about a lot of different security devices in this course, and one of the major issues associated with them is that purchasing all of these devices can be very expensive, particularly for a small or midsized organization. 

**Unified threat management (UTM) systems combine multiple security functions in a single appliance.**

#### Basic UTM Functions

- Protecting network against attacks
- Blocking unsolicited traffic
- Routing traffic to and from the Internet

#### Additional Security Features

- VPN connectivity
- Intrusion detection
- Intrusion prevention

#### Small Business Features

- URL filtering
- Content inspection
- Malware inspection
- Email and spam filtering

**UTM devices still require careful security management and analytics.**



### 2.9 OAuth and OpenID Connect

The OAuth and OpenID Connect protocols provide a federated single sign on experience for the web. 

#### OAuth Providers

- LinkedIn
- Facebook
- Google
- Amazon

#### OAuth

- **Authorization** protocol designed to work across a variety of web services

OAuth is an authorization protocol. It doesn't perform authentication itself. This can be a little confusing because the name OAuth is ambiguous, and many people assume that it means authentication; it doesn't. Auth means authorization in this case. 

#### OpenID

- Identification and authentication protocol designed to work with OAuth

The OAuth and OpenID Connect protocols are commonly used on the **web** for authentication. 



### Chapter Quiz

1. What network device can connect together multiple networks?

   A. wireless controller

   B. router

   C. AP

   D. switch

2. What security principle does a firewall implement with traffic when it does not have a rule that explicitly defines an action for that communication?

   A. informed consent

   B. implicit deny

   C. separation of duties

   D. least privilege

3. Which one of the following devices helps networked services scale with increasing demand?

   A. web security gateway

   B. proxy server

   C. firewall

   D. load balancer

4. What network port is used for SSL/TLS VPN connections?

   A. 88

   B. 1521

   C. 443

   D. 80

5. Which one of the following network intrusion detection technologies requires frequent threat updates from the vendor?

   A. behavior-based

   B. signature detection

   C. heuristic

   D. anomaly detection



Answers: 

1. router
2. implicit deny
3. load balancer
4. 443
5. signature detection



## Reference

[1] https://www.linkedin.com/learning/comptia-security-plus-sy0-501-cert-prep-1-threats-attacks-and-vulnerabilities/



















## Reference

[1] https://www.linkedin.com/learning/comptia-security-plus-sy0-501-cert-prep-1-threats-attacks-and-vulnerabilities/