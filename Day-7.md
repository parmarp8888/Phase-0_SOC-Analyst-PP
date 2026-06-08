
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

---
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

| Security | Goal	Attack |
|----------|-------------|
|Confidentiality |	Disclosure|
|Integrity	| Alteration|
|Availability |	Destruction / Denial|

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
One security control is never enough.

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
**9. ISO/IEC 19249 Questions Explained**
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
