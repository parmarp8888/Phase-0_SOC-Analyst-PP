# Room Walkthrough: [SOC Role in Blue Team](https://tryhackme.com/room/socroleinblueteam)

## 🎯 Day 6 Objective
<img width="225" height="225" align="right" alt="image" src="https://github.com/user-attachments/assets/671d11c5-8002-4bea-b24b-3cbdf8da2aaa" />

As part of my SOC Analyst L1 learning journey, this room helped me understand where the Security Operations Center (SOC) fits within an organization's security structure and how a beginner can progress from SOC L1 to more advanced cybersecurity roles.

Before completing this room, I knew that SOC Analysts monitor alerts and investigate suspicious activity, but I did not fully understand how the SOC interacts with other security teams such as Incident Response, Security Engineering, Governance, Risk & Compliance (GRC), and executive leadership.

> This room helped me understand that a SOC is not an isolated team. It is one part of a larger security operation working together to protect an organization.

---

### Who is this for?

* Aspiring SOC Analysts
* Blue Team beginners
* Cybersecurity students
* Professionals exploring defensive security careers

### What is it?

An introductory room explaining the role of the Blue Team, SOC structure, security hierarchy, and possible career progression paths for SOC Analysts.

### Where does this apply?

* Enterprise organizations
* Government agencies
* Financial institutions
* Healthcare organizations
* Managed Security Service Providers (MSSPs)

### When should I learn this?

Early in a cybersecurity journey before diving deeply into SIEMs, log analysis, threat detection, and incident response.

### Why is it important?

Understanding how security teams operate helps build context for future technical learning and provides a clearer picture of how security incidents are handled in real environments.

### How does it work?

The room introduces:

* Security leadership roles
* Blue Team departments
* SOC career progression
* Internal SOC vs MSSP environments
* Incident handling responsibilities

---

### What confused me?

One area that initially confused me was understanding the relationship between different security teams.

Questions I had included:

* Who makes major cybersecurity decisions?
* How does a SOC interact with CIRT teams?
* What happens after a SOC Analyst escalates an incident?
* What is the difference between working in an Internal SOC and an MSSP?
* Does a SOC Analyst remain in the same role forever?

At first, I viewed the SOC as the entire security department rather than one component of a larger security structure.

### What I learned?

This room introduced several important concepts:

* The CISO is responsible for high-level cybersecurity decisions.
* Blue Team focuses on defensive security operations.
* CIRT handles active security incidents.
* MSSPs provide security services to multiple organizations.
* SOC L1 is often the starting point for a broader cybersecurity career.

I also learned that cybersecurity careers are not linear. Experience gained as a SOC Analyst can lead to roles such as:

* SOC L2 Analyst
* Security Engineer
* Incident Responder
* Threat Hunter
* Security Manager
* CISO

### How I improved?

Before this room, I viewed the SOC role as simply monitoring alerts.

Now I understand that a SOC Analyst is part of a larger security ecosystem.

This changed my perspective from:

> "How do I investigate alerts?"

to

> "How does my investigation support the entire security operation?"

I now better understand how alert investigations contribute to incident response, engineering improvements, and business security decisions.

### Real-World Relevance

In a real enterprise:

* The SOC detects suspicious activity.
* CIRT responds to confirmed incidents.
* Security Engineers improve defenses.
* GRC ensures compliance and policy enforcement.
* The CISO oversees strategic security decisions.

A SOC Analyst often becomes the first person to identify potential threats, making the role critical to the organization's overall security posture.

---

## 🛡️ SOC Analyst L1: Mindset 

### Tricky Connection

Many beginners focus on attack techniques:

> "How would an attacker compromise this system?"

A SOC Analyst focuses on a different question:

> "How would I recognize that compromise as quickly as possible?"

For example:

A Red Teamer may attempt credential theft.

A SOC Analyst focuses on:

* Failed login patterns
* Unusual authentication activity
* Impossible travel logins
* Suspicious account behavior
* Related security alerts

The shift is not learning how attacks work alone.

The shift is learning how attacks appear inside logs, alerts, and monitoring systems.

### Next Learning Steps

To strengthen my SOC Analyst foundation, I should continue learning:

1. Networking Fundamentals
2. TCP/IP Basics
3. Common Network Protocols
4. Windows Event Logs
5. Linux Logs
6. SIEM Fundamentals
7. Incident Response Lifecycle
8. Normal vs Abnormal User Activity
9. Alert Triage Methodology
10. Threat Detection Basics

These topics directly support the responsibilities of a SOC Analyst L1.

---

## Critical Thinking

### Question

You are working as a SOC Analyst L1 when the SIEM generates multiple alerts showing repeated failed login attempts against several employee accounts.

How would you investigate and respond?

### Answer Concept

My approach would be:

#### Step 1: Validate the Alert

* Review the SIEM alert details.
* Identify affected accounts.
* Determine whether the activity is ongoing.

#### Step 2: Investigate Context

* Review source IP addresses.
* Check login timestamps.
* Look for geographic anomalies.
* Identify whether multiple accounts are targeted from the same source.

#### Step 3: Assess Risk

Possible explanations include:

* User password mistakes
* Password spraying attack
* Brute-force attempts
* Automated malicious activity

#### Step 4: Escalate if Necessary

If evidence suggests malicious activity:

* Follow SOC procedures.
* Escalate to SOC L2 or Incident Response.
* Recommend account monitoring or temporary protection measures.

#### Step 5: Document Findings

Record:

* Timeline
* Indicators observed
* Accounts affected
* Actions taken
* Escalation details

The goal is not to immediately assume compromise but to collect evidence, assess risk, and support accurate incident response decisions.

---

## 📝 Room Questions 

### Task 1: Introduction
You've learned about a SOC L1 analyst role in the Junior Security Analyst Intro room. But where is it placed in a company structure? Who is overseeing your team? What other security departments exist? Which skills do you need to advance through your career ladder? Let's find out!

**Learning Objectives**
Understand the concept and purpose of the Blue Team
Explore a place of the SOC within the company structure
Find out about your career path as a SOC L1 analyst 
**Question:** Let's find out!

**Answer:** No answer required.

**Key Takeaway:** Understanding the Blue Team is essential for anyone pursuing a SOC Analyst career.

---

### Task 2: Security Hierarchy
Let's take a look at the high-level example of it:
<img width="2072" height="882" alt="image" src="https://github.com/user-attachments/assets/988467fb-7422-4fb3-9f21-d95116ab0334" />
**Security Departments**
In tiny companies, the IT department takes the role of securing the company. Small to medium-sized companies may have a generic "Information Security" team that does all sorts of tasks. For this room, we will focus on bigger companies with a CISO overseeing multiple security teams, each handling a specific task. For example:

**Red Team**: Offensive security experts, pentesters, or ethical hackers who look for security issues
**GRC Team**: Specialists managing policies and ensuring compliance with regulations like PCI DSS(opens in new tab)
**Blue Team**: Defensive security experts like SOC analysts, engineers, or incident responders

**Question:** Which senior role typically makes key cyber security decisions?

**Answer:** CISO

**Question:** What is the common name for roles like SOC analysts and engineers?

**Answer:** Blue Team

**Key Takeaway:** Cybersecurity is structured into leadership, governance, offensive, and defensive teams, each serving different purposes.

---

### Task 3: Meet the Blue Team
**Security Operations Center (SOC)**
<img width="5890" height="977" alt="image" src="https://github.com/user-attachments/assets/40ce6eac-5138-40ca-ae2a-26b7069eebf0" />
SOC is usually composed of the following roles:
**L1 Analysts**: Junior members who triage alerts and pass complex cases to L2
**L2 Analysts**: Experienced members who investigate more advanced attacks
**Engineers**: Experts in configuring security tools like EDR or SIEM
**Manager**: A person who manages the whole SOC team
<img width="5890" height="977" alt="image" src="https://github.com/user-attachments/assets/dfa1ddba-55a3-48b5-a309-8a9a71345579" />
Here are a few CIRT examples:

JPCERT(opens in new tab): Japan's CERT handling nation-wide breaches
Mandiant(opens in new tab): A private team responding to global cyber incidents
AWS CIRT(opens in new tab): Investigates security incidents of AWS customers

<img width="5890" height="810" alt="image" src="https://github.com/user-attachments/assets/d506b14c-1128-4ee2-80f2-5d2dfd044c0e" />
These narrow roles can include:

**Digital Forensics Analyst:** Uncover hidden threats in disk and memory
**Threat Intelligence Analyst:** Gather data about emerging threat groups
**AppSec Engineer:** Maintain a secure software development lifecycle
**AI Researcher:** Study AI threats and how to defend against them

**Question:** Does Blue Team focus on defensive or offensive security?

**Answer:** Defensive

**Question:** Which department handles active or urgent cyber incidents?

**Answer:** CIRT

**Key Takeaway:** The Blue Team focuses on monitoring, detection, investigation, and response activities.

---

### Task 4: Advancing SOC Career
**SOC Path**
 Let's see how you can start:
Gain core SOC skills and practice them. Related skills like red teaming or general IT would help, too!
Be proactive, try yourself in CTFs, stay in the loop of cyber news, and consider the SAL1 certification!
Prepare for an interview, learn the difference between an internal SOC and MSSP, and apply for a job!
After working for some time in a junior position, consider preparing and advancing to more senior roles!

**Internal SOC vs MSSP**
|Topic|Internal SOC|MSSP|
|---|---|---|
|**Scenario  <br>Example**|You work in a SOC team of the bank and protect the bank's systems|You work for a global MSSP protecting its sixty customers in Europe|
|**Working  <br>Pace**|You usually have calm shifts without too much time pressure|Your shift usually starts from a queue of urgent alerts to analyze|
|**Security  <br>Tools**|You work with just a few tools, but need to know them very well|You have to work with sixty diverse security tools and platforms|
|**Incident  <br>Practice  <br>**|You saw and learned from just two major cyber attacks last year|Every week, you deal with attacks and breaches, and can learn from it|

Your most natural next step after L1 is to become a SOC L2 analyst, but you are free to choose another path! While handling a SIEM alert, you might notice that engineering work appeals to you more. During a cyber attack, you may be fascinated by CIRT actions. You may also find yourself well-suited as a manager and build your path to the CISO role. No matter what, your first year or two is to get real work experience, and to spend this time effectively, follow the tips below!
<img width="1797" height="270" alt="image" src="https://github.com/user-attachments/assets/106eed7f-8f35-4ee1-9d57-4a50055270de" />

**Question:** How would you call a cyber security company providing SOC services?

**Answer:** MSSP

**Question:** Which role naturally continues your SOC L1 analyst journey?

**Answer:** SOC L2 Analyst

**Key Takeaway:** SOC L1 is a strong starting point that can lead to multiple cybersecurity specializations.

---

### Task 5: Final Challenge
For this task, imagine yourself as a CISO of TrySecureMe, a big multinational company. You oversee multiple departments and deal with incidents every month. This time, as many as seven incidents are happening at the same time, and you have to choose the right people to deal with every one of them. Do you know security roles well enough to complete this challenge?
<img width="698" height="796" alt="image" src="https://github.com/user-attachments/assets/9c4ea4ab-0e04-41ed-be50-5a29a1aeb37d" />

**Question:** What flag did you claim after completing the final challenge?

**Answer:** THM{trysecureme_is_secured!}

**Key Takeaway:** Effective security operations require collaboration between multiple teams and roles.

---

### Task 6: Conclusion
Great job completing the challenge! Now you know how SOC team works, where it is placed in the security structure, and what you need to do to start your career journey. Now, continue to the next rooms and learn what does SOC actually protect: humans and systems.
**Question:** Complete the room!

**Answer:** No answer required.

**Key Takeaway:** Understanding organizational security structure provides important context before learning technical detection and monitoring skills.

---

## Final Reflection

This room helped me understand that becoming a SOC Analyst is not just about learning tools or investigating alerts. It is about understanding where the SOC fits within the broader security operation and how different teams work together to defend an organization.

My biggest takeaway was realizing that SOC L1 is not the final destination. It is a foundation that can lead to many different paths within cybersecurity.

As an aspiring SOC Analyst L1, this room gave me a clearer understanding of the Blue Team mindset and how my future responsibilities connect to the larger mission of protecting people, systems, and business operations.
