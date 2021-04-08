# CompTIA Security+ Exam (SY0-501): Identity and Access Management

This domain accounts for 16% of the questions on the real exam. We'll be focusing on:

- understanding common identity and access management concepts
- installing and configuring access and identity services
- implementing identity and access management controls
- using common account management processes



## 1. Identification

### 1.1 Identification, authentication, authorization, and accounting

#### Identification

An individual makes a claim about his or her identity. The person trying to gain access doesn't present any proof at this point. They simply make an assertion. 

#### Authentication

Proof comes into play during the authentication process. The individual proves his or her identity to the satisfaction of the access control system.

#### Authorization

Just proving your identity isn't enough to gain access to a system however. The access control system also needs to be satisfied that you are allowed to access the system. That's the third step of the access control process, authorization.

#### ! EXAM TIPS

Remember that identification and authentication are separate and distinct steps

![01_01_IAA](https://github.com/Jingy1Ma/CompTIA-Security-Exam-SY0-501/blob/main/Images/04_Identity_and_Access_Management/01_01_IAA.PNG?raw=true)

#### Triple A

- **A**uthentication
- **A**uthorization
- **A**ccounting

In addition to these processes, access control systems also provide accounting functionality that allows administrators to track user activity and reconstruct it from logs at a later date. Together, the activities of authentication, authorization, and accounting are commonly described as Triple A.



### 1.2 Identification Mechanisms

#### Usernames

- Usually easily identify the individual
- Often consist of a first initial and last name
- Should not be considered secret

Remember, usernames are for identification, not authentication, so there's no need to keep them secret. Obvious usernames make everyone's lives easier.

#### Access Cards

- Often serve as proof of employment
- May perform both identification and authentication

##### Magnetic Stripe Cards

These magnetic stripes are easily duplicated with readily available equipment, so they should not be considered secure. Anyone who gains possession of a magnetic stripe card, or even knows how the card is encoded, can create a copy of that card. 

##### Smart Cards

Contain an integrated circuit chip that works with the card reader to prove the authenticity of the card. 

Some smart cards are read by directly inserting them into a card reader. Chip and pin credit cards use similar technology. 

Contactless smart cards, or proximity cards, simply need to be placed near the reader. An antenna in the card communicates with the reader. Some of these cards, known as **passive cards**, must be placed into or extremely close to the reader to work properly. They receive power from the reader that energizes the chip, so they last indefinitely. Other proximity cards, known as **active cards**, contain batteries and transmitters. They use these batteries and can then transmit over longer distances and be read from several feet away. Toll transponders use this technology. The **disadvantage to active cards** is that they contain batteries and must be replaced periodically. 



### 1.3 Biometrics

**Something You Are**

- Identification and Authentication

#### Good Biometric Systems Provide

- Easy enrollment
- Low false acceptance rates
- Lose false rejection rates
- Low intrusiveness

##### Fingerprint Scans

- Often found on computing devices
- Allow self-enrollment
- Low false rejection and acceptance rates

##### Eye Scans

- Analyze
  - Color pattern of iris
  - Blood vessel of retina
- Seen as highly intrusive by users

Not commonly used outside of high-security physical buildings.

##### Voiceprint Matching

- Requires user to speak a phrase
- Subject to reply attacks
- Often combined with other authentication techniques

##### Facial Recognition

- Scans user's facial structure
- Has a high “creepiness factor"
- Improving error rates

As authentication tools, biometrics are much harder to fool than passwords and other knowledge-based approaches.



### Chapter Quiz

1. During what phase of the access control process does a user prove his or her identity?

   A. identification

   B. authorization

   C. remediation

   D. authentication

2. Which one of the following access control cards is the easiest to duplicate without permission?

   A. active card

   B. proximity card

   C. smart card

   D. magnetic stripe card

3. What characteristic of biometrics measures the frequency at which legitimate users are denied access to a system or facility?

   A. intrusiveness factor

   B. false rejection rate

   C. false acceptance rate

   D. enrollment reliability



Answers:

1. authentication
2. magnetic stripe card
3. false rejection rate



## Reference

[1] https://www.linkedin.com/learning/comptia-security-plus-sy0-501-cert-prep-4-identity-and-access-management/
