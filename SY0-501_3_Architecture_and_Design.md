# CompTIA Security+ Exam (SY0-501): Architecture and Design

This domain accounts for 15% of the questions on the real test. We'll be focusing on

- explaining use cases for frameworks, best practices, and secure configuration guides
- implementing secure network architectures
- implementing secure system designs
- developing and deploying software in a secure manner
- securing embedded systems
- using the Cloud and virtualization securely
- using resiliency and automation to reduce risk
- implementing physical security controls



## 1. Security Design

### 1.1 Legislative and regulatory compliance

#### Compliance Obligations

- Criminal law
- Civil law
- Administrative law
- Private regulations

##### Criminal Law

- Deter and punish acts detrimental to society

Criminal laws have one important characteristic that is not found in any other type of law. Violations of criminal law may be punishable by The Deprivation of Liberty such as a jail sentence or probation. 

##### Civil Law

- Resolve disputes

Civil laws cover almost any matter that is not addressed by criminal law, including liability claims, estate probate, contractual disputes and other matters. Civil laws do not provide for the possibility of jail time. The most common outcomes of a successful civil lawsuit are monetary damages or orders by the court that someone perform or refrain from an action. 

##### Administrative Law

- Facilitate effective government

These regulations often provide details missing from the law or provide procedural rules for the operation of government. For example, the Health Insurance Portability and Accountability Act, HIPAA, provides criminal and civil law governing the uses of health information, but doesn't go into great detail. The Centers for Medicare and Medicaid Services publishes security and privacy regulations that provide the specific requirements that covered entities must follow. At the federal level, administrative law is found in the Code of Federal Regulations, or CFR. 

##### Private Regulations

- Flow from contractual relationships

The most common example of a private regulation in the world of cyber security is the Payment Card Industry Data Security Standard (PCIDSS). PCIDSS was created by a consortium of companies without the involvement of a government agency. This consortium then included language in the contracts for those accepting and processing credit cards that requires compliance with PCIDSS.

#### Fourth Amendment 

> The right of the people to be secure in their persons, houses, papers, and effects, against unreasonable searches and seizures, shall not be violated, and no warrants shall issue, but upon probable cause, supported by oath or affirmation, and particularly describing the place to be searched, and the persons or things to be seized

The Fourth Amendment comes into play any time a government agents, including law enforcement officers, wish to collect private information from computing systems without the owners consent. If they do this without a warrant, they run the risk of the evidence being inadmissible in court. 

**Federal Information Security Management Act (FISMA)**

A law that governs information security matters for federal agencies and government contractors. It requires the creation of security programs throughout the federal government and provides details on the controls necessary to run information systems that are categorized as FISMA High, FISMA Moderate, or FISMA Low.



### 1.2 Frameworks and reference architectures

#### Security Framework

- A collection of standards and practices designed to form a solid approach to information security

#### Reference Architectures

- A description of the **specific** controls that would achieve an organization's security objectives

Security frameworks are high level, and they're often focused on activities such as identifying risks and responding to attacks. Reference architectures get more into the technical details. Describing the specific controls and the technical components of a security program and how those components fit together to meet control objectives. 

#### NIST Cybersecurity Framework

- Provides a common language for cybersecurity risk
- Helps identify and prioritize actions
- Aligns security actions across control types
- Offers different value to different organizations

https://www.nist.gov/cyberframework

**Reference architectures dive deeper into the <font color=red>how</font> of cybersecurity.**

![01_02_Reference](https://github.com/Jingy1Ma/CompTIA-Security-Exam-SY0-501/blob/main/Images/03_Architecture_and%20Design/01_02_Reference.PNG?raw=true)

**Frameworks and reference architectures represent the collective wisdom of the cybersecurity community.**



### 1.3 Developing security baselines

**Baseline security standards describe minimum requirements.**

#### Baseline Security: Standard Elements

- Administered by a named individual
- Protected against unauthorized access
- Doesn't jeopardize other systems or data
- Remains under positive control
- Complies with data security requirements

#### Baseline Are Generic

- They cover an uncertain future

**Baselines may include specific requirements for handling different categories of information.**

#### Specific Security Standards

- Operating systems
- Mobile devices
- Network infrastructure components
- Appliances

**System configuration managers automate policy deployment.**

#### Monitoring is Critical

- Watcher for baseline deviations



### 1.4 Leveraging industry standards

#### Sources of Security Standards

- Vendors
- Government agencies (e.g. NIST)
- Independent organizations (e.g. CIS)

**Industry standards provide an excellent starting point.**



### 1.5 Customizing security standards

**Scope and tailor standards to meet organization-specific requirements.**

For example, 

> Use strong encryption to protect stored data
>
> Encrypt disk using AES encryption with ~~128-bit, 192-bit,~~ 256-bit keys

an industry standard might suggest using full disc encryption to protect stored data on an endpoint and suggest the use of AES encryption with a 128, 192 or 256-bit key. The organization, however, might be under a more stringent compliance requirement that mandates the use of 256-bit keys and specifically prohibits the use of 128 or 192-bit keys. In this case the organization might use the benchmark standard but modify it to require the use of a 256-bit key, removing the options to use a 128 or 198-bit alternative. 

The easiest way to document these changes is to write a security standard that references another standard. For example,

> Windows Server 2012 R2 systems should be configured to the CIS Benchmark dated 4/28/2016, with the following exceptions...
>
> 1. Change Requirement: 1.1.2 to a 180-day password expiration
> 2. Change Requirement: 1.2.2 to a threshold of five logins

**Document the reasons for any deviations.**

**More stringent settings may be required based upon data sensitivity or system criticality.**



### 1.6 Defense in depth

**Defense in Depth** Organizations should use multiple, overlapping security controls to achieve each of their security objectives.

This is a layered approach to security and protects against the failure of any single security control. 

#### Defense in Depth: Eavesdropping

- Encryption through virtual private networks
- Encryption at the application layer
- Segmentation with VLANs

#### Defense in Depth: Access Control

- Network access control
- Role-appropriate VLANs (802.1x )
- MAC filtering
- Port security

#### Defense in Depth: Perimeter

![01_06_Perimeter](https://github.com/Jingy1Ma/CompTIA-Security-Exam-SY0-501/blob/main/Images/03_Architecture_and%20Design/01_06_Perimeter.PNG?raw=true)

#### ! EXAM TIPS

Keep the defense in depth principle front of mind during the Security+ exam!



### 1.7 Control diversity

**Diversity among our team members helps build stronger teams, with a wide range of experiences.**

#### Diversity in Cybersecurity

- Control type diversity
- Vendor diversity

#### Control Type Diversity

##### Technical

- Dat loss prevention
- Monitoring
- Content filtering

##### Administrative

- Background checks
- Nondisclosure agreements
- Training

##### Physical

- Security guards
- Random inspections
- Cameras

#### Vendor Diversity 

- Reduces susceptibility to vulnerabilities
- Using different firewall brands at different control points is an example of vendor diversity



![01_07_Vendor_Diversity](https://github.com/Jingy1Ma/CompTIA-Security-Exam-SY0-501/blob/main/Images/03_Architecture_and%20Design/01_07_Vendor_Diversity.PNG?raw=true)



### Chapter Quiz

1. Organizations often customize industry security standards to meet their specific security and business requirements.

   A. TRUE

   B. FALSE

2. Security baselines often require hundreds or thousands of individual security settings on a particular device.

   A. TRUE

   B. FALSE

3. The Payment Card Industry Data Security Standard (PCI DSS) is an example of what type of regulation?

   A. criminal law

   B. civil law

   C. administrative law

   D. private regulation

4. What U.S. federal government agency publishes security standards that are widely used throughout the government and private industry?

   A. FTC

   B. NIST

   C. CIA

   D. FCC

5. Which of the following controls would not constitute defense-in-depth for network access control?

   A. IDS

   B. 802.1x

   C. MAC filtering

   D. NAC





Answers:

1. TRUE
2. <font color=red>TRUE</font>
3. private regulation
4. NIST
5. <font color=red>IDS</font>



## 2. User Training

### 2.1 Security Education

##### Security Training

- Provides users with the knowledge that need to protect the organization's security

##### Security Awareness

- Keeps the lessons learned during security training top of mind for employees

#### Security Training Methods

- Instruction in on-site classes
- Integration with orientations
- Education through online providers
- Participation in vendor provided classroom training

**Customize training based upon user roles**

#### Training Frequency

- Initial training for new employees
- Update training for employees with new roles
- Refresher training on an annual basis
- Awareness efforts throughout the year

**Review training materials regularly to ensure relevance.**



### 2.2 Information classification

**Data Classification Policies** Assign information into categories, known as classifications, that determine storage, handling, and access requirements

#### Assign Classifications Based Upon

- Sensitivity of information
- Criticality of information

Classification schemes vary but all basically try to group information into high, medium and low sensitivity levels and differentiate between public and private information. 

#### Classification Levels

| Military Classification | Business Classification |
| ----------------------- | ----------------------- |
| Top Secret              | Highly Sensitive        |
| Secret                  | Sensitive               |
| Confidential            | Internal                |
| Unclassified            | Public                  |

**Classification guides other security decisions.**

For example a company might require the use of strong encryption to protect sensitive and highly sensitive information. Both at rest and in motion.

#### Labeling Requirements

- Identify sensitive information

**Securely dispose of information when no longer needed.**

These include software applications such as Darik's Boot and Nuke otherwise known as DBAN and hardware tools such as magnetic degaussers and device shredders. 

Information classification gives employees a consistent way to identify, label, handle and dispose of sensitive information.



### 2.3 Compliance training

**Compliance Programs** Ensure that an organization's information security controls are consistent with the laws, regulations, and standards that govern the organization's activities

**Include compliance obligations in security training**

#### Compliance Obligations

- Laws (GLBA, Gramm-Leach-Bliley Act)
- Regulations (HIPAA)
-  Standards (PCIDSS, Payment Card Industry Data Security Standard)

Standards are detailed technical specifications for security and other controls. 

**Begin compliance efforts with a gap analysis.**



### 2.4 User habits

- Include secure password practices in security education programs
- Clean desk policies and other data handling practices boost security
- Physical security training should include discussions of the dangers of tailgating
- Include BYOD policies in security training efforts
- Cover appropriate use of social media and peer-to-peer networks in security education



### 2.5 User-based threats

- Phishing uses spoofed messages to obtain information and convince users to perform risky actions
- Social engineering isn't limited to email. It can occur over the phone or in person as well
- New threats arise *every day*



### 2.6 Measuring security education

#### Simulated Phishing

- Directly measures user awareness

#### Security Awareness Surveys

- How well does the organization prepare you to deal with security threats
- Do you know your information security responsibilities?
- Do you know where to report a security incident?

**Measure how awareness changes over time**

**Change tactics based upon survey results**



### Chapter Quiz

1. Which one of the following is not an example of security education?

   A. online education

   B. classroom instruction

   C. briefings at team meetings

   D. reminder posters in the hallway

2. Which one of the following is the lowest level of classification in the government's classification scheme?

   A. secret

   B. confidential

   C. public

   D. top secret

3. Which one of the following regulatory schemes applies to healthcare providers in the United States?

   A. GLBA

   B. HIPAA

   C. PCI DSS

   D. FERPA

4. What is the name of the practice where a user holds a door open for the individual following them into a building?

   A. should surfing

   B. smurfing

   C. tailgating

   D. politeness

5. What type of social engineering attack targets end users via email messages?

   A. shoulder surfing

   B. vishing

   C. phishing

   D. pharming





Answers:

1. <font color=red>reminder posters in the hallway</font>
2. <font color=red>confidential</font>
3. HIPAA
4. tailgating
5. phishing



## 3. Secure Network Design

### 3.1 Security Zones

#### Network Border Firewall

- Internet Zone
- Intranet Zone
- DMZ Zone

![03_01_Firewall](https://github.com/Jingy1Ma/CompTIA-Security-Exam-SY0-501/blob/main/Images/03_Architecture_and%20Design/03_01_Firewall.PNG?raw=true)

#### Extranets

- Intranet segments extended to business partners

#### Honey nets

- Decoy networks designed to attract attackers

#### Ad Hoc Networks

- Temporary networks that may bypass security controls

Ad hoc networks may present a security risk especially if they are inter connected with other networks that lack strong security controls. For example, an employee who sets up a wireless point without using encryption and then connects it to the intranet, may inadvertently expose sensitive information to eavesdropping and create a potential path for an attacker to enter the organizations network. 



### 3.2 Public and private addressing

#### Public IP Addresses

- Assigned by a central authority and are routable over the Internet
- **I**nternet **C**orporation for **A**ssigned **N**ames and **N**umbers (ICANN)
- ICANN distributes large blocks of addresses to regional authorities for distribution
  - ARIN: US and Canada
  - LACNIC: Latin American and Caribbean regions
  - AfriNIC: Africa
  - RIPE NCC: Europe, West Asia, and the former USSR
  - APNIC: Asia-Pacific

##### IP Addresses Scarce

- No large blocks available

There are no large blocks of IPv4 addresses available for assignment today, and the only way to get these public IP addresses is by purchasing or renting them from other organizations, such as ISP.

##### Historic Free Use of Public IPs

![03_03_Historic_Use](https://github.com/Jingy1Ma/CompTIA-Security-Exam-SY0-501/blob/main/Images/03_Architecture_and%20Design/03_02_Historic_Use.PNG?raw=true)

- IPv4 allows for 4.3 billion possible addresses
- But there are currently at least 7.5 billion mobile devices in the world (not including include servers, desktop computers, network appliances, or any non-mobile devices)

#### Private IP Addresses

- Available for anyone's use but not routable over the Internet

##### Private IP Address Ranges

- 10.0.0.1-10.255.255.255
- 172.16.0.1-172.31.255.255
- 192.168.0.1-192.168.255.255

**Private IP Addresses Are not Internet Routable!**

#### Organizations Mix

- Public and private addresses

They use private addresses broadly within their private networks, assigning them to all of their internal systems. They then use a small number of public IP addresses for systems that require public access.

![03_02_Private_IP](https://github.com/Jingy1Ma/CompTIA-Security-Exam-SY0-501/blob/main/Images/03_Architecture_and%20Design/03_02_Private_IP.PNG?raw=true)

Systems that have private IP addresses cannot communicate on the internet using those addresses because they are not internet routable. Thousands of organizations around the world use those same private addresses on their own internal networks, so remote systems would have no way of telling where reply traffic should actually go. 

#### Network Address Translation

- Translates private IP addresses

![03_02_NAT](https://github.com/Jingy1Ma/CompTIA-Security-Exam-SY0-501/blob/main/Images/03_Architecture_and%20Design/03_02_NAT.PNG?raw=true)

#### NAT AND Security

- Hides internal addresses from Internet systems
- Limit direct access to systems
- Makes it difficult to identify the true origin of traffic

For this reason, most organizations maintain logs of their NAT translations that allow them to determine who was using a particular public IP address at any given time.

**NAT requires a large pool of public IP addresses.**

Since most organizations have a limited pool of public addresses, they can quickly run into a situation where that pool is exhausted and no new systems can communicate on the internet. 

#### Port Address Translation (PAT)

- Allows multiple systems to share the same public address
- Assigns unique ports to each communication

Instead of recording translations between IP addresses, PAT assigns each connection a different port on a public IP address. This way, many different systems can share the same public IP address at any point in time.



### 3.3 Subnetting

**Subnetting** Subdivides large networks

#### Subnets

![03_03_Subnet](https://github.com/Jingy1Ma/CompTIA-Security-Exam-SY0-501/blob/main/Images/03_Architecture_and%20Design/03_03_Subnet.PNG?raw=true)

Network Address | Host Address

192.168|1.100 -> single network with over 165,000 possible host addresses

192.168.1 | 100 -> 256 possible subnetworks with 254 possible hosts each

![03_03_Subnet2](https://github.com/Jingy1Ma/CompTIA-Security-Exam-SY0-501/blob/main/Images/03_Architecture_and%20Design/03_03_Subnet2.PNG?raw=true)

![03_03_Subnet3](C:\Users\JY\Desktop\Security+\Images\03_Architecture_and Design\03_03_Subnet3.PNG)

On our network diagram, we can now give the accounting group, the 192 168.1 address space, the sales group, the 192 168.2 subnetwork, and then assign the 192 168.3 subnetwork to the IT group, leaving the remaining 253 subnets for future uses. Each of those subnetworks can have up to 254 systems connected to it. 

#### Subnet Masks

- Identify the dividing line between network and host addresses

![03_03_Subnet_Mask](https://github.com/Jingy1Ma/CompTIA-Security-Exam-SY0-501/blob/main/Images/03_Architecture_and%20Design/03_03_Subnet_Mask.PNG?raw=true)

##### Subnet Mask Notion

- IP addresses: 192.168.1.100
- Subnet mask: 255.255.255.0

##### Slash Notation

- 192.168.1.0/24



### 3.4 VLANs and network segmentation

#### Virtual LANs

- Separate systems on a network into logical groups based upon function, regardless of physical location

![03_04_VLAN](https://github.com/Jingy1Ma/CompTIA-Security-Exam-SY0-501/blob/main/Images/03_Architecture_and%20Design/03_04_VLAN.PNG?raw=true)

When users from different departments are mingled together and those departments are spread across multiple buildings. That's where virtual LANs come into play. We can use them to connect people who are on different parts of the network to each other and also to separate them from other users who might actually be geographically close to them. 

**VLANs extend the broadcast domain.**

This means that users on the same VLAN will be able to directly contact each other as if they were connected to the same switch. All of this happens at layer two of the network stack without involving routers or firewalls. 

#### Configuring VLANs

- Enable VLAN trunking (This allows switches in different locations on the network to carry the same VLANs)
- Assign switchports to VLANS



### 3.5 Security device placement

#### Network Border Firewall

![03_05_Border_Firewall](https://github.com/Jingy1Ma/CompTIA-Security-Exam-SY0-501/blob/main/Images/03_Architecture_and%20Design/03_05_Border_Firewall.PNG?raw=true)

In this example the firewall sits at the network border, separating an internal network and the DMZ from the internet. There could easily be additional firewalls on the internal network. 

![03_05_Additional_Firewall](https://github.com/Jingy1Ma/CompTIA-Security-Exam-SY0-501/blob/main/Images/03_Architecture_and%20Design/03_05_Additional_Firewall.PNG?raw=true)



For example we might place a firewall here to enforce separation between the endpoint network, wireless network, guest network, and data center network. 

#### Network Traffic Collectors

- Intrusion detection and prevention sensors
- Network taps
- Port mirrors

##### Sensor Placement

For example if you place an intrusion detection system sensor in the DMZ, it will be unable to collect traffic that exists only on the internal network. 

If you place a sensor on the internal network, it won't be able to see traffic that passes between systems on the internet and those in the DMZ.

If you place a sensor outside the firewall on the internet, it won't see traffic between internal systems. 

So if you want full coverage of the networks connected to this firewall, you'd need to put sensors on all three networks. As you design network sensors, you'll need to understand your organizations network design. For example here's a common.

**Aggregation (or distribution) switches connect downstream access switches to each other.**

![03_05_Aggregation_Switch](https://github.com/Jingy1Ma/CompTIA-Security-Exam-SY0-501/blob/main/Images/03_Architecture_and%20Design/03_05_Aggregation_Switch.PNG?raw=true)

Here's a common design that uses an aggregation switch to pull together network traffic from the access switches that are deeper in the network, and those are the ones that are actually connected to user devices. 

Span ports on switches provide a copy of all traffic that crosses the switch, and these are very useful for many security applications. However depending upon your design, you may not see the traffic that you would expect. For example, if you place a span port on this switch, you will only see traffic to, from or between any of the systems on that switch. That probably makes sense. However, if you place a span port on the aggregation switch, you won't necessarily see all of the traffic from the four switches beneath it. If two systems connected to the same switch communicate with each other, the edge switch at the access layer handles that traffic without passing it up to the aggregation switch. 

#### Security Information and Event Management

- Gather information using collectors
- Analyze information with a centralized correlation engine
- Place collectors near the systems generating records
- Place the correlation engine in a secure location

**Proxy servers and content filters typically belong in the DMZ.**

The location of these systems may vary depending upon your specific architectural design, but it's often good practice to place them in the DMZ network. This is especially true for proxy servers, because they have to initiate connections to the outside world. Using a DMZ based proxy limits the amount of outbound network traffic from the internal network, placing an added layer of isolation around that sensitive network. 

#### VPN Concentrators

- Aggregate remote user connections
- Often reside in their own VLAN, where access controls may restrict remote user activity
- Sophisticated designs may use multiple VLANs for different user roles

#### SSL Accelerators

- Handle the difficult cryptographic  work of setting up TLS connections

#### Load Balancers

- Distribute connection requests among multiple servers

**SSL accelerators and load balancers belong in the DMZ.**

#### DDoS Mitigation Tools

- Belong as close to the internet as possible

**Purchasing DDoS mitigation services from your ISP is an ideal approach.**

So that the attacks can be blocked before they even reach your network. 



### 3.6 Software-defined networking (SDN)

**Reconfiguring traditional networks requires reconfiguring devices.**

#### Network Functions

##### 1 Control Plane

- Responsible for making routing and switching decisions

##### 2 Data plane

- Responsible for carrying out the instructions of the control plane

**SDN separates the control plane from the data plane.**

Instead of each router and switch making independent decisions about how to route packets, these decisions come from an SDN controller. The SDN controller is where network administrators and algorithms make decisions about network routing, and then the controller reaches out to each device on the network and programs it to carry out those instructions properly. 

The SDN controller implements the control plane of the network, while the routers and switches accept instructions from that control plane to carry out the data plane function. 

**SDN makes the network programmable.**

#### SDN Security Benefits

- Allows granular network configuration

In many organizations, network administrators typically balk at routing VLANs across networks of different buildings because of the difficulty of configuring those VLANs. However, with SDN, this becomes quite easy, and allows the use of strong network-segmentation practices. 

- Facilitates faster response to security incidents

For example, if the network comes under a DoS attack from a misconfigured host, security tools can automatically reach out, and disable the network switch port belonging to that host, and place the host in a quarantine zone, where it has very limited network access. 

**SDN increases network complexity.**

It requires the use of strong access controls. You wouldn't want a malicious individual gaining access to your network control plane and using SDN to conduct eavesdropping or impersonation attacks.



#### 3.7 Port isolation

Particularly useful when users of the network do not trust each other and are not trusted themselves. 

#### ! EXAM TIPS

Port isolation and private VLANs are the same thing.

**Port isolation restricts traffic from a source port to a single destination port.**

#### Why User Port Isolation

- Prevents devices on the same switch from communicating with each other
- Blocks data-link-layer attacks, such as ARP spoofing

**Port isolation typically isn't effective on a corporate network.**

**Port isolation works very well on hotel guest room networks.**



### Chapter Quiz

1. Which one of the following is a public IP address?

   A. 172.18.144.144

   B. 10.194.99.16

   C. 142.19.15.4

   D. 192.168.14.129

2. How would a network technician write the subnet mask 255.255.0.0 in slash notation?

   A. /32

   B. /24

   C. /16

   D. /8

3. Which one of the following devices carries VLANs on a network?

   A. hub

   B. switch

   C. router

   D. firewall



Answers:

1. <font color=red>142.19.15.4</font>

2. /16

3. switch

   

## Reference

[1] https://www.linkedin.com/learning/comptia-security-plus-sy0-501-cert-prep-3-architecture-and-design/
