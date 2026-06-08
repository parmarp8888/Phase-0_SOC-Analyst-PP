# Room Walkthrough: [Unified Kill Chain ](https://tryhackme.com/room/unifiedkillchain) & [Pyramid Of Pain](https://tryhackme.com/room/pyramidofpainax)

## 🎯 Day 11 Objective
<img width="1739" height="878" alt="image" src="https://github.com/user-attachments/assets/e5075e58-701f-40f5-b437-c1a46f661272" />

As part of my SOC Analyst L1 learning journey, this room helped me understand two important concepts used by security teams:

> How attackers move through an environment to achieve their objectives.

and

> How defenders can make attacks more difficult by detecting indicators that are harder for attackers to change.

Before this room, I mostly focused on individual attacks and tools. After completing it, I began seeing cyber attacks as a sequence of connected actions rather than isolated events.

The room introduced the **Unified Kill Chain (UKC)** and the **Pyramid of Pain**, two frameworks that help security teams understand attacker behavior, improve detection capabilities, and strengthen defensive strategies.

---

## Who is this for?

* SOC Analysts
* Threat Hunters
* Incident Responders
* Security Engineers
* Digital Forensics Analysts
* Anyone learning attacker methodologies

## What is it?

### Unified Kill Chain (UKC)
[<img width="409" height="123" alt="image" src="https://github.com/user-attachments/assets/50b2b5b3-e9ff-4e75-85b3-0705faefa77e" />](https://medium.com/@AbhijeetSingh4/cyber-kill-chain-soc-level-1-tryhackme-walkthrough-ac77efd6425a)

A cybersecurity framework published by Paul Pols in 2017 that breaks an attack into 18 different phases.

It helps defenders understand:

* How attacks start
* How attackers gain access
* How they move through networks
* How they achieve their objectives

### Pyramid of Pain
[<img width="720" height="405" alt="image" src="https://github.com/user-attachments/assets/63fdd55b-c918-4d64-91bb-dcb483103417" />](https://www.splunk.com/en_us/blog/learn/ioc-indicators-of-compromise.html)

A threat intelligence model created by David Bianco.

It ranks indicators based on how difficult they are for attackers to change.

The higher up the pyramid defenders can detect, the more disruption they cause to attackers.

## Where does this apply?

* Security Operations Centers (SOC)
* Incident Response Teams
* Threat Hunting Programs
* Enterprise Networks
* Cyber Threat Intelligence Teams

## When should it be learned?

After learning:

* Basic Networking
* Security Awareness
* Cyber Threat Actors
* CIA Triad
* Fundamental Security Concepts

## Why is it important?

Without frameworks, defenders often focus only on alerts.

These frameworks help answer questions such as:

* What stage is the attacker currently in?
* What is the attacker's objective?
* How can we stop the attack earlier?
* Which indicators provide the strongest detection value?

## How does it work?

The Unified Kill Chain maps the attack lifecycle.

The Pyramid of Pain prioritizes detection opportunities.

Together they help defenders understand:

> What the attacker is doing and how painful it would be for them if we detected it.

---

## What confused me?

Initially, I thought the Unified Kill Chain was simply another version of MITRE ATT&CK.

My confusion included:

* Why do multiple frameworks exist?
* What is the difference between UKC and MITRE?
* What exactly is pivoting?
* Why is detecting a hash considered weak while detecting TTPs is considered strong?

The Pyramid of Pain was especially confusing because I assumed every indicator had equal value.

After studying the examples, I understood that some indicators are extremely easy for attackers to replace, while others require significant effort, time, and resources.

## What I learned?

Key lessons from this room:

### Unified Kill Chain
Understanding the behaviours, objectives and methodologies of a cyber threat is a vital step to establishing a strong cybersecurity defence (known as a cybersecurity posture).
I learned the three major attack goals:

**Goal: In (Initial Foothold)**

* Reconnaissance
* Weaponization
* Social Engineering
* Exploitation
* Persistence
* Defense Evasion
* Command & Control
* Pivoting

**Goal: Through (Network Propagation)**

* Discovery
* Privilege Escalation
* Execution
* Credential Access
* Lateral Movement

**Goal: Out (Action on Objectives)**

* Collection
* Exfiltration
* Impact
* Objectives

### Pyramid of Pain
This well-renowned concept is being applied to cybersecurity solutions like Cisco Security(opens in new tab), SentinelOne(opens in new tab), and SOCRadar(opens in new tab) to improve the effectiveness of CTI (Cyber Threat Intelligence), threat hunting, and incident response exercises.

Understanding the Pyramid of Pain concept as a Threat Hunter, Incident Responder, or SOC Analyst is important.
I learned the hierarchy of indicators:

1. Hash Values (Trivial)
2. IP Addresses (Easy)
3. Domain Names (Simple)
4. Host Artifacts (Annoying)
5. Network Artifacts (Annoying)
6. Tools (Challenging)
7. TTPs (Tough)

The higher defenders detect on this pyramid, the more difficult recovery becomes for attackers.

## How I improved?

Before this room, I mainly looked at security alerts individually.

Now I ask:

> Which phase of the attack does this activity belong to?

Instead of seeing:

* A suspicious login
* A malware alert
* A data transfer event

I now see potential stages within a larger attack chain.

This has improved my analytical thinking because I can connect events together rather than investigating them in isolation.

## Real-World Relevance

In a real enterprise:

* Reconnaissance may appear as scanning activity.
* Credential Access may appear as Mimikatz execution.
* Lateral Movement may appear as unusual authentication activity.
* Exfiltration may appear as large outbound data transfers.

SOC analysts use frameworks like UKC to understand where an attacker is in the attack lifecycle.

The Pyramid of Pain helps defenders prioritize detections that have long-term value instead of relying only on simple indicators.

---

## Unified Kill Chain
<img width="711" height="334" alt="image" src="https://github.com/user-attachments/assets/9d43378d-3f07-47e6-8150-d24f81422887" />

### Task 2 – What is a Kill Chain?
Originating from the military, a “Kill Chain” is a term used to explain the various stages of an attack. In the realm of cybersecurity, a “Kill Chain” is used to describe the methodology/path attackers such as hackers or APTs use to approach and intrude a target.

**Question:** Where does the term "Kill Chain" originate from?

**Answer:** Military
<img width="50%" height="50%" alt="image" src="https://github.com/user-attachments/assets/0e284662-67e5-4957-a73b-cb6dd5faa3c2" />

**Key Takeaway:**

The concept originated in military operations and was adapted to cybersecurity to describe attack stages.

---

### Task 3 – Threat Modelling
Threat modelling, in a cybersecurity context, is a series of steps to ultimately improve the security of a system. 
<img align="right" width="230" height="270" alt="image" src="https://github.com/user-attachments/assets/05a7edd4-e5df-4bc6-a38a-5b9a910d8b2b" />

**Question:** What is the technical term for a piece of software or hardware?

**Answer:** Asset

**Key Takeaway:**

Security starts by identifying and protecting assets.

---

### Task 4 – Introducing the Unified Kill Chain
To continue from the previous task, Paul Pols' Unified Kill Chain,(opens in new tab) published in 2017, aims to complement (not compete with) other cybersecurity kill chain frameworks, such as Lockheed Martin’s and MITRE’s ATT&CK.
<img width="1230" height="794" alt="image" src="https://github.com/user-attachments/assets/2f2c29f8-33ea-4839-bcab-c5c815506533" />

**Question:** What year was UKC released?

**Answer:** 2017

**Question:** How many attack phases exist?

**Answer:** 18

**Question:** Which phase focuses on avoiding detection?

**Answer:** Defense Evasion

**Question:** Which phase removes data from a network?

**Answer:** Exfiltration

**Question:** Which phase achieves attacker goals?

**Answer:** Objectives

**Key Takeaway:**

The UKC provides a complete view of attacker activities from preparation to final impact.

---

### Task 5 – Goal: In (Initial Foothold)
The main focus of this series of phases is for an attacker to gain access to a system or networked environment. An attacker will employ numerous tactics to investigate the system for potential vulnerabilities that can be exploited to gain a foothold in the system. 

<img width="1201" height="844" alt="image" src="https://github.com/user-attachments/assets/1c5f73bf-2c85-4507-bed0-3b6aab8cdacd" />

| Question                       | Answer             |
| ------------------------------ | ------------------ |
| Email-based foothold technique | Phishing           |
| Impersonating an employee      | Social Engineering |
| Setting up a C2 server         | Weaponization      |
| Exploiting a vulnerability     | Exploitation       |
| Moving between systems         | Pivoting           |
| Maintaining access             | Persistence        |

**SOC Perspective:**

Many attacks are stopped during these early phases.

---

### Task 6 – Goal: Through (Network Propagation)
<img width="1686" height="391" alt="image" src="https://github.com/user-attachments/assets/c1ace31a-8c0b-4a9c-960c-ed13d25c11c3" />

The "Through" goal follows a successful foothold being established on the target network. If defensive controls prevent the attacker from achieving their objective, they will seek to gain additional access and privileges to systems. The attacker would set up a base on one of the systems to act as their pivot point and use it to gather information about the internal network.

<img width="1115" height="823" alt="image" src="https://github.com/user-attachments/assets/d1ae6afd-f8db-4c1f-b51a-e5793e2badf9" />

**Question:** Failed administrator logins indicate?

**Answer:** Privilege Escalation

**Question:** Mimikatz attempting credential dumping?

**Answer:** Credential Access

**Key Takeaway:**

Attackers frequently seek higher privileges and additional credentials before expanding access.

---

### Task 7 – Goal: Out (Action on Objectives)
The "Out" goal wraps up the journey of an adversary’s attack on an environment, where they have critical asset access and can fulfil their attack goals. These goals are usually geared toward compromising the confidentiality, integrity and availability (CIA) triad. The tactics to be deployed by an attacker would include:

<img width="1197" height="771" alt="image" src="https://github.com/user-attachments/assets/38ad9bfc-378e-47a8-b661-4bc066d37686" />

**Question:** Large outbound traffic to suspicious IP?

**Answer:** Exfiltration

**Question:** Public release of PII affects?

**Answer:** Confidentiality

**Key Takeaway:**

Many organizations discover attacks only during this late stage.

---

### Task 8 – Practical

**Deploy** the static site attached to the task. You will need to match the various actions of an attacker to the correct phase of the Unified Kill Chain framework to reveal the flag.

**Flag:**

`THM{UKC_SCENARIO}`

**Lesson Learned:**

Mapping attacker actions to UKC phases helps reconstruct incidents.

---

# Pyramid of Pain

### Task 2 – Hash Values
As per Microsoft, the hash value is a numeric value of a fixed length that uniquely identifies data. A hash value is the result of a hashing algorithm. 
The following are some of the most common hashing algorithms: 
<img width="1400" height="455" alt="image" src="https://github.com/user-attachments/assets/2d205aed-53ac-41ac-ac76-ec52e3c3c3d8" />

Various online tools can be used to do hash lookups like VirusTotal and Metadefender Cloud - OPSWAT.
[<img width="1844" height="813" alt="image" src="https://github.com/user-attachments/assets/b040c948-8293-47de-841d-81a747a624d2" />](https://www.virustotal.com/gui/)
Below the hash in the screenshot above, you can see the filename. In this case, it is "m_croetian.wnry"

[<img width="1546" height="694" alt="image" src="https://github.com/user-attachments/assets/b7253974-c90c-4c8d-aad5-690cb2a47487" />](https://metadefender.opswat.com/?lang=en)


**Question:** Sample filename?

**Answer:** Sales_Receipt 5606.xls

**Key Takeaway:**

Hashes are easy for attackers to change by modifying files.

---

### Task 3 – IP Addresses
From a defense standpoint, knowledge of the IP addresses an adversary uses can be valuable. A common defense tactic is to block, drop, or deny inbound requests from IP addresses on your parameter or external firewall. This tactic is often not bulletproof as it’s trivial for an experienced adversary to recover simply by using a new public IP address.
Malicious IP connections ([app.any.run](https://app.any.run/tasks/a66178de-7596-4a05-945d-704dbf6b3b90)):
<img width="656" height="157" alt="image" src="https://github.com/user-attachments/assets/d429891d-7ccf-4f50-b134-65f7acd9ade9" />

**NOTE!** Do not attempt to interact with the IP addresses shown above.

One of the ways an adversary can make it challenging to successfully carry out IP blocking is by using **[Fast Flux](https://unit42.paloaltonetworks.com/fast-flux-101/).**
**Question:** First malicious IP?

**Answer:** 50.87.136.52

**Question:** First domain contacted?

**Answer:** craftingalegacy.com

**Key Takeaway:**

Attackers can easily replace infrastructure.

---

### Task 4 – Domain Names
Let's step up the Pyramid of Pain and move on to Domain Names. You can see the transition of colors - from green to teal.
Malicious  Sodinokibi  C2 ( Command and Control Infrastructure)  domains:
<img width="1463" height="592" alt="image" src="https://github.com/user-attachments/assets/0b5ce421-be47-4edf-80e9-bec7b2916678" />

You can see the actual website the shortened link is redirecting you to by appending "+" to it (see the examples below). Type the shortened URL in the address bar of the web browser and add the above characters to see the redirect URL. 
NOTE: The examples of the shortened links below are non-existent.
<img width="1140" height="800" alt="image" src="https://github.com/user-attachments/assets/fa0c0843-9359-4403-8730-15652d4e71d5" />

HTTP Requests: 
This tab shows the recorded HTTP requests since the detonation of the sample. This can be useful to see what resources are being retrieved from a webserver, such as a dropper or a callback.
<img width="1162" height="276" alt="image" src="https://github.com/user-attachments/assets/cf5d237b-739c-4a67-b041-4991c7d27da8" />

Connections:
This tab shows any communications made since the detonation of the sample. This can be useful to see if a process communicates with another host. For example, this could be C2 traffic, uploading/downloading files over FTP, etc.
<img width="1130" height="268" alt="image" src="https://github.com/user-attachments/assets/822b142e-91be-48ca-8eeb-83aef9b5fa92" />

DNS Requests:
This tab shows the DNS requests made since the detonation of the sample. Malware often makes DNS requests to check for internet connectivity (I.e. if It can't reach the internet/call home, then it's probably being sandboxed or is useless). 
<img width="1136" height="264" alt="image" src="https://github.com/user-attachments/assets/2f5090b0-ae93-4482-a833-b7ec3158a6c9" />


**Question:** Suspicious domain?

**Answer:** craftingalegacy.com

**Question:** Website address term?

**Answer:** Domain Name

**Question:** Unicode impersonation attack?

**Answer:** Punycode Attack

**Question:** TinyURL destination?

**Answer:** https://tryhackme.com/

**Key Takeaway:**

Domains provide more intelligence value than hashes but remain replaceable.

---

### Task 5 – Host Artifacts
Host artifacts are the traces or observables that attackers leave on the system, such as registry values, suspicious process execution, attack patterns or IOCs (Indicators of Compromise), files dropped by malicious applications, or anything exclusive to the current threat.

Suspicious process execution from Word: 
<img width="945" height="44" alt="image" src="https://github.com/user-attachments/assets/eb59de91-8268-444f-9f1f-367127c429ec" />

Suspicious events followed by opening a malicious application: 
<img width="1406" height="709" alt="image" src="https://github.com/user-attachments/assets/3512e751-fa8f-488a-a3eb-49c7a0ea8a5b" />

[The files modified/dropped by the malicious actor:
<img width="1203" height="267" alt="image" src="https://github.com/user-attachments/assets/ae3bce50-bf01-429b-8af6-39c8e0995666" />](https://assets.tryhackme.com/additional/pyramidofpain/task5-report.pdf)

**Question:** POST request destination?

**Answer:** 96.126.101.6

**Question:** Malicious executable?

**Answer:** G_jugk.exe

**Question:** VirusTotal detections?

**Answer:** 9

**Key Takeaway:**

Host artifacts reveal attacker behavior on compromised systems.

---

### Task 6 – Network Artifacts
A network artifact can be a user-agent string, C2 information, or URI patterns followed by the HTTP POST requests.An attacker might use a User-Agent string that hasn’t been observed in your environment before or seems out of the ordinary. The User-Agent is defined by RFC2616(opens in new tab) as the request-header field that contains the information about the user agent originating the request.

Network artifacts can be detected in PCAPs (file that contains the network packet dumps) by using a tool such as Wireshark or TShark, or exploring IDS (Intrusion Detection System) alerts from a tool such as Snort(opens in new tab). You will learn these tools in the following rooms, but in short, imagine a list of suspicious HTTP POST requests:
<img width="1572" height="139" alt="image" src="https://github.com/user-attachments/assets/d55b9281-3c46-42c2-ab60-3f794551e648" />

It's hard to attribute the requests to a specific malware from the first glance, but you can dig deeper and look for its network indicators, such as the User-Agent. In TShark, you could use the following command:

**tshark --Y http.request -T fields -e http.host -e http.user_agent -r analysis_file.pcap**
<img width="1395" height="338" alt="image" src="https://github.com/user-attachments/assets/29f4ad59-6a46-4508-b107-1ad8aa883eeb" />
These are the most common User-Agent strings found for the [Emotet](https://www.mcafee.com/blogs/other-blogs/mcafee-labs/emotet-downloader-trojan-returns-in-force/) trojan. If you can detect the custom User-Agent strings that the attacker is using, you might be able to block them, creating more obstacles and making their attempt to compromise the network more annoying.

**Question:** Which indicator identified Emotet?

**Answer:** User-Agent

**Question:** Number of POST requests?

**Answer:** 6

**Key Takeaway:**

Network artifacts are harder for attackers to modify consistently.

---

### Task 7 – Tools
Attackers would use the utilities to create malicious macro documents (maldocs) for spearphishing attempts, a backdoor that can be used to establish C2 (Command and Control Infrastructure)(opens in new tab), any custom .EXE, and .DLL files, payloads, or password crackers.

**A Trojan dropped the suspicious "Stealer.exe" in the Temp folder:**
<img width="956" height="430" alt="image" src="https://github.com/user-attachments/assets/fb3bbed1-922f-4d02-b013-d5e2167e183a" />
The execution of the suspicious binary:
<img width="822" height="48" alt="image" src="https://github.com/user-attachments/assets/b234aed1-0114-479d-81f4-54cc2a56ce19" />

Antivirus signatures, detection rules, and YARA rules can be great weapons for you to use against attackers at this stage.

[MalwareBazaar](https://bazaar.abuse.ch/) and [Malshare](https://malshare.com/) are good resources to provide you with access to the samples, malicious feeds, and [**YARA**](https://www.picussecurity.com/resource/glossary/what-is-a-yara-rule) results - these all can be very helpful when it comes to threat hunting and incident response. 

Example of SSDeep from VirusTotal:
<img width="1152" height="648" alt="image" src="https://github.com/user-attachments/assets/fdc9a3a4-b83c-44be-a058-83a60910cd3d" />

**Question:** Similarity detection method?

**Answer:** Fuzzy Hashing

**Question:** Full name?

**Answer:** Context Triggered Piecewise Hashes

**Key Takeaway:**

Detecting attacker tools creates greater disruption than detecting simple indicators.

---

### Task 8 – TTPs
TTPs stands for Tactics, Techniques & Procedures. This includes the whole [MITRE ATT&CK Matrix](https://attack.mitre.org/), which means all the steps taken by an adversary to achieve his goal, starting from phishing attempts to persistence and data exfiltration. 
<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/920febdd-cb3f-4705-9d1f-94141bf908af" />

**Question:** Exfiltration techniques in ATT&CK?

**Answer:** 9

**Question:** Tool used by Chimera?

**Answer:** Cobalt Strike

**Key Takeaway:**

TTP-based detection targets attacker behavior rather than specific infrastructure.

---

### Task 9 – Practical
Deploy the static site attached to this task and place the prompts into the correct tiers in the pyramid of pain!

Once you are sure, submit your answer on the static site to retrieve a flag!

**Flag:**

`THM{PYRAMIDS_COMPLETE}`

---

# 🛡️ SOC Analyst L1: Mindset 

## Tricky Connection

Many beginners think:

> "How do attackers compromise systems?"

A SOC Analyst thinks:

> "Which phase are they currently in, and how can I detect them before they reach their objective?"

This room taught me that defenders do not need to stop every attack at the beginning.

An attacker can still be detected during:

* Credential Access
* Lateral Movement
* Exfiltration
* Impact

The Pyramid of Pain adds another layer:

Detecting a malicious hash may stop one file.

Detecting a TTP may stop an entire campaign.

That is a huge mindset shift.

## Next Learning Steps

To strengthen this knowledge, I should continue learning:

1. MITRE ATT&CK Framework
2. Windows Event Logs
3. Network Traffic Analysis
4. Wireshark Fundamentals
5. Threat Hunting Basics
6. Malware Analysis Fundamentals
7. Detection Engineering
8. SIEM Alert Investigation
9. Normal vs Abnormal Authentication Activity
10. Incident Response Workflow

---

# 💼 Scenario-Based Interview Question 

## Question

As a SOC Analyst, you receive three alerts within one hour:

1. Mimikatz detected on a workstation.
2. Multiple failed administrator logins.
3. Large outbound encrypted traffic to an unknown external IP.

How would you analyze this situation using the Unified Kill Chain?

## Answer Concept

My approach would be:

### Step 1: Build a Timeline

Determine the sequence of events.

### Step 2: Map Events to UKC

* Failed administrator logins → Privilege Escalation
* Mimikatz activity → Credential Access
* Large outbound traffic → Exfiltration

### Step 3: Assess Risk

The attacker may already have internal access and be actively stealing data.

### Step 4: Investigate

* Review authentication logs.
* Identify compromised accounts.
* Analyze endpoint activity.
* Examine network traffic.
* Determine what data may have been accessed.

### Step 5: Containment

* Isolate affected systems.
* Disable compromised accounts.
* Block suspicious connections.
* Escalate according to incident response procedures.

### Step 6: Detection Improvement

Create new detections around:

* Credential dumping activity
* Privilege escalation attempts
* Data exfiltration patterns

This approach focuses on understanding the attack lifecycle rather than treating each alert as an isolated event.

---

# Final Reflection

This room fundamentally changed how I view cyber attacks.

Before learning the Unified Kill Chain and Pyramid of Pain, I focused mostly on indicators and alerts. Now I understand that attacks follow patterns, phases, and objectives.

The Unified Kill Chain helps me understand where an attacker is in their journey, while the Pyramid of Pain helps me understand which detections create the greatest operational difficulty for an adversary.

As an aspiring SOC Analyst L1, these frameworks provide a structured way to investigate incidents, understand attacker behavior, and build stronger detection strategies.

