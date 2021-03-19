# CompTIA Security+ Exam (SY0-501): Threats, Attacks, and Vulnerabilities

- Up to 90 minutes
- Up to 90 questions

Domains:

- Threats, Attacks, and Vulnerabilities (21%)
- Technologies and tools (22%)
- Architecture and design (15%)
- Identity and access management (16%)
- Risk management (14%)
- Cryptography and PKI (12%)

Formats:

- multiple choice questions
- performance-based questions

Grading Scale:

To pass the exam: at least 750 on a scale ranging from 100 to 900

Study Resources:

[1] [Get Certified Get Ahead](https://blogs.getcertifiedgetahead.com/)

[2] [CertMike](https://www.certmike.com/)



Objectives:

- Analyze IoC and determine the type of malware used; understand the propagation method and payloads used by various types of malicious code.
- Compare and contrast different types of attacks; understand the flavors of spam and phishing attacks; understanding of network attacks, wireless and cryptographic attacks
- Explain threat actors and attributes.
- Explain the proper use of penetration testing, including active and passive reconnaissance, pivoting, and escalation of privilege; understand the differences between black, white, and gray box testing.
- Use appropriate tools and techniques for vulnerability scanning, including identifying vulnerabilities, nothing the lack of security controls, and identifying common misconfigurations.
- Explain the impact associated with different types of vulnerabilities (e.g. race conditions, end of vendor support, input and error handling, memory issues, zero day attacks)



## 1. Malware

### 1.1 Comparing viruses, worms and Trojans (Propagation)

Two components of malware

- Propagation mechanism: The way that a malware object spreads
- Payload: The malicious action that the malware performs

**Any** malware object can carry **any** payload.

#### Viruses: Spread by human action

The best way to defend against viruses is user education

#### Worms: Spread by themselves

- Requires vulnerable systems to spread

The best way to defend against worms is keeping systems updated with the most recent operating system and application patches

Examples:

- The RTM Worm: first major worm outbreak, in 1988
- Stuxnet: infiltrated Iranian nuclear facility, in 2010

#### Trojan Horses

- Disguise themselves as beneficial programs

- Act as advertised when they are run
- Deliver their malicious payload behind the scenes

Application control provides a good defense limiting the software that may run on the systems to titles and versions specifically approved by administrators.

#### Remote Access Trojans (RAT)

- Provides backdoors to hacked systems

#### Propagation Mechanisms

- Viruses: spread through human action
- Worms: spread by themselves
- Trojan horses: pose as beneficial software

#### ! EXAM TIPS

Know the differences between viruses, worms and Trojan horses



### 1.2 Comparing adware, spyware and ransomware (Payload)

#### Adware: Displays advertisements

Mechanisms

- Changing the default search engine
- Displaying pop-up advertisements
- Replacing legitimate ads with other ads

#### Spyware: Gathers information

Techniques

- Logging keystrokes
- Monitoring web browsing
- Searching hard drives and cloud storage

#### Ransomware: Bocks access to your files 

Example:

CryptoLocker: arrives via email attachment, encrypts local files using strong RSA, in 2014

#### Preventing Malware

- Anti-malware software
- Security patches
- User education

#### Payloads

- Adware: Display advertisements
- Spyware: Gathers information
- Ransomware: Blocks access to your files 



### 1.3 Understanding backdoors and logic bombs

(Viruses), worms, Trojans, adware, spyware, and ransomware have one thing in common: they are independent programs written by malware developers to deliver malicious payload

However, instead of being an independent programs, they are pieces of code inserted into other applications with malicious intent

#### Backdoors: Provide workaround access

- Hardcoded accounts
- Default passwords
- Unknown access channels

#### Logic Bombs: Deliver a triggered payload

Logic Bomb Conditions:

- Date/time reached
- File contents
- API call results

#### Malicious Code

- Backdoors: Provide unregulated access
- Logic Bombs: Deliver a triggered payload

In addition to the standard anti-malware controls, you should

- routinely change default passwords
- disable unused accounts
- monitor security bulletins for news of logic bombs and backdoors



### 1.4 Advanced Malware

The Root Account: A special superuser account that provides unrestricted access to system resources.

#### Rootkits

- Originally were designed for privilege escalation
- Now used to describe software techniques designed to hide other software on a system

**Rootkit Payloads**

- Backdoors
- Botnet agents
- Adware/Spyware
- Antitheft mechanisms for copyrighted content (not always malicious in design)

**User Mode vs. Kernel Model **

![Ring_Protection_Model](https://github.com/Jingy1Ma/CompTIA-Security-Exam-SY0-501/blob/main/Images/01_04_Ring_Model.PNG?raw=true)

User mode rootkits

- Run with normal user privileges
- Are easy to write and difficult to detect

Kernel model rootkits

- Run with system privileges
- Are difficult to write and easy to detect

#### Polymorphic Viruses: Change to avoid detection

Signature Detections: Identifying viruses by detecting known code patterns from a database.

##### **Polymorphic Virus Techniques**

- Changing their own code to avoid signature detection
- Using encryption with a different key on each infected system

#### Armored Viruses: Prevent reverse engineering

Armored Viruses Techniques

- Writing the virus in obfuscated assembly language
- Blocking the use of system debuggers
- Preventing the use of sandboxing

#### Payloads

- Rootkits: Escalate user privileges (now used to hide)
- Polymorphism: Changes code to avoid detection
- Armored Viruses: Prevent reverse engineering



### 1.5 Botnet: Network of infected machines

- Malware Target: Added to botnet once infected
- Botnet: Network of infected machines

#### How are botnet used?

- Renting out computing power
- Delivering spam
- Engaging DDoS attacks
- Mining Bitcoin
- Waging brute force attacks

#### **Botnet Command and Control**

- Command and control networks relay orders
- Communication must be indirect and redundant
  - Internet Relay Chat (IRC)
  - Twitter
  - Peer-to-peer within the botnet

#### Botnets

1. Infect systems
2. Convert to bots
3. Infect others
4. Check in 
5. Get instructions
6. Deliver payload



### 1.6 Advanced persistent threats

- Zero Days and the Advanced Persistent Threat (APT)

- Undiscovered security vulnerabilities lurk in existing code

#### Ethical Disclosure

1. Notify the vendor of the vulnerability
2. Provide the vendor a reasonable amount of time to create a patch
3. Disclose the vulnerability publicly

#### What if a vulnerability is kept secret?

This type of vulnerability is known as Zero-Day Vulnerability. 

- Zero-day vulnerability: A vulnerability in a product that has been discovered by at least one researcher but has not yet been patched by the vendor
- Window of Vulnerability: The time between the discovery of a zero-day vulnerability and the release of a security patch

**Exploiting zero days is difficult.** However, there's a type of attacker that is known to use this type of attack.

#### Advanced Persistent Threats (APTs)

- Are well-funded and highly skilled
- Are typically government sponsored
- Have access to zero days and other sophisticated weapons
- Work methodically to  gain access to a target

#### Defending Against APTs is Difficult

- Build a strong security foundation
- Implement strong encryption
- User rigorous monitoring



### Chapter Quiz

1. Cryptolocker is an example of what type of malicious software?

   A. Trojan horse

   B. ransomware

   C. adware

   D. spyware

2. What type of malware delivers its payload only after certain conditions are met, such as specific date and time occurring?

   A. worm

   B. Trojan horse

   C. ransomware

   D. logic bomb

3. What technique does some malware use to modify itself each time it infects a new system to avoid signature detection systems?

   A. bipartite

   B. armored

   C. multipartite

   D. polymorphism

4. Which of the following is a common command-and-control mechanism for botnets?]

   A. HTTP

   B. FTP

   C. IRC

   D. SMTP



Answers:

1. ransomware
2. logic bomb
3. polymorphism
4.  IRC



## 2 Understanding Attackers

### 2.1 Cybersecurity adversaries

#### Differentiating Attackers

- Internal vs. external attackers
- Level of sophistication
- Access to resources
- Motivation
- Intent

**Script kiddies** are unskilled attackers who simply reuse hacking tools developed by others.

**Hacktivists** seek to use hacking tools to advance political and social agendas.

**Organized crime** seeks to use hacking tools, such as ransomware, for financial gain.

**Competitors** may use hacking tools and techniques for corporate espionage purposes.

**Nation-states** sponsor highly sophisticated advanced persistent threat (APT) groups. 



### 2.2 Preventing insider threats

#### Insider Attackers Are Commonplace

- 51% of organizations experiencing a security breach experienced an insider attack
- 72% of insider attacks are handled internally
- 67% of insider breaches are more costly than external attacks

#### Privilege Escalation Attacks

In many cases, inside attacks occur at the hands of the most trusted users, such as system administrators and executives. But not all attacks use these privileged accounts. **Privilege escalation attacks** can take a normal user's credentials and transform them into powerful  super user accounts. Before you think that normal users don't have the technical skills required to conduct a privilege escalation attack, remember they may have skills that you don't know about. And even if they don't have those skills, your receptionist might be married to an information security expert

#### Most Insider Attackers...

The people who conduct insider attacks often share some common characteristics

**Had personal predispositions**

- Mental illness
- Series of rule violations

**Were disgruntled due to unmet expectations**

- Low salary
- Passed over for promotion

**Were triggered by stressful events**

- Performance evaluation
- Divorcer/death in family

**Showed technical precursors**

- Downloading hacker tools

- Inappropriate Internet use

**Used access methods unknown to management**

- 59% former employees
- 75% create alternative access paths (cuz they might typically disabled when they're terminated)

##### HR Practices Control Insider Threats

- Perform background checks to uncover past legal issues
- Give users only the permissions that they need
- Require multiple users to carry our sensitive operations
- Implement mandatory vacations for critical staff

##### Behavioral Indicators from the FBI

- Tacking work materials home
- Interest in issues outside responsibilities
- Unexplained duplication of materials
- Strange network access pattern
- Using personal hardware/software
- Working odd hours
- Unexplained foreign contacts/trips
- Unexplained affluence



### 2.3 Threat intelligence

#### Threat Intelligent

The set of activities that an organization undertake to educate itself about changes in cybersecurity threat landscape, and adapt security controls based upon that information

#### Open-Source Intelligence

- Uses public information
- Security websites
- News media
- Social media
- Government-sponsored security analysis centers
- Security researchers

#### Email Address Harvesting

- Searches for valid address
- Sends out spearing phishing attacks

#### **Many security companies offer commercial threat intelligence solutions. **



### Chapter Quiz

1. Which one of the following controls is not particularly effective against the insider threat?

   A. firewalls

   B. background checks

   C. least privilege

   D. separation of duties



Answers:

1. firewalls



## 3 Understanding Attack Types

### 3.1 Denial of service attacks

![CIA](https://github.com/Jingy1Ma/CompTIA-Security-Exam-SY0-501/blob/main/Images/03_01_CIA.PNG?raw=true)

- Makes a resource unavailable for legitimate use
- Sends a huge number of requests to a server
- Is difficult to distinguish from legitimate requests

#### Limitations of a DoS Attack

- Requires a massive amount of bandwidth
- Is easy to block based on IP addresses

That's where DDoS come into play

#### Distributed Denial of Service

A denial of service attack that leverages a botnet to overwhelm a target

**Ping Command** 

![Ping](https://github.com/Jingy1Ma/CompTIA-Security-Exam-SY0-501/blob/main/Images/03_01_Ping.PNG?raw=true)

#### Smurf Attack

![Smurf_Attack](https://github.com/Jingy1Ma/CompTIA-Security-Exam-SY0-501/blob/main/Images/03_01_Smurf_Attack.PNG?raw=true)

The smurf attack is also an example of a special type of DDoS attack known as Amplified DDoS Attack.

#### Amplified DDoS Attack

![Amplified_DoS](https://github.com/Jingy1Ma/CompTIA-Security-Exam-SY0-501/blob/main/Images/03_01_Amplified_DDoS.PNG?raw=true)

In a basic DDoS attack, bandwidth is a limiting factor. In an amplification attack, the attacker carefully chooses requests that have very large responses. The attackers can then send very small requests over his/her network connection that generate very large replies over the third party's network connection. Variations on the smurf attack send carefully crafted requests that have very large responses

**Amplification Factor** is the degree to which the attack increases in size:

$$\frac{Reply}{Request}=Amplification$$

$$\frac{512bytes}{64bytes}=8*Amplification$$



DDoS attacks are a serious threat to system administrators as they can quickly overwhelm a network with illegitimate traffic. Defending against them requires that security professionals understand them well and implement blocking technology on the network that identifies and weeds out suspected attack traffic before it reaches servers. This is often done with cooperation of ISP and third party DDoS protection services.



### 3.2 Eavesdropping attacks

#### Rely on a compromised communications path

- Network device tapping
- DNS poisoning
- ARP poisoning

Since simple eavesdropping is easily defeated by encryption, attackers can use the **Man in the Middle Attack** to step up the game a bit.

#### Man in the Middle Attack (MITM)

Instead of establishing communications with a legitimate server, the user then connects directly to the attacker. The attacker, in turn, connects to the legitimate server. The user authenticates to the fake server set up by the attacker, and the attacker acts as a relay, the man in the middle, and can view all of the communications that take place between the client and the server. 

The attacker receives the requests from the user, passes them onto the server, and receives the real responses, reads them, and then replays them to the original user, who has no idea that there is a man in the middle intercepting those communications.

**Man-in-the-browser attack exploit flaws in browsers and browser plugins**

If attackers have the ability to capture network traffic, they can also conduct a **Replay Attack**.

#### Replay Attack

It uses previously captured data, such as an encrypted authentication token, to create a separate connection to the server that is authenticated, but does not involve the real end user. If the attacker can resend the authentication sequence without the remote system noticing that it's being replayed, the attacker can then use those credentials for his or her own purposes.

**Replay Attack Limitations**

- The attacker can't see the encoded credentials

#### Preventing Eavesdropping Attacks

- Include a unique characteristic
  - Token
  - Timestamp
- Prevent reuse of captured credentials



Once an attacker gains access to the network underlying a connection, it becomes very difficult to protect those communications. Encryption, secure network configuration, and strong authentication mechanisms are all good ways to protect your applications and users from falling victim to eavesdropping attacks.



### 3.3 Network attacks

#### **Packets**

- Are the basic unit of network communications
- Contain a data payload to be sent
- Contain a header with additional information

Packet Header Flag:

![Header](https://github.com/Jingy1Ma/CompTIA-Security-Exam-SY0-501/blob/main/Images/03_03_Header_Flag.PNG?raw=true)

A typical packet has only 1 or 2 flags set to a value of 1.

#### Christmas Tree Packet

All of the flags are set to one. It's said to be lit up like a Christmas tree.

![Xmas_Tree](https://github.com/Jingy1Ma/CompTIA-Security-Exam-SY0-501/blob/main/Images/03_03_Xmas_tree.PNG?raw=true)

- Some systems can't handle all the flags being set
- Responses can be used to identify the operating system



**Domain Name Service (DNS)** A service that translates common domain names into IP addresses for the purpose of network routing.

**Hierarchical DNS Lookups**

![DNS_Lookup](https://github.com/Jingy1Ma/CompTIA-Security-Exam-SY0-501/blob/main/Images/03_03_DNS_Lookups.PNG?raw=true)

#### DNS Poisoning

Disrupt the normal operation of DNS by providing false results. The attacker inserts incorrect DNS records at any point along that hierarchy, and can then redirect the traffic to attacker's system. The attacker's system contains a web server built closely resemble the system that the unsuspecting victim expects to visit. When the victim logs on to the attacker's fake system, the attacker captures log on information.

In a well done DNS poisoning attack, the attacker passes the credentials through to the real system, and then captures all traffic between the client and server, preventing the victim from noticing the attack. That's a MITM attack

![DNS_Poisoning](https://github.com/Jingy1Ma/CompTIA-Security-Exam-SY0-501/blob/main/Images/03_03_DNS_Poisoning.PNG?raw=true)



**Address Resolution Protocol (ARP)** A protocol that translates logical (IP) addresses into the hardware (MAC) addresses on local area of networks.

#### ARP Poisoning

Much like DNS poisoning, ARP poisoning is a spoofing technique that provides false information in response to ARP requests. Unlike DNS poisoning, ARP poisoning only works on a local network. 

Normally, any system on the network sends all traffic bound for outside the network to a gateway system. When ARP spoofing occurs successfully, the victim system believes that another system is the gateway, and sends traffic to it. That system actually belongs to a malicious user engaging in a MITM attack.

![ARP_Poisoning](https://github.com/Jingy1Ma/CompTIA-Security-Exam-SY0-501/blob/main/Images/03_03_ARP_Poisoning.PNG?raw=true)



#### Typosquatting (URL Hijacking)

An attack that consists of registering domain names similar to official sites, hoping that users will make a typo and visit their site.

Example:

2012 Election Typosquatting

- Missing periods: ww<font color=red>wb</font>arackobama.com
- Missing letters: www.bar<font color=red>ak</font>obama.com
- Mistyped letters: www.barackoba<font color=red>n</font>a.com
- Added letters: www.bar<font color=red>r</font>ackobama.com
- Reversed letters: www.baracko<font color=red>ab</font>ma.com

**Domain hijacking attacks steal a domain registration or alter DNS records**

They may do this by contacting the domain registrar, and attempting to illegitimately transfer actual ownership of the domain to themselves, or they conduct a DNS attack that changes the legitimate site's DNS records.

#### Network Attacks

- **Christmas Tree Attack** Use packet flags to exploit a system
- **DNS/ARP Poisoning** Redirects or intercepts traffic
- **Typosquatting** Exploits typos to get web traffic



### 3.4 Network address spoofing

Network addresses are easily altered by anyone with administrative access to a system, so they should not be relied upon for authentication purposes. Attackers can modify both the IP address and the MAC address of a system

#### MAC Spoofing Attack

- Alters hardware addresses

**Anyone with administrative access to a system can change its MAC address.**

```bash
$sudo ifconfig en0
en0: flags=8863<UP,BROADCAST,SMART,RUNNING,SIMPLEX,MULTICAST> mtu 1500
		ether 20:c9:d0:44:ba:6f
		...
		
$sudo ifconfig en0 ether 00:00:aa:55:66
$sudo ifconfig en0
en0: flags=8863<UP,BROADCAST,SMART,RUNNING,SIMPLEX,MULTICAST> mtu 1500
		ether 00:00:aa:55:66
		...
```

#### IP Spoofing Attack

- Alters IP addresses

However, IP Spoofing Attack are often more difficult to use in reality, because it's difficult to reconfigure the network to receive return traffic at a spoofed IP address. For this reason, spoofed IP addresses are often used in DoS attacks where that return information isn't necessary, but they can't commonly be used in attacks that require two-way communication.



### 3.5 Password attacks

Password secure access to the vast majority of systems today. This time test approach does provides adequate security for many purposes, but also has potential drawbacks. Attackers can wage attacks designed to crack passwords stored in system files. Many recent attack used this approach to steal massive numbers of user accounts.

#### /etc/passwd: Password File

On Linux systems, password files contain user credentials. When a user attempts to login to a system, the login process checks the password file to determine whether the password is valid. Of course, the file doesn't simply contain a copy of the password, which would be an easy target for attackers and would also allow system admins to know all of the user password on a system. Instead, the password file contains a password hash computed using a one way hash function. When the user logs in, the login process takes the password, computes a hash, and then compares that hash with the one stored in the file. If they match, the user is logged in. This approach is still vulnerable to password cracking attempts, because a user who obtains a copy of the password file, which must be publicly accessible on the system for a number of technical reasons, can simply start guessing passwords and comparing the hashes offline in a brute force attack.

#### /etc/passwd: Removed Passwords

The first step in securing this approach is to remove password hashes from the publicly accessible `/etc/passwd` file. But, in this approach,  how does the system log users in?

#### /etc/shadow: Shadow File

The hashes still exist, but they are stored in a separate file, known as the shadow password file. Unlike the password file, the shadow file can be locked down and highly restricted, so only the super user root may access it.

**Hash Function** A mathematical function that converts a variable length input into a fixed-length input.

#### Hash Function Criteria

- It must produce a completely different output for each input
- It must be computationally difficult to retrieve the input from the output (irreversible)
- It must be computationally difficult to find two different inputs that generate the same output (collision)

Collision is because of a mathematical phenomenon known as the birthday problem.

#### The Birthday Problem

Collisions become common with large samples.

What are the odds two people in a room will share a birthday?

- 100% with 367 people
- 50% with only 23 people
- 99.9% with 70 people

Hashing algorithms must be carefully designed to avoid the birthday problem.

#### Cracking Passwords

Passwords are hashed, so if someone gets the file, they can't just read the passwords. If the hash function is well designed, they can't reverse the hash either. Instead, they need to guess the password, run that guess through the hash algorithm and then compare the results. There are 4 common types of password attacks. 

**Brute Force Attacks** Try all possibilities (only against short, non-complex passwords)

**Dictionary Attacks** Try English words first

**Hybrid Attacks** Add variation to tries (e.g. add a year to the end of a word, or replace o with 0)

**Rainbow Table Attacks** Precomputes hashes

Hackers often post cracked password files on public websites, just to make a public display of security vulnerabilities. Password are a common authentication mechanism, but they have serious security flaws, if they're not implemented properly. Security professionals must take care to ensure that password algorithms use strong hashing and that the files are safeguarded. When security is paramount, password should be only one component of a multi-factor authentication system.



### 3.6 Brute force cryptographic attacks

#### Brute-Force Attacks

- Repeatedly guess keys
- also called known ciphertext attacks

**Keyspace** The set of all possible encryption keys usable with an algorithm

**Modern algorithms aren't susceptible to brute-force attacks.**

#### Size of Keyspaces

- 56-bit DES: $2^{56}=7.2057594*10^{16}$ keys
- 128-bit AES: $2^{128}=3.4028237e*10^{38}$ keys
- 256-bit AEC: $2^{256}=3.4028237*10^{38}$ keys

**Flawed algorithms may be vulnerable to brute-force attacks.**

Brute-force attacks simply aren't possible against modern encryption algorithms, with one exception. If there's a flaw in the way that the encryption algorithm works that limits the size of the key space, brute-force attacks may be possible against that weak implementation of the cryptographic system.



### 3.7 Knowledge-based cryptographic attacks

Knowledge-based attacks go beyond the simplicity of brute-force attacks. And combine other information available to the attacker, with cryptanalytic techniques, to break the security of encrypted data. 

#### Frequency Analysis

- Detects patterns in ciphertext
  - The most common letters in English text are E, T, O, A, I, and N
  - The most common digraphs in English text are TH, HE, IN, and ER

#### Exam Tips

- You won't need to perform cryptanalysis on the exam - just know the different techniques

#### Known-Plaintext Attack

- Attacker has access to an unencrypted message

#### Chosen-Plaintext Attack

- Attacker can create an encrypted message of his or her choice

In this type of attack, the attacker can study the algorithm's workings in greater detail and attempt to learn the key being used. 

#### Downgrade Attack

Downgrade Attacks are possible when a system supports many different types of encryption, some of which are insecure. 

- Attacker forces two systems to use weak cryptographic implementations

In a downgrade attack, the attacker uses a man in the middle exploit, to force two other systems that attempting to communicate, to switch to a weak implementation of a cryptographic algorithm, that the attacker can eavesdrop on, and then crack. 

Example

POODLE Attack (Padding Oracle On Downgraded Legacy Encryption), in 2014. Attackers discovered that they could exploit a flaw in a software library used for encryption by many browsers, and other applications. And then force the communicating systems to switch, from the secure TLS protocol, to the insecure SSL protocol.



### 3.8 Watering hole attacks

In nature, a watering hole is a place that animals gather, particularly in dry climates. It's important that animals visit the watering hole, because the water there is essential to their survival. But, there are also significant risks involved. First, diseases can spread easily at watering holes, because all of the animals drink from a common source. Second, predators can lay and wait at the watering hole, waiting for prey to show up in need of a drink and then attack. 

#### Websites Spread Malware Effectively

- Users trust the websites they visit, to some extent
- Browsers and add-ons often have vulnerabilities
- Users are conditioned to click "OK" on security warnings

In the electronic world, websites are a great way to spread malware. Watering hole attacks are an example of a type of attack known as client-side attacks. These attacks don't necessarily exploit security issues on the server. Rather, they use malicious code and other attacks that exploit vulnerabilities in the client accessing the server. Watering hole attacks often cause popup warnings, but users are conditioned to click "OK" to security warnings to get them out of the way and move on to the content they requested. Attackers can take advantage of this by installing malware on a website and letting users come to them. 

#### Limitations

- Attackers can't just build their own sites
- Why would users visit the website
- Content filtering can block known malware sites

#### How a Watering Hole Technique Works

1. Identify and compromise a highly targeted website
2. Choose a client exploit and bundle in a botnet
3. Place the malware on the compromised website
4. Sit back and wait for infected system to phone home

Watering hole attacks are especially dangerous, because they often come from otherwise trusted websites. Attackers using this technique, making an access to highly targeted systems, and find the proverbial needle in a haystack, because the victim comes to them. Website owners and web users alike must remain current on security patches to prevent falling victim to watering hole attacks.



#### Chapter Quiz

1. What type of packet do participating systems send during a Smurf attack?

   A. ICMP information reply

   B. ICMP status check

   C. ICMP timestamp

   D. ICMP echo request

2. Which one of the following techniques is useful in preventing replay attacks?

   A. mobile device management

   B. session tokens

   C. man-in-the-middle

   D. full disk encryption

3. What attack uses carefully crafted packets that have all available option flags set to 1?

   A. DNS poisoning

   B. URL hijacking

   C. ARP poisoning

   D. Christmas tree

4. Dan is engaging in a password cracking attack where he uses precomputed hash values.  What type of attack is Dan waging?

   A. rainbow table

   B. hybrid

   C. brute force

   D. dictionary

5. What type of attack is possible when the attacker has access to both an encrypted and unencrypted version of a single message?

   A. known ciphertext

   B. chosen ciphertext

   C. known plaintext

   D. chosen plaintext

6. What type of website does the attacker use when waging a watering hole attack?

   A. site trusted by the end user

   B. software distribution site

   C. known malicious site

   D. hacker forum



Answers:

1. ICMP echo request
2. session tokens
3. Christmas tree
4. rainbow table
5. known plaintext
6. site trusted by the end user







## Reference

[1] https://www.linkedin.com/learning/comptia-security-plus-sy0-501-cert-prep-1-threats-attacks-and-vulnerabilities/