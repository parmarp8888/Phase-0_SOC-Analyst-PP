# Room Walkthrough: [Junior Security Analyst Intro
](https://tryhackme.com/room/jrsecanalystintrouxo)
## 🎯 Day 4 Objective

As part of my SOC Analyst L1 learning journey, this room introduced me to the daily responsibilities of a Junior Security Analyst and provided a small hands-on experience of investigating and responding to security alerts.

After learning about cybersecurity careers and security roles in previous rooms, I wanted to understand:

> "What does a SOC Analyst actually do during a normal workday?"
<img width="2285" height="470" alt="image" src="https://github.com/user-attachments/assets/73889d45-f402-4450-834b-5eb4615fbeff" />

Above are the cyber news for September 2025 T[he Hacker News](https://thehackernews.com/)

This room helped answer that question by showing how analysts monitor alerts, investigate suspicious activity, escalate incidents, and work with other SOC team members.

---

### Who is this for?

* Aspiring SOC Analysts
* Cybersecurity beginners
* Blue Team learners
* Students interested in Security Operations Centers (SOC)

### What is it?

An introductory room that explains the role of a Junior Security Analyst and simulates a basic alert investigation workflow.

### Where does this apply?

* Security Operations Centers (SOC)
* Enterprise environments
* Managed Security Service Providers (MSSPs)
* Government security teams

### When should I learn this?

After understanding basic cybersecurity concepts and career paths, but before learning advanced detection and incident response topics.

### Why is it important?

A SOC Analyst is often the first line of defense against cyber threats. Understanding their responsibilities helps build the foundation for future Blue Team skills.

### How does it work?

The room introduces:

* SOC team structure
* Daily analyst responsibilities
* Security alert investigations
* Escalation procedures
* Basic incident response actions

---

### What confused me?

My biggest confusion was understanding what happens after an alert appears.

Questions that came to mind included:

* How do analysts know which alert is important?
* When should an alert be escalated?
* Who receives the escalation?
* How does blocking a malicious IP actually help protect the organization?

Before this room, I thought SOC work mainly involved watching dashboards.

### What I learned?

This room taught me that a Junior Security Analyst does much more than simply monitoring alerts.

Key concepts learned:

* Security alerts require investigation.
* Analysts must identify malicious indicators.
* Escalation is an important part of the workflow.
* Team collaboration is critical inside a SOC.
* Detection and response are continuous activities.

During the lab, I:

* Investigated alerts.
* Identified a malicious IP address.
* Escalated the alert to the appropriate person.
* Blocked the malicious IP through a security control.

### How I improved?

Before this room, I viewed SOC work as mostly monitoring security tools.

After completing the room, I understand that analysts must think critically about alerts, gather evidence, make decisions, and communicate findings effectively.

My perspective shifted from:

> "An alert appeared."

to

> "Why did this alert trigger, what does it mean, and what action should be taken next?"

### Real-World Relevance

In a real organization:

* Analysts review hundreds of alerts daily.
* Some alerts are false positives.
* Some alerts indicate active threats.
* Analysts must investigate quickly and accurately.
* Escalation ensures more experienced responders can assist when needed.

This process helps reduce risk and prevent attacks from causing significant business impact.

---

## 🛡️ SOC Analyst L1: Mindset

### Tricky Connection

A beginner often focuses on:

> "How can an attacker gain access?"

A SOC Analyst focuses on:

> "What evidence would the attacker leave behind?"

For example:

* An attacker connects from a suspicious IP.
* The SOC Analyst investigates connection logs.
* The analyst determines whether the activity is malicious.
* The analyst escalates and blocks the threat.

The focus is no longer on performing the attack but on detecting and disrupting it.

### Next Learning Steps

To build a stronger SOC foundation, I should continue learning:

1. Networking Fundamentals
2. IP Addresses and Subnets
3. DNS Fundamentals
4. Log Analysis
5. SIEM Basics
6. Windows Event Logs
7. Linux Logs
8. Indicators of Compromise (IOCs)
9. Incident Response Fundamentals

---

## Critical Thinking

### Question

You receive an alert showing repeated connections from an external IP address to multiple internal devices. The IP has previously been associated with malicious activity.

As a Junior SOC Analyst, what would you do?

### Answer Concept

My approach would be:

1. Review the alert details and affected systems.
2. Verify whether the IP has a known malicious reputation.
3. Check logs to understand the connection activity.
4. Determine whether any successful compromise occurred.
5. Document findings and evidence.
6. Escalate according to SOC procedures.
7. Recommend blocking the IP if confirmed malicious.

The objective is to validate the threat, understand its impact, and support containment efforts.

---

## 📝 Room Questions & Key Takeaways

### Task 1: [Junior Security Analyst Journey](https://medium.com/fnplus/security-operations-center-93e67268180a)

**Question:** Which team do you work with as a Junior Security Analyst?

**Answer:** SOC
Your Daily Duties
As a Junior Security Analyst, also called a SOC Level 1 Analyst, you work in a 24/7 SOC team and mostly review the security alerts together with your colleagues. To do it efficiently, you will need practice and skills learned through this path. During your work shift, you would typically:

Monitor and investigate various security alerts
Participate in SOC brainstorms and workshops
Cooperate with other teams to keep your company safe
Constantly learn and discover new attacks and defenses

**Key Takeaway:**

A Junior Security Analyst works within the Security Operations Center (SOC), collaborating with analysts, engineers, responders, and managers to monitor and protect the organization.

---

### Task 2: Security Operations Center (SOC)
<img width="1693" height="913" alt="SOC image" src="https://github.com/user-attachments/assets/d5d2e6a8-828d-45bb-80cc-b246a39b620a" />
**SOC and Your Team**
You are not alone in monitoring the alerts and securing the whole company. A lot of people support you with your job. SOC engineers are configuring the security tools, senior analysts are helping with complex attacks, and a manager is trying to keep everything under control. A Security Operations Center (SOC) is your big team that protects the company, each role in its own way. Now, let's meet your colleagues!

---
**Will Griffin
Senior Analyst**
Will is your closest colleague. He helps you and other Junior analysts when something is unclear and handles complex cases after you do the initial analysis.

**Corey Stevens
SOC Engineer**
Corey doesn't have shifts and doesn't analyze the alerts. Instead, he maintains security tools and configures the alerts to make your analyst's job easier.

**Emily Conway
SOC Manager**
Emily tries to keep everything under control. She reports SOC results to the top management and makes sure you aren't lost in that big new cyber security world.

**Daniel Herrera
Incident Responder**
You don't work with Daniel every day, but when he's online, you know something serious has happened. He is called on demand during major incidents.

---
**Your Daily Duties**
Are you inspired by your colleagues' work and wish to advance to their roles? Cyber security is a broad field, and with time you'll find the path that excites you most. But before that, you need to gain work experience as a Junior Security Analyst. Along the way, you'll have many lessons and challenges, where you may:

Detect and prevent a data stealer infection on a coworker's laptop
Analyze and stop a phishing campaign targeting the finance team
Participate in a bigger incident, such as a full-scale ransomware attack
Team up with your teammates to build detection rules and automations
Go beyond cyber and understand how companies operate from the inside 
**Question:** Continue to the next task!

**Answer:** No answer required.

**Key Takeaway:**

The SOC is a team environment where different specialists work together to detect, investigate, and respond to threats.

Examples of real-world SOC activities include:

* Phishing investigations
* Malware infections
* Ransomware incidents
* Detection engineering
* Security automation

---

### Task 3: A Day in the Life of a Security Analyst
<img width="1200" height="677" alt="image" src="https://github.com/user-attachments/assets/80eaa921-81e7-4654-8eb1-9cf2bb8f47a8" />

**Being a Security Analyst**
Being in the defensive frontline is not easy, as you have to constantly learn new things. During a busy 8-hour shift, you might be buried under a mountain of "tickets" - the alerts and tasks that you need to resolve in a timely manner. Still, the job is fun and rewarding, especially after you stop a real threat from damaging your organization. Even better, it is fascinating to know how the attacks you hear about in the news actually happen in the real world.
**Question:** What was the malicious IP address in the alerts?

**Answer:** `221.181.185.159`

**Key Takeaway:**

IP addresses can act as Indicators of Compromise (IOCs) during investigations.

---

**Question:** To whom did you escalate the alert with the malicious IP?

**Answer:** `Will Griffin`

**Key Takeaway:**

Escalation ensures that important security incidents receive proper attention and investigation.

---

**Question:** What message did you get after blocking the IP address on the firewall?

**Answer:** `THM{until-we-meet-again}`

**Key Takeaway:**

Blocking malicious infrastructure is one method of containment that helps reduce an attacker's ability to interact with organizational systems.

---

## Final Reflection

This room provided my first practical look into the daily life of a Junior Security Analyst.

The biggest lesson was realizing that SOC work is not simply watching dashboards. It involves investigating alerts, validating threats, communicating findings, escalating incidents, and helping protect the organization through informed decisions.

As an aspiring SOC Analyst L1, this room gave me a clearer understanding of what I may be doing in a real SOC environment and reinforced my interest in defensive security operations.
