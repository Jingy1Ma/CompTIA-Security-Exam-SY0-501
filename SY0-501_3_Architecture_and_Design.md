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



## Reference

[1] https://www.linkedin.com/learning/comptia-security-plus-sy0-501-cert-prep-3-architecture-and-design/