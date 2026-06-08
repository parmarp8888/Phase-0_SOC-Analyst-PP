# Room Walkthrough:[ Security Principles](https://tryhackme.com/room/securityprinciples)
## 🎯 Day 7 Objective

As part of my SOC Analyst L1 learning journey, this room introduced me to the fundamental principles that guide security decisions across organizations.

Before starting this room, I knew security involved protecting systems and data, but I was unsure how organizations determine what to protect first, how security controls are designed, and why certain security models exist.
<img width="1140" height="694" alt="image" src="https://github.com/user-attachments/assets/0421fad0-79c4-4ebb-9fbb-4b584e45bf0f" />

The objective of this room is to:
. Explain the security functions: Confidentiality, Integrity and Availability (CIA).

. Present the opposite of the security triad, CIA: Disclosure, Alteration, and                     Destruction/Denial (DAD).

. Introduce the fundamental concepts of security models, such as the Bell-LaPadula model.

. Explain security principles such as Defence-in-Depth, Zero Trust, and Trust but Verify.

. Introduce ISO/IEC 19249.

. Explain the difference between Vulnerability, Threat, and Risk.

---

### Who is this for?

* SOC Analysts
* Security Engineers
* System Administrators
* Risk and Compliance Teams
* Anyone beginning a cybersecurity career

### What is it?

An introductory room that explains the core principles of information security, including the CIA Triad, security models, and fundamental concepts used to protect organizational assets.

### Where does this apply?

* Enterprise networks
* Cloud environments
* Government organizations
* Financial institutions
* Healthcare systems
* Security Operations Centers (SOC)

### When should I learn this?

At the beginning of a cybersecurity journey before learning threat detection, incident response, SIEM tools, or advanced security technologies.

### Why is it important?

Security principles provide the foundation for understanding why security controls exist and how organizations make security decisions.

Without understanding these principles, it becomes difficult to analyze threats, assess risk, or understand the purpose behind security technologies.

### How does it work?

Security principles define objectives that organizations aim to achieve when protecting information.

The room focused on:

* CIA Triad
* Defense in Depth
* Principle of Least Privilege
* Separation of Duties
* Security Models
* Risk Reduction Concepts

These principles guide how systems, users, and security controls interact within an organization.

---

### What confused me?

My biggest confusion was understanding why security professionals constantly refer to the CIA Triad.

Questions that came to mind included:

* Why are Confidentiality, Integrity, and Availability considered the foundation of security?
* Can a security incident affect more than one part of the CIA Triad?
* Why do organizations use multiple security controls instead of a single strong control?
* What is the practical difference between Least Privilege and Separation of Duties?

Initially, these concepts felt theoretical, and I struggled to connect them to real security operations.

### What I learned?

This room taught me several important security concepts:

#### CIA Triad
<img width="1140" height="694" alt="image" src="https://github.com/user-attachments/assets/f24f7d31-fed8-460f-8b31-ddce6d737673" />

* **Confidentiality** → Prevent unauthorized access to information.
* **Integrity** → Ensure information remains accurate and trustworthy.
* **Availability** → Ensure systems and information remain accessible when needed.

#### Defense in Depth

Security should not rely on a single protective control.

<img width="1140" height="694" alt="image" src="https://github.com/user-attachments/assets/9d0b6f0a-8a63-4937-bdf6-83b94435f38e" />

Organizations implement multiple layers such as:

* Firewalls
* Endpoint Security
* Access Controls
* Monitoring Solutions
* Security Awareness Training

#### Principle of Least Privilege
[<img width="1275" height="915" alt="image" src="https://github.com/user-attachments/assets/66c1aa48-c32a-4192-aed3-05215dcd4caa" />](https://blog.sucuri.net/2024/01/what-is-the-principle-of-least-privilege.html)

Users should only receive the permissions required to perform their job responsibilities.

#### Separation of Duties
[<img width="1473" height="710" alt="image" src="https://github.com/user-attachments/assets/daa2ece4-cc58-483c-b4a0-198d4f65e71d" />](https://www.safepaas.com/articles/what-are-some-common-examples-of-segregation-of-duties/)

Critical actions should be divided among multiple individuals to reduce risk and prevent abuse.

#### Security Models
[<img width="1581" height="1774" alt="image" src="https://github.com/user-attachments/assets/a06aba3a-06c2-4b36-bed4-26ee582e9ada" />](https://sprinto.com/blog/types-of-security-models/)

Security models provide structured methods for enforcing security policies and protecting information.

### How I improved?

Before this room, I viewed security controls as individual tools.

After completing it, I began understanding security as a framework of principles that influence every security decision.

My thinking changed from:

> "What security tool should we deploy?"

to

> "What security objective are we trying to achieve?"

This perspective helped me understand why organizations implement multiple layers of security rather than relying on a single defense mechanism.

### Real-World Relevance

In a real organization:

* HR records require confidentiality.
* Financial transactions require integrity.
* Critical business applications require availability.

Organizations use Defense in Depth to protect these assets through multiple security layers.

For example:

A VPN protects remote access.

Multi-Factor Authentication protects user accounts.

Endpoint Detection and Response (EDR) protects endpoints.

SIEM platforms monitor security events.

Each control contributes to protecting one or more elements of the CIA Triad.

This is why security principles directly influence enterprise security architecture and daily SOC operations.

---

## 🛡️ SOC Analyst L1: Mindset

### Tricky Connection

A beginner often focuses on:

> "How was the system attacked?"

A SOC Analyst focuses on:

> "Which security objective was impacted and what evidence supports it?"

For example:

* A phishing attack may impact Confidentiality if credentials are stolen.
* A ransomware attack may impact Availability if systems become inaccessible.
* Unauthorized database modifications may impact Integrity.

Understanding the CIA Triad helps transform alerts into meaningful business-impact investigations.

Instead of only investigating technical indicators, a SOC Analyst learns to evaluate:

* Business impact
* Data exposure
* Operational disruption
* Risk severity

This is the mindset shift from learning attacks to understanding protection objectives.

### Next Learning Steps

To strengthen this foundation, I should continue learning:
1. Networking Fundamentals
2. Windows Event Logs
3. Linux Logging
4. SIEM Fundamentals
5. Incident Response Basics

These topics build directly upon the security principles introduced in this room.

---

## Critical Thinking

### Question
A company's customer portal remains online and accessible, but an investigation reveals that several customer account records were modified without authorization.

As a SOC Analyst L1, which security principle has been affected, and how would you approach the investigation?

### Answer Concept
The primary security principle affected is **Integrity** because information has been altered without authorization.

My investigation approach would include:

1. Identify the affected records and determine the scope of modification.
2. Review authentication and access logs to identify who performed the changes.
3. Establish a timeline of events.
4. Verify whether the activity was authorized or expected.
5. Check for compromised user accounts or privilege misuse.
6. Review related alerts from monitoring tools and SIEM platforms.
7. Escalate findings according to incident response procedures.
8. Document evidence and actions taken.

Although the portal remains available and there is no indication of data theft, the trustworthiness and accuracy of the data have been compromised.

A strong SOC Analyst focuses not only on technical indicators but also on understanding which security objective has been affected and how it impacts the business.

---
###

**1. What Does "Secure" Actually Mean?**
Most beginners answer:
"A secure system is one that cannot be hacked."

This is incorrect.
No system is 100% secure.
A better definition is:
  A secure system protects information and services from unauthorized access, modification, or    disruption while allowing legitimate users to perform their work.

Notice something important:
Security is not about blocking everyone.
Security is about balancing protection and business operations.

Example:
A bank website that nobody can access is secure from attackers.
But it is useless for customers.
Therefore it has failed security because Availability is broken.

---

**2. CIA Triad (Most Important Topic)**
Everything in cybersecurity eventually comes back to CIA.
<img width="550" height="500" alt="image" src="https://github.com/user-attachments/assets/6eeb8bc3-596f-4d04-85f2-d9748d4ff598" />

**Confidentiality**
Goal:
Prevent unauthorized access to information.

Examples:
Passwords
Medical records
Credit card numbers
Employee salary data

**Security Controls:**
Encryption
MFA
Access Control
VPN
Permissions
SOC Analyst Perspective:
If an attacker steals a database:
Confidentiality has failed.

Example:
Customer database leaked online.

Impact:
Privacy violations
Reputation damage
Regulatory fines

---
**Integrity**
Goal:
Ensure data remains accurate and unmodified.
Many beginners think:
"If data still exists, everything is fine."
Not true.
Incorrect data can be more dangerous than deleted data.

Example:
Bank balance:
Actual: ₹50,000
Modified: ₹5,00,000
Data exists.
But integrity is broken.

**Security Controls:**
Hashing
Digital Signatures
Checksums
File Integrity Monitoring
SOC Analyst Perspective:

Questions:
Who changed the file?
When was it changed?
Was it authorized?
Availability

Goal:
Ensure systems and data are accessible when needed.

Examples:
ATM services
Email systems
Cloud applications

**Security Controls:**
Backups
Redundancy
Load Balancers
Disaster Recovery

SOC Analyst Perspective:
. A system doesn't need to be hacked to fail availability.
. Power failure can cause availability issues.
. Hardware failure can cause availability issues.
. DDoS attacks can cause availability issues.

**Easy Memory Trick**
  Think of Online Banking.

**Confidentiality:**
Nobody else should see my account.

**Integrity:**
 Nobody should change my balance.

**Availability:**
 I should be able to access it anytime.

---
**3. Authenticity**
Many people skip this concept.

Big mistake.
Authenticity answers:
Is this really from who it claims to be from?

Example:
Email says:
"Your CEO sent this."

Question:
Did the CEO actually send it?
If yes → Authentic.
If attacker spoofed it → Not Authentic.

SOC Relevance:
Phishing investigations often focus on authenticity.

---
**4. Nonrepudiation**
Fancy word.
Simple meaning:
Someone cannot deny performing an action.

Example:
Employee digitally signs a contract.

Later they say:      "I never signed it."

Digital signature proves they did.

Therefore:
Nonrepudiation exists.

Used heavily in:
Banking
E-commerce
Legal systems
Healthcare

---
**5. Parkerian Hexad**
CIA is not the only security model.
**Parker added:**
1.Confidentiality
2.Integrity
3.Availability
4.Authenticity
5.Utility
6.Possession

---
**Utility**
Question:
Can the information actually be used?

Example:
Encrypted drive exists.
Data exists.
But decryption key is lost.
Availability exists.
Data still exists.
But usefulness is gone.
Utility is lost.

**Possession**
Question:
Who controls the information?

Example:
Attacker steals company backup drive.
Data isn't leaked yet.
Integrity intact.
Confidentiality intact.
But company lost possession.
This is why possession matters.

---
**6. DAD Triad**
DAD is simply CIA viewed from the attacker's perspective.
<img width="1409" height="1348" alt="WhatsApp Image 2026-06-08 at 11 15 40" src="https://github.com/user-attachments/assets/e533f5d0-4c41-4183-b945-0452d764c8e5" />

| Security | Goal	Attack |
|----------|-------------|
|Confidentiality |	Disclosure|
|Integrity	| Alteration|
|Availability |	Destruction / Denial|

[<img width="800" height="800" alt="image" src="https://github.com/user-attachments/assets/11892f94-c7fc-4a95-941e-955a56b414c2" />
](https://medium.com/@tarundevrani281993/the-cia-and-dad-triads-in-cybersecurity-3dc802036fe5)
---
Why Was "Disclosure" Correct?
Question:
Customer records dumped online.
**Think:**
What happened?
Attackers exposed confidential information.

Therefore:
Confidentiality broken.

**Attack type:**
Disclosure
Not alteration.
Not destruction.
No evidence data changed.
No evidence service stopped.

---
**Why Was "Destruction/Denial" Correct?**

Question:
Main power and backup power shut down.
Network stopped working.

What failed?
Availability.
Systems unavailable.

**Attack type:**
Destruction/Denial
This is exactly opposite of Availability.

---
**7. Security Models**
Most students memorize names and move on.
Instead understand:
Security models answer:
"How should access be controlled?"
Bell-LaPadula Model

Focus:
Confidentiality

Rule:
. No Read Up
 Low-level user cannot read higher classified data.
. No Write Down
 High-level user cannot write sensitive data to lower classifications.

Military Example:
**Confidential → Secret → Top Secret**

Purpose:
.Prevent information leakage.
.Biba Model

Focus:
Integrity
Opposite of Bell-LaPadula.

Rule:
. No Read Down
. Avoid reading untrusted data.
. No Write Up
. Avoid contaminating higher integrity data.

Purpose:
.Protect accuracy.
.Clark-Wilson Model

Focus:
Business Integrity

Uses:
.Auditing
.Separation of Duties
.Transactions

Example:
. One employee creates payment.
. Another approves payment.

Purpose:
Reduce fraud.

---
**8. Defence-in-Depth**
One security control is never enough,Defence-in-Depth refers to creating a security system of multiple levels; hence it is also called Multi-Level Security.

[<img width="434" height="322" alt="image" src="https://github.com/user-attachments/assets/a43ae0df-f98d-4b03-8d20-7a68d892b527" />
](https://medium.com/insa-tc/defense-in-depth-for-web-applications-38178696f833)

Example:
. Only antivirus installed.
. Attacker bypasses antivirus.
. Game over.
. Instead use layers.

Layer 1:
Firewall

Layer 2:
MFA

Layer 3:
EDR

Layer 4:
SIEM

Layer 5:
Security Awareness

Layer 6:
Incident Response

Attacker must defeat all layers.
SOC analysts work as one layer of Defence-in-Depth.

---
**9. ISO/IEC 19249 Questions Explained**[<img width="1280" height="644" alt="image" src="https://github.com/user-attachments/assets/f94c1124-1658-49ca-965a-efd1deb5891a" />
](https://www.iso.org/standard/64140.html)
The International Organization for Standardization (ISO) and the International Electrotechnical Commission (IEC) have created the ISO/IEC 19249. In this task, we will brush briefly upon ISO/IEC 19249:2017 Information technology - Security techniques - Catalogue of architectural and design principles for secure products, systems and applications.
Question 1
Turn off insecure server not critical to business.
Answer: Principle 2

**Reason:**
.Reduce unnecessary attack surface.
.Less software.
.Less exposure.
.Less risk.

---
Question 2
New sales representative only gets product and pricing access.
Answer: Principle 1

**Reason:**
.Least Privilege.
.Give only required permissions.
.Nothing extra.
.SOC analysts constantly verify this.

---
Question 3
ATM handles network failure and power failure.
Answer: Principle 5

**Reason:**
.Prepare for secure failure.
.Systems should fail safely.
.Not crash unpredictably.

---
**10. Trust But Verify vs Zero Trust**

This topic is becoming increasingly important.

**Trust But Verify**
Old mindset.

Example:
. Employee connects from company network.
. System trusts them.
. Verification occurs later.

**Idea:**
""Trust first, verify afterwards.""

---
**Zero Trust**
Modern mindset.
Assume nobody is trusted.
Verification required every time.
**Check:**
.Identity
.Device
.Location
.Risk

**Idea:**
  ""Never trust. Always verify.""

SOC Relevance:
Most modern enterprises are moving toward Zero Trust architectures.

---
**11. Vulnerability vs Threat vs Risk**
Most interview candidates confuse these.

**Vulnerability**
 Vulnerable means susceptible to attack or damage. In information security, a vulnerability is a weakness.
Example:
. Outdated Windows server.
. Weak password.
. Open port.
. Misconfiguration.

**Threat**
 A threat is a potential danger associated with this weakness or vulnerability.
Example:
. Ransomware group.
. Attacker.
. Malware.
. Insider threat.

**Risk**
The risk is concerned with the likelihood of a threat actor exploiting a vulnerability and the consequent impact on the business(Likelihood + Impact).
Example:
. Internet-facing server
. Critical vulnerability
. Active attackers = High Risk

**Simple Formula = Risk ≈ Likelihood × Impact**
<img width="346" height="146" alt="image" src="https://github.com/user-attachments/assets/99ff1d45-b86a-467f-97ff-64a0e54219ea" />

---
**SOC Analyst L1**
When you investigate an alert, always ask:
### Which CIA component is affected?
Examples:
| Incident                  | CIA Impact                 |
| ------------------------- | -------------------------- |
| Database leak             | Confidentiality            |
| File tampering            | Integrity                  |
| DDoS attack               | Availability               |
| Phishing email            | Confidentiality (possible) |
| Ransomware                | Availability + Integrity   |
| Credential theft          | Confidentiality            |
| Unauthorized admin change | Integrity                  |

###

## Final Reflection

This room helped me understand that cybersecurity is built on foundational principles rather than individual tools.

My biggest takeaway was realizing that nearly every security incident can be analyzed through the lens of Confidentiality, Integrity, and Availability.

As an aspiring SOC Analyst L1, understanding these principles gives me a stronger foundation for future topics such as threat detection, log analysis, SIEM monitoring, incident response, and risk assessment.

Going forward, I will view security alerts not only as technical events but also as potential threats to the organization's information, operations, and business objectives.
