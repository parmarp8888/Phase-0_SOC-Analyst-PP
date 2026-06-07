# Room Walkthrough: [SOC Fundamentals](https://tryhackme.com/room/socfundamentals)

## 🎯 Day 5 Objective
<img width="550" height="500" alt="image" src="https://github.com/user-attachments/assets/fc8c02fd-dcda-4c9c-bd68-6dc35cc2f4f1" />

As part of my SOC Analyst L1 learning journey, this room introduced me to the core purpose of a Security Operations Center (SOC) and the day-to-day responsibilities of security professionals working inside it.

Before this room, I knew that a SOC monitored security alerts, but I did not fully understand how People, Processes, and Technology work together to detect and respond to security incidents.

> This room helped me experience a simplified version of a real SOC investigation and introduced me to the mindset required for an entry-level Security Analyst.
This room will delve into some key concepts of SOC, one of the most important fields in defensive security.

Learning Objectives
Building a baseline for SOC (Security Operations Center)
Detection and response in SOC
The role of People, Processes, and Technology
Practical exercise 

---

### Who is this for?

* Aspiring SOC Analysts
* Blue Team learners
* Incident Responders
* Security Operations professionals
* Anyone interested in threat detection

### What is it?

An introduction to Security Operations Centers (SOC), their responsibilities, team structure, investigation processes, and security technologies.

### Where does this apply?

* Enterprise environments
* Government organizations
* Financial institutions
* Healthcare networks
* Managed Security Service Providers (MSSPs)

### When should I learn this?

After learning cybersecurity fundamentals and before diving deeper into SIEMs, log analysis, and incident response.

### Why is it important?
<img width="600" height="400" alt="image" src="https://github.com/user-attachments/assets/a253b3c4-5532-4f26-8d42-efa3e7da8fe0" />
Organizations face security threats every day. A SOC helps detect suspicious activity, investigate alerts, and coordinate responses before incidents become major breaches.

### How does it work?

A mature SOC relies on three pillars:
<img width="869" height="317" alt="image" src="https://github.com/user-attachments/assets/d36fbfd3-3521-4401-92e1-56d6af0cf2ce" />
* **People** → Analysts, Engineers, Managers, and Responders
* **Process** → Investigation workflows and response procedures
* **Technology** → SIEM, Firewall, IDS/IPS, XDR, Antivirus, SOAR, and other security tools

Together these pillars help organizations maintain effective detection and response capabilities.

---

### What confused me?

One thing that initially confused me was the difference between SOC Analyst Level 1, Level 2, and Level 3 roles.

At first, all three appeared to perform investigations.

Questions I had included:

* What does Level 1 do that Level 2 does not?
* When is an alert escalated?
* Why are Detection Engineers separate from Analysts?
* Does a SIEM respond to incidents or only detect them?

The practical exercise helped clarify these differences.

### What I learned?

This room introduced several important SOC concepts:

* SOC stands for **Security Operations Center**
* Detection and Response are the primary objectives of a SOC
* People, Process, and Technology form the foundation of SOC operations
* Alert triage is a key responsibility of a SOC Analyst Level 1
* The 5 Ws help analysts structure investigations
* SIEM solutions primarily focus on detection and alerting
* Analysts must investigate context before deciding whether an alert is malicious or legitimate

I also learned that not every alert represents an attack.

### How I improved?

Before this room, I thought security monitoring was simply looking at alerts and deciding whether they were bad.

Now I understand that analysts must collect evidence and answer investigative questions before making conclusions.

The practical port-scanning exercise showed me the importance of asking:

* What happened?
* When did it happen?
* Where did it happen?
* Who performed the activity?
* Why did it happen?

Instead of immediately assuming malicious intent.

### Real-World Relevance

In a real enterprise, security tools generate thousands of alerts daily.

If analysts treat every alert as an attack, operations become inefficient.

For example:

* Vulnerability scanners may generate port-scanning alerts.
* System administrators may perform unusual but legitimate activities.
* Automated security tools may trigger expected detections.

A SOC Analyst must investigate context before escalating incidents.

This room demonstrated that security analysis is evidence-based decision-making rather than guesswork.

---

## 🛡️ SOC Analyst L1: Mindset

### Tricky Connection

A beginner often thinks:

> "A port scan means an attacker is scanning the network."

A SOC Analyst asks:

> "Who performed the scan, why was it performed, and is it expected behavior?"

In the practical exercise, the alert showed a port scan.

Initially, this appears suspicious.

However, further investigation revealed:

* The source host was Nessus.
* The vulnerability assessment team had already informed the SOC.
* The activity was intended and authorized.

This is a major mindset shift.

A SOC Analyst does not investigate alerts to prove an attack happened.

A SOC Analyst investigates alerts to discover the truth.

### Next Learning Steps

To strengthen my SOC foundation, I should continue learning:

1. Networking Fundamentals
2. TCP/IP and Common Protocols
3. Windows Event Logs
4. Linux Logs
5. SIEM Fundamentals
6. Threat Intelligence Basics
7. Incident Response Lifecycle
8. Log Correlation
9. Normal vs Abnormal Network Traffic

---

## Critical Thinking

### Question

A SIEM generates an alert indicating that a host inside the organization is performing port scans against multiple internal systems.

As a SOC Analyst L1, what would be your first steps?

### Answer Concept

My investigation approach would be:

1. Review the alert details.
2. Identify source and destination systems.
3. Determine when the activity occurred.
4. Check whether vulnerability scanning activities were scheduled.
5. Review asset ownership and business purpose.
6. Analyze supporting logs and related events.
7. Determine whether the activity is authorized or malicious.
8. Escalate only if suspicious behavior is confirmed.

The objective is to gather evidence and establish context before making a conclusion.

---

## 📝 Room Questions 

### Task 1: Introduction to SOC
<img width="1244" height="700" alt="image" src="https://github.com/user-attachments/assets/e46b9181-2850-4375-aaee-6db1a97d0f99" />

**Question:** What does SOC stand for?

**Answer:** Security Operations Center

**Key Takeaway:** A SOC is responsible for monitoring, detecting, investigating, and responding to security threats.

---

### Task 2: Purpose and Components
The main focus of the SOC team is to keep Detection and Response intact. The SOC team has some resources available in the form of security solutions that help them achieve this. These solutions integrate the whole company’s network and all the systems to monitor them from one centralized location. Continuous monitoring is required to detect and respond to any security incident.

**Question:** The SOC team discovers an unauthorized user attempting to log in. Which capability is this?

**Answer:** Detection

<img width="825" height="801" alt="image" src="https://github.com/user-attachments/assets/132d0afa-7f60-454e-ba63-737b5ac3acf2" />
**Question:** What are the three pillars of a SOC?

**Answer:** People, Process, Technology

**Key Takeaway:** Detection and Response are the core objectives of a SOC, supported by People, Process, and Technology.

---

### Task 3: People
The People are known as the SOC team. This team has the following roles and responsibilities.
<img width="1140" height="572" alt="image" src="https://github.com/user-attachments/assets/52416770-b06f-4682-9cee-c2901ade8715" />

**Question:** Alert triage and reporting is the responsibility of?

**Answer:** SOC Analyst (Level 1)
<img width="800" height="1200" alt="image" src="https://github.com/user-attachments/assets/8f8a0fc7-1b1c-4fd5-a62e-e003f2437643" />

**Question:** Which role focuses on creating detection rules?

**Answer:** Detection Engineer

**Key Takeaway:** Different SOC roles work together to detect, investigate, and respond to threats.

---

### Task 4: Process
**Alert Triage**
The alert triage is the basis of the SOC team. The first response to any alert is to perform the triage. The triage is focused on analyzing the specific alert. This determines the severity of the alert and helps us prioritize it. The alert triage is all about answering the 5 Ws. What are these 5 Ws?
<img width="740" height="627" alt="image" src="https://github.com/user-attachments/assets/41f02a94-c944-4647-8abe-808ddff2b3c2" />

**Reporting**
The detected harmful alerts need to be escalated to higher-level analysts for a timely response and resolution. These alerts are escalated as tickets and assigned to the relevant people. The report should discuss all the 5 Ws along with a thorough analysis, and screenshots should be used as evidence of the activity.

**Incident Response and Forensics**
Sometimes, the reported detections point to highly malicious activities that are critical. In these scenarios, high-level teams initiate an incident response. The incident response process is discussed in detail in the Incident Response room. A few times, a detailed forensics activity also needs to be performed. This forensic activity aims to determine the incident’s root cause by analyzing the artifacts from a system or network.
**Question:** John attempted to steal system data. Which W does this answer?

**Answer:** Who

**Question:** Large-scale data exfiltration was detected. Which W does this answer?

**Answer:** What

**Key Takeaway:** The 5 Ws provide a structured approach to investigations.

---

### Task 5: Technology
<img width="1509" height="719" alt="image" src="https://github.com/user-attachments/assets/49655836-3556-4d0a-8a7b-4650b5abcd9a" />

**Question:** Which security solution monitors incoming and outgoing network traffic?

**Answer:** Firewall

**Question:** Do SIEM solutions primarily focus on detection and alerting?

**Answer:** Yea

**Key Takeaway:** Technology helps automate detection and provides visibility into security events.
|   |   |
|---|---|
|Skill|Why It Matters|
|Log Analysis|The core daily task is interpreting logs from firewalls, endpoints, applications, and servers to detect threats.|
|SIEM Proficiency|Operating platforms like Splunk, Microsoft Sentinel, IBM QRadar, or Elastic SIEM to correlate events and investigate alerts.|
|Network Security|Understanding TCP/IP, DNS, firewalls, VPNs, and how attackers exploit network weaknesses.|
|Incident Response|Executing the full IR lifecycle: identification, containment, eradication, recovery, and lessons learned.|
|Malware Analysis|Identifying indicators of compromise (IOCs) and understanding how malware operates at a basic level.|
|Digital Forensics|Preserving and analyzing digital evidence from compromised systems.|
|Threat Intelligence|Applying knowledge of attacker TTPs (as mapped in the MITRE ATT&CK framework) to detect and prioritize threats.|
|Scripting (Python / PowerShell)|Automating repetitive tasks, writing detection rules, and building custom analysis tools.|
|Cloud Security Awareness|Understanding threat detection in AWS, Azure, and GCP environments as infrastructure moves to the cloud.|
|Vulnerability Management|Identifying and prioritizing known vulnerabilities using tools like Nessus or Qualys.|

---

### Task 6: Practical Exercise

**Investigation Results**

* What? → Port Scan
* When? → June 12, 2024 17:24
* Where? → 10.0.0.3
* Who? → Nessus
* Why? → Intended
* Response Sent? → Yea
* Flag → THM{000_INTRO_TO_SOC}

**Key Takeaway:** Context matters. Not every alert indicates malicious activity.

---

## Final Reflection

This room was my first practical introduction to the daily work of a SOC Analyst.

The most valuable lesson was learning that alerts are only the starting point of an investigation. Effective analysts gather context, validate assumptions, and use evidence to determine whether activity is legitimate or malicious.

As an aspiring SOC Analyst L1, this room helped me understand how People, Process, and Technology work together to support detection and response inside a real-world Security Operations Center.
