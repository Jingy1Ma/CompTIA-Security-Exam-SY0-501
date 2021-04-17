# CompTIA Security+ Exam (SY0-501): Risk Management

We'll be focusing on 

- explaining the importance of policies, plans, and procedures related to organizational security
- summarizing business impact analysis concepts
- explaining risk management processes and concepts
- following incident response procedures
- summarizing the basic concepts of forensics
- explaining disaster recovery and continuity of operation concepts
- comparing and contrasting various types of security controls
- carrying out data security and privacy practices



## 1. Controls and Risks

### 1.1 Security Controls

#### Security Controls

- Security Controls are the procedures and mechanisms that an organization puts in place to manage security risks

#### Defense in Depth

- Multiple controls for one objective

#### Categorizing Controls by Purpose

- Deterrent controls: Designed to discourage attack attempts
- Detective controls: Designed to identify attack attempts (e.g. IDS)
- Preventive controls: Designed to stop attacks that are in progress
- Corrective controls: Designed to help an organization to recover from an incident (e.g. backup)

#### Categorizing Controls by Mechanism

- Technical controls: Use technology to achieve security control objectives
- Administrative controls: Management processes that we put in place to improve enterprise security
- Physical controls: Deter, detect, or prevent unauthorized physical access to a facility

You might find yourself facing a control requirement that seems impossible to meet. For example, your organization might have a security requirement that you use only current versions of operating systems, but you might also have a business requirement to use a critical software product that requires the use of an outdated operating system. In those cases, you might meet both requirements by deploying a compensating control.

#### Compensating Controls

- Fill gaps left when you are unable to implement other required controls

#### False Positive Errors

- Occur when a control inadvertently triggers when it should not

They're dangerous because they reduce the confidence that security administrators have in the control, and sometimes lead to administrators ignoring future alerts from that system. 

#### False Negative Errors

- Occur when a control fails to trigger in a situation when it should



### 1.2 Security Policy Framework

- Policies
- Standards
- Guidelines
- Procedures

#### Security Policies

- Provide the foundation for a security program
- Are written carefully over a long period of time
- Require compliance from all employees
- Are approved at the highest levels of the organization

##### Too Specific

> Encrypt sensitive information with AES-256

> Store employee records in Room 226

##### Right Level

> Encrypt sensitive data in transit and at rest

> Store employee records in HR-approved locations

#### Security Standards

- Provide specific details of security controls
- Derive their authority from policies
- Follow a less rigorous approval process
- Require compliance from all employees

When it comes to complex configuration standards, organizations often draw up industry sources such as the standards available from the Center for Internet Security. These standards standards provide detailed configuration settings for a wide variety of operating systems, network devices, application platforms, and other components of the IT infrastructure. They provide a great starting point for an organization's security standards.

#### Security Guidelines

- Provide security advice to the organization
- Follow best practices from industry
- Suggest optional practices; not mandatory

#### Security Procedures

- Outline a step-by-step process for an activity
- May require compliance, depending upon the circumstances 

#### ! EXAM TIPS

Policies and standards are mandatory. Guidelines are optional. Procedures can go either way.



### 1.3 Security Policies

#### Factors Affecting Security Policy

- Culture of the organization
- Industry
- Regulatory environment

#### Common Policies

- Information security policy
- Privacy policy
- Acceptable use policy

##### Information Security Policy

- Designation of individual responsible for security
- Description of security roles and responsibilities
- Authority for creation of security standards
- Authority for incident response
- Process for policy exceptions and violations

##### Privacy policy

The organization should also have a published privacy policy that covers the ways that the organization collects, stores, and shares information about individuals. 

##### Acceptable use policy

- Also known as responsible use policy
- Describes how individuals may use information systems
- Prohibits illegal activity
- Describes what personal use is permitted

#### Least Privilege

- Assign users only the minimum set of permissions necessary for their jobs

#### Separation of Duties

- Prevents users from simultaneously holding two conflicting permissions

#### Mandatory Vacation

- Force privileged users to take one or two weeks of consecutive vacation annually

#### Job Rotation

- Rotate users in and out of positions with sensitive responsibilities



### 1.4 Risk Assessment

Addressing each one of risks takes both time and money, therefore, information security professionals need to prioritize their risk lists in order to spend these precious resources where they will have the greatest security effect. 

#### Risk Assessment

- Identifies and prioritizes risks

based upon the likelihood of their occurrence and the expected impact they will have on the organization's operations.

#### Key Terms

- Threats
- Risks
- Vulnerabilities

#### Threat

- External force jeopardizing security

Threats might be naturally occurring, such as hurricanes and wildfires, or manmade, such as hacking and terrorism. **You can't normally control what threats are out there, they exist independently**. There is one related term that you should know for the exam. 

#### ! EXAM TIPS

Threat vectors are the specific methods that threats use to exploit a vulnerabilities.

(This might be a hacker toolkit, social engineering, physical intrusion, or any of a number of other hacking techniques.)

#### Vulnerability

- Weaknesses in security controls

that a threat might exploit to undermine the confidentiality, integrity, or availability of your information or systems. These might include missing patches, promiscuous firewall rules, or other security misconfigurations. **You do have control over the vulnerabilities in your environment** and security professionals spend much of their time hunting down and remediating vulnerabilities. 

#### Risk

- The combination of a vulnerability and a corresponding threat

![01_04_Risk](https://github.com/Jingy1Ma/CompTIA-Security-Exam-SY0-501/blob/main/Images/05_Risk_Management/01_04_Risk.PNG?raw=true)

For example, if you haven't update your antivirus signatures recently and hackers release a new virus on the internet, you face a risk. You are vulnerable because you're missing a security control and there is a threat, the new virus. 

There is no risk if either the threat or vulnerability factor is missing. For example, if you live in an area far from the coast, it doesn't matter if your building is vulnerable to hurricanes because there's no threat of a hurricane in your region. Similarly, if you store your backup tapes in a fire-proof box, there is no risk from a building fire because your storage container is not vulnerable to fire.

**Never conduct penetration testing or vulnerability testing without authorization!**

#### Prioritize Risks

- Likelihood: Probability that a risk will occur
- Impact: Amount of expected damage

#### Qualitative Risk Assessment

- Uses subjective ratings to evaluate risk likelihood and impact (e.g. low, medium, high)

![01_04_Qualitative_Risk_Assessment](https://github.com/Jingy1Ma/CompTIA-Security-Exam-SY0-501/blob/main/Images/05_Risk_Management/01_04_Qualitative_Risk_Assessment.PNG?raw=true)

#### Quantitative Risk Assessment

- Uses objective numeric ratings to evaluate risk likelihood and impact (usually in terms of dollars)



### 1.5 Quantitative Risk Assessment

**Perform quantitative risk assessment for a single risk and asset pair. **

#### Asset Value (AV)

- The dollar value of an asset

##### Asset Valuation Techniques

- Original cost
- Depreciated cost
- Replacement cost

#### Exposure Factor (EF)

- Expected % of damage to an asset

#### Single-Loss Expectancy

- Expected dollar loss if a risk occurs one time
- AV * EF = SLE
  - \$20M * 50% = ​\$10M

#### Annualized Rate of Occurrence (ARO)

- Number of times a risk is expected to occur each year

#### Annualized Loss Expectancy (ALE)

- Expected dollar loss from a risk in any given year
- SLE * ARO = ALE
  - \$10 * 0.01 = \$100,000

It is important to remember that in reality this cost won't occur each year. What will really have happened is \$10 million in damage each time a flood occurs but since we expect that to happen only once every 100 years, it averages out to ​\$100,000 a year. 

#### ! EXAM TIPS

Be prepared to work through a quantitative risk assessment calculation on the exam!

**Time to restore service depends upon whether a component is repairable.**

#### Mean Time To Failure (MTTF)

- Average time a **nonrepairable** component will last

When using mean values, it's important to remember that these are averages. Half of the assets of this type will fail before the MTTF and half will last longer than the average value. Mean values are useful for planning purposes but you shouldn't completely depend upon them. 

#### Mean Time Between Failures (MTBF)

- Average time gap between failures of a **repairable** component

#### Mean Time To Repair (MTTR)

- Average time required to return a **repairable** component to service

When we look at the MTTF, and MTTR values together, we can get a good idea of the expected downtime for an IT service or a component.



### 1.6 Risk Management

**Risk Management** This is a process of systematically analyzing potential responses to each risk and implementing strategies to control those risks appropriately.

#### Risk Management Strategies

- Risk avoidance: Changes the organization's business practices
  - e.g. Avoid the risk of a flood by relocating the data center
- Risk transference: Shifts the impact of a risk to another organization
  - e.g. Transfer the risk of a flood by purchasing flood insurance
  - insurance policy (cyber liability insurance)
  - you can't always transfer risk completely
- Risk mitigation: Reduces the likelihood or impact of the risk
  - e.g. Mitigate the risk of a flood by installing flood control measures
- Risk acceptance: Accepts the risk without taking further action
  - e.g. Accepting the risk would continue operations as is in a data center despite the flooding risk
- Risk deterrence: Takes actions that dissuade a threat from exploiting a vulnerability
  - Deter the risk of burglary with dangerous-looing fences and guard dogs!

#### ! EXAM TIPS

Outside the exam environment, most consider risk deterrence as an example of risk mitigation.



### 1.7 Risk Visibility and Reporting

Risk visibility and reporting techniques ensure that the results of these risk management processes are clearly documented and tracked over time.

#### Risk Register

- Tracks risk information

#### Risk Register Contents

- Description
- Category
- Probability and impact
- Risk rating
- Risk management actions

#### Risk Register Information Sources

- Risk assessment results
- Audit findings
- Team member input
- Threat Intelligence: Shares risk information.

**Threat intelligence may be used both strategically and operationally.**



### Chapter Quiz

1. Which category of security control focuses on the processes that we put in place to manage technology in a secure manner?

   A. technical controls

   B. management controls

   C. administrative controls

   D. operational controls

2. Which element of the security policy framework includes suggestions that are not mandatory?

   A. policies

   B. guidelines

   C. standards

   D. procedures

3. What security principle prevents against an individual having excess security rights?

   A. separation of duties

   B. mandatory vacations

   C. job rotation

   D. least privilege

4. What two factors are used to evaluate a risk?

   A. frequency and likelihood

   B. criticality and likelihood

   C. impact and criticality

   D. likelihood and impact

5. What is the correct formula for computing the annualized loss expectancy?

   A. ALE = EF * SLE * ARO

   B. ALE = AV - SLE

   C. ALE = ARO * AV

   D. ALE = SLE * ARO

6. Purchasing an insurance policy is an example of which risk management strategy?

   A. risk acceptance

   B. risk mitigation

   C. risk transference

   D. risk deterrence



Answers:

1. <font color=red>operational controls?</font>

   The classes identified by NIST are:

   - Technical - the control is implemented as a system (hardware, software, firmware). For example, firewalls, anti-virus software, and OS access control models.
   - Operational / administrative - the control is implement primarily by people rather than systems. For example, security guards and training programs are operational controls.
   - Management - the control gives oversight of the information system. Examples could include risk identification or a tool allowing the evaluation and selection of other security controls. 

2. guidelines

3. least privilege

4. likelihood and impact

5. ALE = SLE * ARO

6. risk transference



## 2. Supply Chain Risk

### 2.1 Managing Vendor Relationships

**Ensure that vendor security policies are *at least as* stringent as your own**

#### Vendor Management Life Cycle

```mermaid
graph LR
A[Vendor Selection] --> B[Onboarding]
B[Onboarding] --> C[Monitoring]
C[Monitoring] --> D[Offboarding]
D[Offboarding] --> A[Vendor Selection]
```

##### Vendor Selection

- May use a formal RFP
- May be an informal process
- Should include security requirements
- Should evaluate security

##### Onboarding

- Verify contract details
- Arrange secure data transfer
- Establish incident procedures

##### Monitoring

- Conduct site visits
- Review independent audits
- Handle security incidents

##### Offboarding

- Destroys confidential information
- Unwinds a business relationship
- May restart the life cycle



### 2.2 Vendor Agreements

#### Service-Level Requirement (SLR)

- Document specific requirements that a customer has about any aspect of a vendor's service performance

##### Examples of SLRs

- System response time 
- Service availability
- Data preservation

**Document SLRs in a service-level agreement (SLA)**

#### Other Agreement Types

- Memorandum of understanding (MOU, a.k.a MOA)
- Business partnership agreement (BPA)
- Interconnection security agreement (ISA)

MOUs are commonly used when a legal dispute is unlikely but the customer and vendor still wish to document their relationship to avoid future misunderstandings. MOUs are commonly used in cases where an internal service provider is offering a service to a customer that is in a different business unit of the same company.

**Include security requirements in SLRs, SLAs, and other agreements.**

#### Security and Compliance Terms

- Document security and compliance requirements
- Facilitate customer monitoring of compliance
- Ensure the right of audit and assessment



### 2.3 Vendor Information Management

**Agreements should contain clear data ownership language.**

#### Data ownership Provisions

- Customer retains uninhibited data ownership
- Vendor's right to use information is limited to activities performed on behalf of the customer
- Vendor's right to use information is limited to activities performed with the customer's knowledge
- Vendor must delete information at the end of the contract

**Agreements should limit data sharing with third parties.**

**Agreement should include data protection provisions.**



### Chapter Quiz

1. Vendors extend your organization's technology environment. If they handle data on your behalf, you should expect they execute the same degree of care that you would in your own operations.

   A. TRUE

   B. FALSE

2. What type of agreement is used to define availability requirements for an IT service that an organization is purchasing from a vendor?

   A. SLA

   B. MOU

   C. ISA

   D. BPA



Answer:

1. TRUE
2. SLA



## 3. Personnel Management

### 3.1 Need to Know and Least Privilege

#### Need to Know

- Limits information access

This need-to-know principle is commonly followed in military and government circles that handle classified information. 

#### Least Privilege

- Limits system permissions
- Implementing least privilege can be cumbersome

**Emergency access procedures reduce the business impact.**

#### Privilege Aggregation (Privilege Creep)

- Jeopardizes least privilege

IT staff who remain in an organization for a long time, with a variety of different positions, may accumulate privileges over time that, in aggregate, violate the least privilege principle. **User account reviews** are a good control against privilege creep. The principles of need-to-know and least privilege form the core foundation of cyber security programs.



### 3.2 Separation of Duties and Responsibilities

#### Separation of Duties

- No individual should possess two permissions that, in combination, allow them to perform a highly sensitive action.
- Accounting groups often separate the responsibilities of creating new vendors and issuing payments
- Information security professionals are often called on to implement separation of duties
- IT teams often separate the privileges of writing code and deploying code into production

#### Two-Person (Dual) Control

- Requires the authorization of two separate individuals to carry out a sensitive action; also known as dual control
- Missile launch facilities implement the concept of two-person control.
- Checks that require two signatures are an example of two-person control
- IT teams commonly use two-person control for sensitive tasks



### 3.3 Security in the Hiring Process

**Employees pose a significant threat to enterprise security, known as the "insider threat."**

**Preemployment screening checks the background of potential employees.**

#### Preemployment Screening

- Criminal records check
- Sex offender registry
- Reference checks
- Education and employment verification
- Credit checks

#### Employment Agreements

- Should include nondisclosure agreements (NDAs)
- Should discuss return of information and physical assets at termination

#### Include Security Policies in Orientation Sessions



### 3.4 Employee Termination Process

- Every employee eventually leaves the organization.
- Exit interview provide a chance to debrief departing employees.
- Use exit interviews to remind employees of their NDA
- Revoke access promptly, but not prematurely

#### Retrieve Organization Property

- Keys
- Access badges
- Laptops and mobile devices
- Paper and electronic files



### Chapter Quiz

1. What security principle most directly applies to limiting information access?

   A. least privilege

   B. two person control

   C. separation of duties

   D. need to know

2. What security principle requires two individuals to perform a sensitive action?

   A. separation of duties

   B. least privilege

   C. two person control

   D. need to know

3. Which one of the following agreements is most directly designed to protect confidential information after an employee has left the organization?

   A. SLA

   B. BAA

   C. NDA

   D. Asset return



Answers:

1. need to know
2. two person control
3. NDA



## 4. Awareness and Training

### 4.1 Security Education

#### Security Training

- Provides users with the knowledge they need to protect the organization's security

#### Security Awareness

- Keeps the lessons learned during security training

#### Security Training Methods

- Instruction in on-site classes
- Integration with orientations
- Education through online providers
- Participation in vendor-provided classroom training

**Customize training based upon user roles.**

For example, employees handling credit card information should receive training on PCI DSS requirements. Human resources team members should be trained on handling personally identifiable information or PII. IT staff need specialized skills to implement security controls. 

#### Role-Based Training

- Data and system owners
- System administrators and other privileged users
- Normal users
- Executives

#### Training Frequency

- Initial training for new employees
- Update training for employees with new roles
- Refresher training on an annual basis
- Awareness efforts throughout the year

**Review training materials regularly to ensure relevance.**

#### Continuing Education

- Reminds employees of security responsibilities



### 4.2 Information Classification

#### Data Classification Policies

- Assign information into categories, known as classifications, that determines storage, handling and access requirements

#### Assign Classifications Based Upon

- Sensitivity of information
- Criticality of information

Classification schemes vary, but all basically try to group information into high, medium, and low sensitivity levels and differentiate between public and private information. 

#### Classification Levels

| Military Classification | Business Classification |
| ----------------------- | ----------------------- |
| Top Secret              | Highly Sensitive        |
| Secret                  | Sensitive               |
| Confidential            | Internal                |
| Unclassified            | Public                  |

**Classification guides other security decisions.**

#### Labeling Requirements

- Identify sensitive information

**Securely dispose of information when no longer needed.**

e.g. software: Darik's Boot and Nuke (DBAN); hardware: magnetic degaussers, device shredders



### 4.3 Compliance Training

#### Compliance Programs

- Ensure that an organization's information security controls are consistent with the laws, regulations, and standards that govern the organization's activities
- Include compliance obligations in security training

#### Compliance Obligations

- Laws
  - Requirements passed by a government authority at the national or local level
  - e.g. Graham-Leech-Bliley Act, or GLBA, affects security practices of financial institutions. 
- Regulations
  - Mandatory requirements but are not embodied in law
  - e.g. HIPAA (Health Insurance Portability and Accountability Act) rules
- Standards
  - Detailed technical specifications
  - PCIDSS (Payment Card Industry Data Security Standard)

**Begin compliance efforts with a gap analysis.**



### 4.4 User Habits

- Include secure password practices in security education programs.
- Clean desk policies and other data handling practices boost security.
- Physical security training should include discussions of the dangers of tailgating.
- Include BYOD policies in security training efforts.
- Cover appropriate use of social media and peer-to-peer networks in security education.
- Security training should cover acceptable uses of corporate IT resources and the consequences of policy violations.



### 4.5 User-based Threats

- Phishing uses spoofed messages to obtain information and convince users to perform risky actions.
- Social engineering isn't limited to email. It can occur over the phone or in person as well.
- New threats arise *every day*.



### 4.6 Measuring Security Education

#### Simulated Phishing

- Directly measures user awareness

#### Security Awareness Surveys

- How well do the organization prepare you to deal with security threats?
- Do you know your information security responsibilities?
- Do you know where to report a security incident?

**Measure how awareness changes over time.**

**Change tactics based upon survey results.**



### Chapter Quiz

1. Which one of the following is not an example of security education?

   A. briefings at team meetings

   B. reminder posters in the hallway

   C. online education

   D. classroom instruction

2. Which one of the following is the lowest level of classification in the government's classification scheme?

   A. Public

   B. Top Secret

   C. Secret

   D. Confidential

3. Which one of the following regulatory schemes applies to healthcare providers in the United States?

   A. GLBA

   B. FERPA

   C. PCI DSS

   D. HIPAA

4. What is the name of the practice where a user holds a door open for the individual following them into a building?

   A. smurfing

   B. politeness

   C. shoulder surfing

   D. tailgating

5. What type of social engineering attack targets end users via email messages?

   A. phishing

   B. pharming

   C. vishing

   D. shoulder surfing



Answers:

1. **reminder posters in the hallway** (security awareness)
2. Confidential
3. HIPAA
4. tailgating
5. phishing



## 5. Business Continuity and Disaster Recovery

### 5.1 Business Continuity Planning

#### Business Continuity Planning

- A set of controls designed to keep a business running in the face of adversity, whether natural or man-made

Business continuity is a core security concept because it is the primary control that supports the security objective of **availability**. 

#### Defining BCP Scope

- Business actives
- Systems
- Controls

#### Business Impact Assessment (BIA)

- Identifies and prioritizes risks

#### Risk Assessment Factors

- Impact on life and safety
- Impact on property and finances
- Impact on reputation

**Risk assessments should include environmental and man-made threats from internal and external sources.**

#### BIA Results

| Risk                            | Annualized Loss Expectancy (ALE) |
| ------------------------------- | -------------------------------- |
| Hurricane damage to data center | \$145,000                        |
| Fire in data center             | \$18,000                         |
| Power outage                    | \$12,000                         |
| Theft of equipment              | \$3,400                          |

It makes sense to place the highest priority on addressing the risk at the top of the list, hurricane damage to the data center. But the organization must then make decisions about control implementation that factor in cost. For example, if a $50,000 flood prevention system would reduce the risk of hurricane damage to the data center by 50%, purchasing the system is clearly a good decision because it has an expected payback period of less than one year.



### 5.2 Business Continuity Controls

**Redundancy protects against the failure of a single component.**

#### Single Point of Failure Analysis

- Identifies and removes SPOFs

##### Example

![05_02_SPOF](https://github.com/Jingy1Ma/CompTIA-Security-Exam-SY0-501/blob/main/Images/05_Risk_Management/05_02_SPOF.png?raw=true)

- A simple web server architecture has many single points of failure.

- **Clustering** address the single point of failure at the the web server.

- Address the single point of failure at the firewall through failover capability (a pair of **high-availability** firewalls)
- **Redundancy** addresses the single point of failure at the network

**SPOF analysis continues until the cost of addressing risks outweighs the benefits.**

#### IT Contingency Scenario Examples

- Sudden bankruptcy of a key vendor
- Insufficient storage or compute capacity
- Failure of utility service

**Remember to perform succession planning for staff as well!**



### 5.3 High Availability and Fault Tolerance

#### High Availability (HA)

- Uses multiple systems to protect against service failure

#### Fault Tolerance (FT)

- Makes a single system resilient against technical failures

#### Load Balancing

- Spreads demand across systems

While they use similar technologies, load balancing and high availability are different goals. Load balancing uses multiple systems in an attempt to spread the burden of providing a service across those systems providing a scalable computing environment. 

Most implementations of clustering and similar technologies are designed to achieve both high availability and load balancing but it is possible to have one without the other. 

#### Common Points of Failure

- Power supply
- Storage media

##### Power Supplies

- Contain moving parts
- Have high-failure rates
- Can be redundant
- May use multiple power sources

#### Redundant Array of Inexpensive Disks (RAID)

- Disk mirroring, RAID 1, stores the same data on two different disks
- Disk striping with parity, RAID 5, uses 3 or more disks to store data and parity information

![05_03_RAID](https://github.com/Jingy1Ma/CompTIA-Security-Exam-SY0-501/blob/main/Images/05_Risk_Management/05_03_RAID.png?raw=true)

#### ! EXAM TIPS

- Know that disk mirroring requires 2 disks while disk striping with parity requires 3
- RAID is a fault tolerance technique, not a backup strategy!

**Network Quality of Service (QoS) provides critical services with protected network capacity.**



### 5.4 Disaster Recovery

**Disaster Recovery** Disaster Recovery capabilities are designed to restore a business to normal operations as quickly as possible. Disaster Recovery is a subset of business continuity.

#### Initial Response

- Contain the damage caused by disaster
- Recover whatever capabilities may be immediately restored
- Include a variety of activities depending upon the nature of disaster

**Employee responsibilities will change dramatically during disaster recovery.**

#### Disaster Communications

- Initial activation of the disaster recovery team
- Regular status updates
- Tactical communications

**After the danger passes, the team shifts to assessment mode.**

#### Order of Restoration

- Should prioritize systems by criticality

#### Recovery Time Object (RTO)

- Maximum amount of time that it should take to recover a service after a disaster

#### Recovery Point Objective (RPO)

- Maximum time period from which data may be lost in the wake of a disaster

Together, the RTO and RPO provide valuable information to disaster recovery planners. 

**After developing a plan, responders restore services in an orderly fashion.**

#### ! EXAM TIPS

Disaster recovery efforts end only when the business is operating normally in its primary facility.

**Team members should receive regular training on their DR responsibilities.**



### 5.5 Backups

Backups are perhaps the most important component of any disaster recovery plan.

#### Backups

- Provide a data "safety net"

#### Backup Media

- Tape backups
- Disk-to-disk backups
- Cloud backups

#### Full Backups

- Include a complete copy of all data

#### Differential Backups

- Include all data modified since the last full backup

#### Incremental Backups

- Include all data modified since the last full backup or incremental backup

#### Snapshots

- Capture system state at a moment in time

#### ! EXAM TIPS

Understand what backups need to be restored in the event of a disaster

#### Scenario

Job performs full backups every Sunday evening and differential backups every weekday evening. His system fails on Friday morning. What backups does he restore?

1. Sunday's full backup
2. Thursday's differential backup

Job performs full backups every Sunday evening and **incremental** backups every weekday evening. His system fails on Friday morning. What backups does he restore?

1. Sunday's full backup
2. Monday, Tuesday, Wednesday, and Thursday incremental backups

(Incremental backups are smaller than differential backups.)

**Incremental backups use *less* space but require *greater recovery* time.**

#### Media Rotation Strategies

- Allow reuse of backup media

**Most restoration requests are for recent backups.**

#### Grandfather-Father-Son Rotation (GFS Approach)

| Son 1    | Son 2     | Son 3    | Son 4      |
| -------- | --------- | -------- | ---------- |
| MON 10/1 | TUES 10/2 | WED 10/3 | THURS 10/4 |

| Dad 1    | Dad 2     | Dad 3     | Dad 4     |
| -------- | --------- | --------- | --------- |
| FRI 10/5 | FRI 10/12 | FRI 10/19 | FRI 10/26 |

| GF 1      | GF 2      | GF 3      | GF 4    |
| --------- | --------- | --------- | ------- |
| WED 10/31 | WED 11/30 | WED 12/31 | WE 1/31 |

Once all of these sets have filled up, we're left in the situation where we can go back in time at different intervals. We can restore backups from any of the past five days, from Friday of the past four weeks, and from the last day of the past four months. We can do all of that with 12 sets of backup media. 

Alternatively, if we had retained every day's backup media from the past four months, we'd have somewhere around 120 sets of tapes. That's 10 times as expensive. 

Organizations can and do customize these schedules to meet their unique business needs. For example, one common twist on this grandfather-father-son approach is to use 12 grandfather sets, allowing the organization to restore data from the last day of any month within the past year.



### 5.6 Disaster Recovery site

**Disaster Recovery site** Provide alternate data processing

#### Disaster Recovery Facility Types

- Host site
- Cold site
- Warm site

##### Hot Sites

- Fully operational data centers
- Stocked with equipment and data
- Available at a moment's notice
- Very expensive

##### Cold Sites

- Empty data centers
- Stocked with core equipment, network, and environmental controls
- Relatively inexpensive
- Operational in weeks or months

##### Warm Sites

- Stocked with all necessary equipment and data
- Not maintained in a parallel fashion
- Similar in expense to hot sites
- Available in hours or days

**Store backups at an offsite location**

Backups may be physically transported to the disaster recovery site on a periodic basis, or they may be transferred digitally using a process known as electronic vaulting. 

**Alternate business processes add flexibility in the wake of a disaster.**

For example, the organization might move to a paper based ordering process, if an electronic order management system will remain down for an extended period of time. 



### 5.7 Geographic Disaster Recovery Considerations

- Backups serve as the last line of defense for data protection.
- Backups should be stored in data centers that are unlikely to be affected by the same disaster as the primary facility.
- Redundant data centers should also be located geographically distant from facilities.
- Cloud computing facilitates the use of geographically distant facilities.
- Data storage locations may have legal implications.

#### Data Sovereignty

- Data is subject to the law of the jurisdiction where it's stored.



### 5.8 Testing BC/DR Plans

#### DR Testing Goals

1. Validate that the plan functions correctly
2. Identify necessary plan updates

#### DR Test Types

- Read-through
- Walk-through
- Simulation
- Parallel test
- Full interruption test

##### Read-through (Checklist Review)

- Ask each team member to review their role in the disaster recovery process and provide feed back.

##### Walk-through (Tabletop Exercise)

- Gather the team together for a formal review of the disaster recovery plan.

##### Simulation

- use a practice scenario to test the disaster recovery plan.

The 3 test types we've discussed so far are all theoretical exercises. They talk about disaster recovery, but don't actually use any disaster recovery technology. 

##### Parallel test

- Activate the disaster recovery facility but do not switch operations there.

##### Full interruption test

- Switch primary operations to the alternate facility and can be very disruptive to business.

**DR testing strategies often combine multiple types of tests.**



### 5.9 After Action Reports

- After action reports create a formal record of a disaster recovery (DR) or business continuity (BC) event.

These reports are an important because they facilitate the recognition of lessons learned and allow the organization to continuously improve its business continuity and disaster recovery processes.

- Conduct after action reviews after every BC or DR event, even those that are considered successful.
- Begin the report with a brief executive summary.
- Provide enough background to allow the reader to understand the context.
- Answer all the key factual questions around the event
- Include lessons learned during the response.
- Conclude with clear next steps.



### Chapter Quiz

1. What goal of security is enhanced by a strong business continuity program?

   A. confidentiality

   B. non-repudiation

   C. integrity

   D. availability

2. What type of control are we using if we supplement a single firewall with a second standby firewall ready to assume responsibility if the primary firewall fails?

   A. component redundancy

   B. load balancing

   C. high availability

   D. clustering

3. What is the minimum number of disks required to perform RAID level 5?

   A. 1

   B. 2

   C. 4

   D. 3

4. What disaster recovery metric provides the targeted amount of time to restore a service after a failure?

   A. MTO

   B. RPO

   C. RTO

   D. TLS

5. What type of backup includes only those files that have changed since the most recent full or incremental backup?

   A. full

   B. incremental

   C. partial

   D. differential

6. What type of disaster recovery site is able to be activated most quickly in the event of a disruption?

   A. hot site

   B. warm site

   C. lukewarm site

   D. cold site

7. Which one of the following disaster recovery tests involves the actual activation of the DR site?

   A. parallel test

   B. simulation

   C. walk-through

   D. read-through



Answers:

1. availability
2. <font color=red>high availability</font>
3. **3**
4. <font color=red>RTO</font>
5. <font color=red>incremental</font>
6. hot site
7. parallel test



## 6. Incident Response

### 6.1 Security Incidents

Cyber security professionals are often called upon to handle the identification, prioritization, response, and recovery efforts related to security incidents.

#### Security Event

- Any observable action on a computer system that impacts security

This may be a user accessing a web page, a file being written to disk by a process, a connection being established through a firewall, or any other security related event. Thousands of security events take place every hour on active networks. 

#### Adverse Security Event

- Any security event with negative consequences

A user attempting to access a file without permission is an example of an adverse event, as is the receipt of a phishing email message.

#### Security Incident

- Any adverse event that violates security policies

For example, if the user that tried to access a file was able to view confidential information and send it to a third party without permission, that would be a security incident. Similarly, if the recipient of a phishing message clicked a link in the message and provided their password to an attacker, that would also be a security incident. 

**Security professionals must identify and respond to adverse events and incidents.**

**Categorizing incidents allows the implementation of different response procedures.**

#### Attack Vector Categorization

- External media
- Attrition: conduct brute force attacks, such as exhausting network bandwidth
- Web
- Email
- Improper usage
- Equipment loss or theft
- Other



### 6.2 Preparing for Incident Response

NIST Special Publication 800-61

[Computer Security Incident Handling Guide (NIST)](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-61r2.pdf)

#### IR Program Components

1. Policy and plan documentation
2. Procedures for incident handling
3. Guidelines for communicating externally
4. Structure and staffing model for the team
5. Description of relationships with other group

#### Incident Response Policy

- Provides foundational authority for the program
- Defines incidents that fall under the policy
- Includes an incident prioritization scheme

#### Incident Response Procedures

- Contain the details of your plan
- Notification
- Escalation
- Reporting
- System isolation
- Forensic analysis
- Evidence handling

#### Communications Guidelines

- Senior executives
- Legal counsel
- Public relations
- Regulatory agencies
- Law enforcement

**Law enforcement brings resources to an investigation but also introduces new risks and regulations.**

Once you file a report with law enforcement, it's likely that the details of the incident will become public, which may be undesirable. Also, law enforcement officers are held to much higher standards in gathering and processing evidence. 

#### Building an IR Team

- Management
- Information security
- Subject matter experts
- Legal counsel
- Public affairs
- Human resources
- Physical security

**Diverse team membership builds relationships that are crucial during an incident.**

**Testing incident response plans ensures readiness for real incidents.**



### 6.3 Incident Identification and Containment

**Monitoring is crucial to effective incident identification.**

#### Incident Data Sources

- IDS and IPS
- Firewalls
- Authentication systems
- Integrity monitors
- Vulnerability scanners
- System event logs
- NetFlow records
- Anti-malware packages

#### Security Incident and Event Management (SIEM)

- Security solution that collects information from diverse sources, analyzes it for signs of security incidents, and retains it for later use

**The first reports of an incident may come from *external* sources!**

**Threat intelligence solutions provide important strategic and tactical insights.**

#### First Responders Must Act Quickly

- Isolate affected systems!

#### ! EXAM TIPS

The highest priority of a first responder must be containing damage through isolation.



### 6.4 Escalation and Notification

#### Escalation and Notification Objectives

- Evaluate incident severity based upon impact
- Escalate response to an appropriate level
- Notify management and other stakeholders

#### Triaging Incidents

- Low impact
- Moderate impact
- high impact

##### Low-Impact Incidents

- Have minimal potential to affect security
- Are normally handled by first responders
- Don't require after-hour response

##### Moderate-Impact Incidents

- Have significant potential to affect security
- Trigger incident response team activation
- Require prompt notification to management

##### High-Impact Incidents

- May cause critical damage to information or system
- Justify an immediate, full response
- Require immediate notification to senior management
- Demand full mobilization of incident response team

**First responders must have the ability to quickly activate a full incident response process.**



### 6.5 Incident Mitigation

**Control damage and loss to the organization through containment**

#### Containment Strategy Evolution

1. Damage potential
2. Evidence preservation
3. Service availability
4. Resource requirements
5. Expected effectiveness
6. Solution timeframe

**Balance business needs and security objectives.**

**Attackers may detect containment actions.**

This may cause the attacker to speed up activities, destroy evidence, or perform other actions that are detrimental to the incident response, or the organization's business. 

#### Mitigation Ends with Stability

- Business functioning without danger



### 6.6 Eradication and Recovery

**Remove effects of the incident and return to normal operations.**

#### Technical Recovery Efforts

- Rebuild compromised systems
- Remove malware
- Disable breached accounts
- Restore corrupted or deleted data

**Reconstitution corrects vulnerabilities.**

#### Remediation Efforts

- Applying security patches
- Updating firewall rules
- Implementing intrusion prevention
- Strengthening access controls

**Use a phased approach to recovery and reconstitution.**



### 6.7 Lessons Learned and Reporting

Once the incident response team returns the organization to a normal operating state all too often, the response effort ends without completing an important final step: conducting a Lessons Learned session and writing up the results in an incident report. 

#### Lessons Learned

- Provides incident responders with an opportunity to reflect on the incident response efforts and offer feedback that will improve the organization's response to future incidents
- Use a trained facilitator

Ideally, this facilitator should have played no role in the incident response, leaving him or her with no preconceived notions about the response. The facilitator should be a neutral party who simply helps guide the conversation. 

- Time is of the essence

#### Lessons Learned Questions

- How well did staff and management perform?
- Were documented procedures followed?
- Were those procedures adequate?
- Did any actions inhibit the recovery effort?
- What would responders do differently next time?
- How could information sharing improve?
- What could prevent similar incidents?
- What should the organization watch for?
- What tools or resources are needed?

**Create a report that includes lessons learned and recommendations.**



### Chapter Quiz

1. Which one of the following individuals would not normally be found on the incident response team?

   A. CEO

   B. human resources staff

   C. legal counsel

   D. information security professional

2. During an incident response, what is the highest priority of first responders?

   A. restoring operations

   B. identifying the root cause

   C. containing the damage

   D. collect evidence



Answers:

1. <font color=red>CEO</font>
2. containing the damage



## 7. Forensics

### 7.1 Conducting Investigations

#### Investigation Types

- Operational investigations
- Criminal investigations
- Civil investigations
- Regulatory investigations

#### Operational Investigations

- Look into technology issues
- Seek to resolve technology issues
- Restore normal operations as quickly as possible
- Use very low standards of evidence
- Involve root cause analysis

#### Criminal Investigations

- Look into possible crimes
- Involve the possibility of fines and jail time
- Use the *beyond a reasonable doubt* standard of evidence

#### Civil investigations

- Resolve disputes between parties
- Do not involve the possibility of fines and jail time
- Use the *preponderance* of the evidence standard

e.g. contract disputes, employment law violations, and intellectual property infringement cases.

#### Regulatory Investigations

- Are conducted by the government

Are conducted by government agencies looking into potential violations of administrative law. Regulatory investigations may be either civil, or criminal in nature, and they use the standard of evidence that's appropriate for the type of case that the agency plans to bring. 

**Interviews are a valuable tool available to investigators.**

It is important to remember that an interview is always voluntary. When investigators question a hostile subject without that subject's consent, it's known as an **interrogation**. 

#### ! EXAM TIPS

Cybersecurity investigators should leave interrogations to law enforcement!



### 7.2 Evidence Types

#### Evidence Types

- Real evidence
- Documentary evidence
- Testimonial evidence

#### Real Evidence

- Consists of tangible objects

#### Documentary evidence

- Consists of written information

##### Documentary Evidence Rules

1. Authentication rule
   - Documents must be authenticated by testimony.
2. Best evidence rule
   - Original documents are superior to copies.
3. Parol evidence rule
   - Written contracts are assumed to be the entire agreement.

#### Testimonial Evidence

- Consists of witness statements

##### Direct Evidence

- Witness provides evidence based upon his or her own observations.

##### Expert Opinion

- Expert witness draws conclusions based upon other evidence

**Testimonial evidence may not consist of hearsay.**



### 7.3 Digital Forensics

#### Digital Forensics

- Investigative techniques that collect, preserve, analyze, and interpret digital evidence

**Investigations must *never* alter evidence!**

#### Volatility

- The relative permanence of a piece of evidence; evidence that may not last long is more volatile than more permanent sources of evidence.

#### Order of Volatility

1. Network traffic
2. Memory content
3. System and process data
4. Files (collect temporary files such as system swap space first.)
5. Logs
6. Archived records

**Time offsets help correlate records from different sources.**

Just because a system recorded a time stamp on a file or a log entry doesn't mean that that time is accurate. After all, how many of us have devices in our homes that constantly display an incorrect time? When conducting any forensic data capture, investigators should take note of the current time from a reliable source and compare it to the time on the device.

#### Consider Alternate Evidence Sources

- Video recordings
- Witness statements

**Track your use of time and resource**

**Recovery and preservation of evidence are the core tasks of digital forensics.**



### 7.4 System and File Forensics

- Investigations must *never* alter evidence!

- Images take the place of original physical media.
- Write blockers, also known as forensic disk controller, prevent accidental modification of disks during imaging

#### Hashes Protect Evidence

- They provide a unique file signature

**Use hashes to demonstrate that a file hasn't been altered.**

If the investigators compute hash values at the time they collect evidence, they can then recompute hash values when analyzing and presenting evidence or an image of that evidence to prove that the file they are working on is identical to the file that was originally collected. 

#### ! EXAM TIPS

Learn more about hashing in the CompTIA Security+ (SY0-501) Cert Prep: 6 Cryptography.

#### Other Forensic Sources

- Screenshots
- Memory contents
- Process table
- Operating system configuration

#### ! EXAM TIPS

Never try to perform forensics yourself unless you've received appropriate training!



### 7.5 Network Forensics

- Ethernet networks send electrical pulses over copper wire.
- Fiber-optic networks send light pulses over strands of glass.
- Wireless networks send pulses via radio waves.

**Network communications may be intercepted.**

Copper and fiber optic cables may be tapped. Wireless radio signals may be intercepted. Switches and routers can be compromised. 

#### Wireshark Monitors Networks

- Capturing full packet data

**Full packet capture requires lots of storage.**

If you know what you're looking for, you can use filters to save only relevant information, but those filters are only useful when you know in advanced that you'll be conducting a forensic investigation. In most cases, you don't know you'll need network forensic information until after an incident occurs. Network forensics then becomes a big data problem. 

#### NetFlow Summarizes Traffic

- Providing high-level information

##### Telephone Bill

- Numbers called
- Timestamp
- Call duration

##### NetFlow Data

- IP addresses and ports
- Timestamp
- Amount of data transferred

This provides valuable who talked to whom information about network communications, but just like a telephone bill doesn't include the content of the telephone communication, NetFlow data doesn't include the payload of the packets that were transferred. NetFlow data is often captured by routers, firewalls, and other network devices stationed at network choke points.

**Routers and firewalls capture NetFlow data.**



### 7.6 Software Forensics

#### Intellectual Property

- Software forensics may be used to  resolve intellectual property disputes between two parties.

#### Malware Origins

- Software forensics may be used to identify the author of malicious software found on a system.

Example

[GRIZZLY STEPPE – Russian Malicious Cyber Activity by NCCIC](https://us-cert.cisa.gov/sites/default/files/publications/JAR_16-20296A_GRIZZLY%20STEPPE-2016-1229.pdf)

The idea is that if cybersecurity analysts find these signatures in code on their systems, they may be able to attribute the code to that Russian source. 

However, now that the signature information is public, it would be easy for an attacker to simply include the signature in their own attack, in an attempt to frame the Russian government for an attack they had nothing to do with. For this reason, you must take publicly available signature information with a grain of salt when seeking to use it for attack attribution.

Conducting software forensic analysis is tricky work and requires both advanced software engineering knowledge and investigative skills. Information security professionals should not attempt to do this work on their own, but rather should consult trained experts if required.



### 7.7 Embedded Device Forensics

#### Embedded Devices

- Special-purpose computers inside smart devices found in homes, businesses, and industrial settings
- Vehicles often contain many embedded devices with valuable forensic information
- Embedded devices are often found in homes

Smart home assistants, such as Amazon's Alexa, and Google's Home, also collect information about us and send it off to the Cloud. These devices contain microphones capable of recording activity in an area and then sending it to a Cloud service speech recognition. 



### 7.8 Chain of Custody

#### Chain of Custody

- Provides a paper trail for evidence

In the case of digital forensics, this might include the original hard drive or other primary evidence collected by investigators and used for later analysis. 

**Evidence should be labeled and stored in a sealed evidence container.**

#### Evidence Log Events

- Initial collection
- Transfer
- Storage
- Opening and resealing the container

#### Evidence Log Entry Details

- Investigator name
- Date and time
- Purpose
- Nature of action

**Evidence logs must be available to present in court.**

If an opposing attorney can show a failure to appropriately maintain the evidence log, this is a situation known as a breach of the chain of custody. 



### 7.9 Electronic Discovery (ediscovery)

**There are three major steps in the electronic discovery process.**

```mermaid
graph LR
A[Preservation] --> B[Collection]
B[Collection] --> C[Production]
```

**Litigation holds require the preservation of relevant electronic and paper record.**

It's important to remember that preservation includes more than just not intentionally destroying information. 

**System administrators must suspend the automatic deletion of relevant logs.**

This most often affects IT groups by requiring the preservation of log entries. If there are logs relevant to the dispute, IT staff must ensure that those logs are preserved and not automatically purged by a system after a certain period of time, or after the log files reach a certain size. 

**Security teams often assist in collection efforts.**

#### Sources of Electronic Records

- File servers
- Endpoint systems
- Email messages
- Enterprise systems and cloud services

**Electronic discovery management systems coordinate collection efforts.**

**If production occurs, attorneys must review documents for relevance and turn them over to the other side.**

**Most litigation holds never move forward to the production phase.**



### Chapter Quiz

1. The chain of custody must be updated EVERY time someone handles a piece of evidence.

   A. TRUE

   B. FALSE

2. Software forensics may be used to identify the origin of malware.

   A. TRUE

   B. FALSE

3. What type of investigation would typically be launched in response to a report of high network latency?

   A. criminal

   B. civil

   C. operational

   D. regulatory

4. Server logs are an example of _____ evidence.

   A. testimonial

   B. expert opinion

   C. real

   D. documentary

5. Which evidence source should be collected first when considering the order of volatility?

   A. temporary files

   B. process information

   C. logs

   D. memory contents

6. What type of technology prevents a forensic examiner from accidentally corrupting evidence while creating an image of a disk?

   A. sealed container

   B. hashing

   C. evidence log

   D. write blocker

7. Three of these choices are data elements found in NetFlow data. Which is not?

   A. packet content

   B. amount of data transferred

   C. source address

   D. destination address

8. During what phase of ediscovery does an organization share information with the other side?

   A. collection

   B. analysis

   C. preservation

   D. production



Answers:

1. TRUE
2. TRUE
3. operational
4. documentary
5. **memory contents**
6. write blocker
7. packet contents
8. **production**



## 8. Data Security and Privacy

### 8.1 Understanding Data Security

#### Data at Rest

- Data stored for later use on a hard drive, USB device, magnetic tape, cloud service, or other data storage environment

Data at rest is vulnerable to theft if an attacker gains either physical or logical access to the storage media. This might be by stealing a hard drive or hacking into an operating system that has the drive mounted. 

#### Data in Motion

- Data being sent over a network between two systems

It might be data moving from a storage location to a user's computer, or data that is simply being transmitted between two systems, such as a user entering their credit card number into a website or sending an email message. 

Data in motion must be protected against eavesdropping attacks because this data often travels over public networks such as the internet. 

#### Data Security Controls

- Clear policies and procedures covering data use and security
- Encryption to protect sensitive information
- Access controls on stored data

You can use file system access control lists to specify who may view, modify, or delete information stored on a device. 

#### Big Data

- Big data is the use of datasets much larger than those that may be handled by conventional data processing and analytic techniques.

For example, big data rarely uses relational databases because of the significant overhead involved. Instead, big data storage and analysis uses specialized technology like the key value stores of NoSQL databases. 

**Big Data Requires Special Security Considerations**



### 8.2 Data Security Polices

#### Data Security Policy Criteria

- Foundational authority for data security efforts
- Clear expectations for data security responsbilities
- Guidance for requesting access to information
- Process for granting policy exceptions

#### Data Classification Policies

- Describe security levels

These classifications are assigned based upon both the sensitivity of information and the criticality of that information to the enterprise.

#### Classification Levels

| Military Classification | Business Classification |
| ----------------------- | ----------------------- |
| Top Secret              | Confidential            |
| Secret                  | Proprietary             |
| Confidential            | Private                 |
| Unclassified            | Public                  |

**Classification is used as the basis for other data handling requirements.**

#### Data Storage Policies

- Appropriate storage locations
- Access control requirements
- Encryption requirements

#### Data Transmission Policies

- Appropriate data transmissions
- Encryption requirement
- Acceptable transmission mechanism

#### Data Lifecycle Policies

- Describe end-of-life for data

This is important, because information may retain sensitivity, even after the organization no longer requires it. 

##### Data Retention Policies

- Specify the minimum and/or maximum period that an organization will retain different data elements

Data retention policies limit an organization's risk exposure by ensuring that data is kept for as long as it is needed, but no longer. 

##### Data Disposal Policies

- Describe proper techniques for destroying data that is no longer needed by the organization

This is extremely important, because of data remnants issues. Simply deleting files or formatting a hard disc is not sufficient to remove all traces of that data from a device. 

Depending upon the type of media used, this may include burning, shredding or pulping paper, and pulverizing, degaussing, purging, or wiping discs, flash drives, and other electronic media. These tools include software applications, such as Darik's Boot And Nuke (DBAN), otherwise known as DBAN, and hardware tools, such as magnetic degaussers and device shredders. 



### 8.3 Data Security Roles

#### Three Tier Model

![08_03_3_Tier_Model](https://github.com/Jingy1Ma/CompTIA-Security-Exam-SY0-501/blob/main/Images/05_Risk_Management/08_03_3_Tier_Model.png?raw=true)

##### Data Owners

- Are business leaders with overall responsibility for data. They set policies and guidelines for their data sets.

Practically speaking, most individuals who are senior enough to hold the position of data owner do not have the time available to get involved in the nitty gritty decisions of data governance. They usually delegate that responsibility to a Data Steward

##### Data Stewards

- Handle the day-to-day data governance activities. They are delegated responsibility by data owners

##### Data Custodians

- Actually store and process information and are often IT staff members.

Technologists are rarely data owners or data stewards, but they are usually data custodians for almost all of the data in the organization, due to the nature of their jobs. 

**Privacy officers are responsible for ensuring that the organization meets its privacy obligations.**



### 8.4 Data Privacy

#### Personally Identifiable Information (PII)

- Records that may be associated with a specific individual

PII might include extremely sensitive data such as credit reports and tax returns, or more mundane records such as movie viewing histories. 

#### Protected Health Information (PHI)

- Health records about an individual patient

In many cases, PHI is regulated under the Health Insurance Portability and Accountability Act, HIPAA. 

**Generally Accepted Privacy Principles (GAPP) outline 10 components of data privacy.**

#### GAPP Developers

- American Institute of Certified Public Accountants (AICPA)
- Canadian Institute of Chartered Accountants (CICA)
- Information System Audit and Control Association (ISACA)
- Institute of Internal Auditors (IIA)

##### 1. Management

- Organization handling private information should have polices, procedures, and governance structures in place to protect privacy

##### 2. Notice

- Data subjects should received notice that their information is being collected and used, as well as access to the privacy policies and procedures followed by the organization.

##### 3. Choice and Consent

- The organization should inform data subjects of their options regarding the data they own and get consent from those individuals for the collection, storage, use, and sharing of that information.

##### 4. Collection

- The organization should only collect personal information for purposes disclosed in their privacy notice

##### 5. Use, Retention, and Disposal

- Organizations should only collect and use personal information for disclosed purposes and they should dispose of the data securely as soon as it is no longer needed for the disclosed purpose.

##### 6. Access

- Organizations should provide data subjects with the ability to review and update their personal information.

##### 7. Disclosure to Third Parties

- Organizations should only share information with third parties if that sharing is consistent with the purposes disclosed in privacy notices and they have the consent of the individual to share that information.

##### 8. Security

- The organization must secure private information against unauthorized access, either physically or logically.

##### 9. Quality

- The organization should take reasonable steps to ensure that the private information they maintain is accurate, complete, and relevant.

##### 10. Monitoring and Enforcement

- The organization should have a program in place to monitor compliance with its privacy policies and provide a dispute resolution mechanism.



### 8.5 Limiting Data Collection

**Notice and consent is just the first level of restriction on data collection.**

**Never collect undisclosed information, even if it seems "incidental".**

#### Minimize Information Collected

- Delete unneeded information quickly

For example, you might be using a web server that records more information in web access logs than you need for your disclosed analysis purposes. When that's the case, you still must disclose this collection to individuals because, after all, you are collecting the information. The difference is that if you don't have legitimate need to keep the information, you should remove unnecessary information from those records as quickly as possible, preferably through an automated process that doesn't require any human intervention. 

**Ensure that your data collection practice are fair and lawful.**

#### Monitor Third Parties

- Verify their privacy practices

In those cases you should take reasonable steps to ensure that the third party is collecting that information in accordance with privacy principles and that the third party has obtained prior permission to share it with you. 



### 8.6 Privacy Assessment

#### Privacy Threshold Analysis (PTA)

- Evaluates the use of personal information to determine whether privacy controls are necessary

When a system reaches the threshold specified in the PTA, organizations must complete a PIA that dives into deeper detail to ensure that the system meets privacy requirements. 

#### Privacy Impact Assessment (PIA)

- Evaluates the privacy controls used by IT system to determine whether they are sufficient

The Privacy Threshold Assessment requires that agencies answer a series of questions about the types of information that the system will handle, how the system is connected to other systems and other technical and operational details.

Example

[PRIVACY THRESHOLD ANALYSIS (PTA) by Homeland Security](https://www.dhs.gov/xlibrary/assets/privacy/privacy_pta_template.pdf)

#### PIA 3 Goals

1. Ensures that PII handling meets all applicable requirements
2. Identifies risks associated with handling PII within an IT system
3. Examines privacy controls and recommends mitigations

#### PIA Questions

- What information is being collected?
- Why is the information being collected?
- What is the intended use of the information?
- With whom will the information be shared?
- What notice will be provided to individuals?
- How will the information be secured?
- Is the information subject to the Privacy Act?

#### PIA Requirements

1. Whenever a PTA requires the completion of a PIA
2. Before developing or purchasing PII systems
3. After any significant change to a PII system
4. Every 3 years

Example

[Privacy Impact Assessment Template](https://www.dhs.gov/xlibrary/assets/privacy/privacy_pia_template.pdf)

It is much more detailed than the PTA and requires detailed answers about the system and its privacy controls. 



### Chapter Quiz

1. Once an organization complies with GAPP, best practice says they should collect as much information as possible to provide good service, provided that they remain GAPP compliant.

   A. TRUE

   B. FALSE

2. What technology is commonly used for Big Data datasets?

   A. PostreSQL

   B. NoSQL

   C. MySQL

   D. SQL Server

3. Which one of the following is not a commonly-used business classification level?

   A. Internal

   B. Highly Sensitive

   C. Top Secret

   D. Sensitive

4. What data security role is normally filled by a senior-level official who bears overall responsibility for the data?

   A. data custodian

   B. data guardian

   C. data owner

   D. data steward

5. Which one of the following is not one of the GAPP principles?

   A. collection

   B. management

   C. integrity

   D. notice



Answers:

1. FALSE
2. NoSQL
3. Top Secret
4. **data owner**
5. **integrity**



## Reference

[1] https://www.linkedin.com/learning/comptia-security-plus-sy0-501-cert-prep-5-risk-management

[2] [Security Threat and Controls](http://ccilearning.com/store-ca/wp-content/uploads/2015/03/CompTIA%20Security+%20Student-Sample.pdf)

[3] [Computer Security Incident Handling Guide (NIST)](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-61r2.pdf)

[4] [PRIVACY THRESHOLD ANALYSIS (PTA) by Homeland Security](https://www.dhs.gov/xlibrary/assets/privacy/privacy_pta_template.pdf)

[5] [Privacy Impact Assessment Template](https://www.dhs.gov/xlibrary/assets/privacy/privacy_pia_template.pdf)


