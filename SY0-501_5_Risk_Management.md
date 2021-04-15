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



## Reference

[1] https://www.linkedin.com/learning/comptia-security-plus-sy0-501-cert-prep-5-risk-management

[2] [Security Threat and Controls](http://ccilearning.com/store-ca/wp-content/uploads/2015/03/CompTIA%20Security+%20Student-Sample.pdf)


