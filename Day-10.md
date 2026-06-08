
# Room Walkthrough:[ Cyber Kill Chain](https://tryhackme.com/room/cyberkillchainzmt)

## 🎯 Day 10 Objective

As part of my SOC Analyst L1 learning journey, this room introduced me to one of the most important attack analysis frameworks in cybersecurity:

> "How does an attacker move from gathering information to achieving their objective inside a target environment?"

Before this room, I mostly viewed cyber attacks as a single event. After completing it, I learned that attacks are usually a series of connected stages, and defenders can stop an attack by disrupting any one of those stages.

---

### Who is this for?

* SOC Analysts
* Incident Responders
* Threat Hunters
* Security Researchers
* Blue Team Professionals

### What is Cyber Kill Chain?

The Cyber Kill Chain is a framework developed to understand how attackers plan, execute, and complete cyber attacks.

It breaks an intrusion into seven stages:

1. Reconnaissance
2. Weaponization
3. Delivery
4. Exploitation
5. Installation
6. Command & Control (C2)
7. Actions on Objectives

### Where does this apply?

* Security Operations Centers (SOC)
* Enterprise Networks
* Incident Response Investigations
* Threat Hunting Activities
* Malware Analysis

### When should it be learned?

Before advanced threat detection and incident response because it helps analysts understand the attack lifecycle.

### Why is it important?

If defenders can identify which stage an attacker is in, they can stop the attack before business damage occurs.

### How does it work?

The framework maps attacker behavior from initial information gathering to the final objective, helping defenders recognize and break the attack chain.

---

### What confused me?

Initially, I thought malware infection was the beginning of an attack.

My confusion was:

* What happens before malware reaches the victim?
* Why do attackers spend time gathering information first?
* How are phishing emails connected to exploitation?
* Why does an attacker need persistence after gaining access?

After studying the Cyber Kill Chain, I realized that malware is often only one step in a larger attack process.

### What I learned?

Key lessons from this room:

* Cyber attacks follow a structured lifecycle.
* Reconnaissance helps attackers identify targets.
* Weaponization combines malware and exploits into a usable payload.
* Delivery methods determine how malware reaches victims.
* Exploitation abuses vulnerabilities or user actions.
* Installation establishes persistence.
* Command & Control allows remote communication.
* Actions on Objectives represent the attacker's final goal.

I also learned that the traditional Cyber Kill Chain has limitations and cannot effectively identify Insider Threats.

### How I improved?

Before this room, I focused mainly on the malware itself.

Now I understand that defenders should identify attack activity much earlier.

My thinking changed from:

> "How do we remove malware?"

to

> "Which stage of the attack lifecycle can we detect and stop first?"

### Real-World Relevance

In a real enterprise:

* Phishing campaigns represent Delivery.
* Exploiting vulnerabilities represents Exploitation.
* Registry persistence represents Installation.
* Beaconing traffic represents Command & Control.
* Data theft represents Actions on Objectives.

SOC teams monitor logs, endpoints, DNS activity, and network traffic to identify these stages before attackers achieve their objectives.

---

## Task 1: Kill chain
The term kill chain is a military concept related to the structure of an attack. It consists of target identification, decision and order to attack the target, and finally the target destruction.

<img width="1098" height="1280" alt="image" src="https://github.com/user-attachments/assets/3597b548-02cb-42d9-a86a-4bd2e328ecda" />

Thanks to Lockheed Martin, a global security and aerospace company, that established the Cyber Kill Chain® framework for the cybersecurity industry in 2011 based on the military concept. The framework defines the steps used by adversaries or malicious actors in cyberspace. To succeed, an adversary needs to go through all phases of the Kill Chain. We will go through the attack phases and help you better understand adversaries and their techniques used in the attack to defend yourself.

So, why is it important to understand how Cyber Kill Chain works?

The Cyber Kill Chain will help you understand and protect against ransomware attacks, security breaches as well as Advanced Persistent Threats (APTs). You can use the Cyber Kill Chain to assess your network and system security by identifying missing security controls and closing certain security gaps based on your company's infrastructure.

By understanding the Kill Chain as a SOC Analyst, Security Researcher, Threat Hunter, or Incident Responder, you will be able to recognize the intrusion attempts and understand the intruder's goals and objectives. 

We will be exploring the following attack phases in this room:

Reconnaissance
Weaponization
Delivery
Exploitation
Installation
Command & Control
Actions on Objectives
Learning Objectives
In this room, you will learn about each phase of the Cyber Kill Chain Framework, the advantages and disadvantages of the traditional Cyber Kill Chain. 

**Outcome**
As a result, you will be ready to recognize different phases or stages of the attack carried out by an adversary and be able to break the "kill chain."          

### Task 2: Reconnaissance
<img width="452" height="332" alt="image" src="https://github.com/user-attachments/assets/ef46c4a1-096b-41af-8003-c1ec04dbf75e" />
A valuable piece of recon is **OSINT (Open-Source Intelligence).** With OSINT, adversaries gather insights about their target through publicly available information. Some public sources where OSINT data can be collected from include:

Search engines
Print and online media
Social media accounts
Online forums and blogs
Online public record databases
WHOIS and technical data
Find out more about OSINT from this Varonis article, "What is OSINT?"(opens in new tab)

### Reconnaissance Types
**Passive Recon:** This involves having no direct interaction with the target. This may include WHOIS lookups, social media scraping, or reviewing breach data.

**Active Recon:** This involves direct contact with the target with activities such as social engineering, port scanning, banner grabbing, or probing for open services.

**Email harvesting** is the process of obtaining email addresses from public, paid, or free services.
 Here are some of them:

[theHarvester](https://github.com/laramies/theHarvester): other than gathering emails, this tool is also capable of gathering names, subdomains, IPs, and URLs using multiple public data sources.

[Hunter.io](https://hunter.io/): this is an email hunting tool that will let you obtain contact information associated with the domain.

[OSINT Framework](https://osintframework.com/): OSINT Framework provides the collection of OSINT tools based on various categories.
**Question:** What is the name of the Intel Gathering Tool that is a web-based interface to common OSINT resources?

**Answer:** OSINT Framework

**Explanation:**
OSINT Framework helps analysts gather publicly available information about targets during reconnaissance.

**Question:** What is the definition for the email gathering process during reconnaissance?

**Answer:** Email Harvesting

**Explanation:**
Attackers collect email addresses to prepare phishing campaigns or social engineering attacks.

---

### Task 3: Weaponization
After gathering information, attackers create malware or malicious payloads to exploit identified weaknesses. This process can include designing new malware forms or modifying existing programs to match specific vulnerabilities.
**Question:** What is the term for automated scripts embedded in Microsoft Office documents?

**Answer:** Macro

**Explanation:**
Macros automate tasks but can also be abused to execute malicious code when a victim opens a document.

---

### Task 4: Delivery
Attackers attempt to infiltrate the target's network by delivering malware. Common methods include sending phishing emails, using social engineering tools, and exploiting hardware or software vulnerabilities.
**Question:** What do you call an attack targeting a specific group by infecting their frequently visited website?

**Answer:** Watering Hole Attack

**Explanation:**
Attackers compromise trusted websites and wait for intended victims to visit them.

---

### Task 5: Exploitation
Once the malware is delivered, attackers exploit the target's vulnerabilities, further infiltrating the network. They often move laterally across systems, identifying more potential entry points and weaknesses.
**Question:** What is the term for a cyber attack that exploits an unknown software vulnerability?

**Answer:** Zero-Day

**Explanation:**
A Zero-Day vulnerability is unknown to the vendor and usually has no available patch when first exploited.

---

### Task 6: Installation
In this phase, attackers install malware to gain additional control over the network. Strategies include using Trojan horses, access token manipulation, command-line interfaces, and backdoors to escalate privileges and change permissions.

**Question:** What technique is used to modify file timestamps to hide malicious activity?

**Answer:** Timestomping

**Explanation:**
Attackers alter file timestamps to make malicious files appear legitimate.

**Question:** What malicious script can be planted on a web server to maintain access?

**Answer:** Web Shell

**Explanation:**
A web shell provides attackers with persistent remote access to compromised web servers.

---

### Task 7: Command & Control
Attackers establish a command and control (C2) channel to remotely monitor and guide their deployed cyberweapons. They use obfuscation techniques to cover their tracks and denial of service (DoS) tactics to distract security teams from the core objectives of the attack.

**Question:** What C2 communication method uses repeated DNS requests to attacker-controlled infrastructure?

**Answer:** DNS Tunneling

**Explanation:**
DNS traffic often appears legitimate, making it useful for hiding attacker communications.

---

### Task 8: Actions on Objectives
After going through six phases of the attack, Megatron can finally achieve his goals, which means taking action on the original objectives. With hands-on keyboard access, the attacker can achieve the following: 

* Collect the credentials from users.

* Perform privilege escalation (gaining elevated access like domain administrator access from a workstation by exploiting the misconfiguration).

* Internal reconnaissance (for example, an attacker gets to interact with internal software to find its vulnerabilities).

* Lateral movement through the company's environment.

* Collect and exfiltrate sensitive data.

* Deleting the backups and shadow copies. Shadow Copy is a Microsoft technology that can create backup copies, snapshots of computer files, or volumes. 

* Overwrite or corrupt data.

**Question:** What Microsoft technology creates backup copies or snapshots of files and volumes?

**Answer:** Shadow Copy

**Explanation:**
Attackers often delete Shadow Copies to prevent recovery after ransomware attacks.

---

### Task 9: Practice Analysis
<img width="892" height="800" alt="image" src="https://github.com/user-attachments/assets/e8db9d15-2c82-4d64-bbbe-0e9379d6f1ee" />
**Here is the real-world scenario for you to tackle:**

The infamous Target cyber-attack, which led to one of the largest data breaches in history took place on November 27, 2013.

On December 19th, 2013, Target released a statement(opens in new tab) confirming the breach, stating that approximately 40 million credit and debit card accounts were impacted between Nov. 27 and Dec. 15, 2013. Target had to pay the fine of $18.5 million under the terms of the multistate settlement agreement(opens in new tab). This is considered to be the largest data-breach settlement in history.

How did the data breach happen? Deploy the static site attached to this task and apply your skills to build the Cyber Kill Chain of this scenario. Here are some tips to help you complete the practical:

1. Add each item on the list in the correct Kill Chain entry-form on the Static Site Lab:

exploit public-facing application
data from local system
powershell
dynamic linker hijacking
spearphishing attachment
fallback channels

2. Use the ‘Check answers’ button to verify whether the answers are correct (where wrong answers will be underlined in red).
**Question:** What was the final flag?

**Answer:** THM{7HR347_1N73L_12_4w35om3}

**Explanation:**
This practical exercise required mapping attacker actions to the appropriate Cyber Kill Chain stages to understand how the breach occurred.

---

## 🛡️ SOC Analyst L1: Mindset

### Tricky Connection

Many beginners study attacks by asking:

> "How was the system hacked?"

A SOC Analyst asks:

> "Which stage of the attack chain generated detectable evidence?"

For example:

* Suspicious DNS traffic → Command & Control
* Phishing email → Delivery
* Privilege escalation logs → Exploitation
* Data transfer spikes → Exfiltration

The objective is not only to understand attacks but to identify where defenders can interrupt them.

### Next Learning Steps

To strengthen this foundation, I should continue learning:

1. MITRE ATT&CK Framework
2. Unified Kill Chain
3. Windows Event Logs
4. DNS Analysis
5. Network Traffic Analysis
6. Persistence Mechanisms
7. Threat Hunting Fundamentals

---

## Critical Thinking

### Question

A user reports opening a suspicious Microsoft Word attachment received through email. Shortly afterward, endpoint logs show a new PowerShell process, unusual DNS requests, and outbound traffic to an unknown domain.

Which Cyber Kill Chain stages are visible, and how would you investigate?

### Answer Concept

My investigation approach would be:

1. Analyze the email and attachment.
2. Identify whether a malicious macro executed.
3. Review PowerShell logs and process creation events.
4. Investigate DNS requests for signs of DNS tunneling or beaconing.
5. Check endpoint persistence mechanisms.
6. Determine whether data exfiltration occurred.
7. Isolate affected systems and escalate if necessary.

Based on available evidence:

* Email Attachment → Delivery
* Macro Execution → Exploitation
* Persistence Activity → Installation
* DNS Requests → Command & Control

The goal is to determine how far the attacker progressed through the Kill Chain and stop the intrusion before business impact occurs.

---

## Final Reflection

This room taught me that cyber attacks are rarely random events. They are usually a sequence of planned actions designed to achieve a specific objective.

As an aspiring SOC Analyst L1, understanding the Cyber Kill Chain helps me analyze attacks systematically, identify detection opportunities, and understand where security controls can interrupt an intrusion. It also showed me why defenders should not rely solely on the traditional Cyber Kill Chain and should complement it with frameworks such as MITRE ATT&CK and the Unified Kill Chain for broader visibility.
