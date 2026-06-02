# Room Walkthrough: Information Security vs Cybersecurity

## 🎯 Day X Objective:

As part of my SOC Analyst L1 learning journey, this room helped me understand a question that many colleagues have asked me about this topic :

> "What is the difference between Information Security and Cybersecurity?"

Before learning detection, monitoring, or incident response, I wanted to understand what exactly we are protecting and why organizations invest heavily in security.

##

### Who is this for?

* SOC Analysts
* Security Engineers
* Network Administrators
* Risk and Compliance Teams
* Anyone starting a cybersecurity career

### What is Information Security?

Information Security (InfoSec) focuses on protecting information in any form, whether digital, physical, or verbal. Cybersecurity focuses on protecting digital systems, networks, applications, and data from cyber threats.
<div> <img width="50%" height="50%" alt="informations image" src="https://github.com/user-attachments/assets/706d31fa-51fe-4843-aa8d-9e0bccb8290d" /><img width="50%" height="50%" alt="image" src="https://github.com/user-attachments/assets/4a61147e-d52b-497e-879a-39f5cc0e9391" />
</div>

##

### Where does this apply?
<img align="right" width="50%" height="50%" alt="components of InfoSec" src="https://github.com/user-attachments/assets/99b897be-4cd3-49a2-a99e-3f37810496fa" />
* Businesses and enterprises<br>
* Government organizations<br>
* Healthcare and banking sectors<br>
* Educational institutions<br>
* Cloud and on-premises environments<br>

##
<br>

</br>

##

### Why is it important?

Organizations depend on information to operate. Losing sensitive information can result in financial loss, legal issues, operational disruption, and reputational damage.<img align="centre" width="50%" height="50%" alt="imp_image" src="https://github.com/user-attachments/assets/16e6a803-059c-4776-bd21-5791d5724c4a" />

##

### How does it work?

Information Security is built around the CIA Triad:
<img align="right" width="50%" height="50%" alt="CIA-Triad_image" src="https://github.com/user-attachments/assets/88159982-e465-4b68-9bc7-8934493a81f0" />
* **Confidentiality** → Only authorized people can access data.
* **Integrity** → Data remains accurate and unmodified.  
* **Availability** → Information remains accessible when needed.

Cybersecurity implements technical controls such as firewalls, VPNs, endpoint security, monitoring tools, and incident response processes to support these goals.

<!--<img align="centre" width="50%" height="50%" alt="image" src="https://github.com/user-attachments/assets/2d3d1b30-42d3-476a-96b8-f1c6844cd689" />-->

##

### What confused me?

Initially, I thought Information Security and Cybersecurity were the same thing.

My confusion was:

* Why do both terms exist?
* Which one is bigger?
* Does Information Security only involve computers?
* What does "subfield" actually mean in security?

After studying the topic, I understood that Cybersecurity is a specialized area focused on digital environments, while Information Security has a broader scope that includes physical documents, business processes, policies, and people.

##

### What I learned?

Key lessons from this room:

* Information is the real asset being protected.
* Cybersecurity is one component of Information Security.
* The CIA Triad forms the foundation of security decision-making.
* Security is not only about technology; it also includes processes and people.
* Effective security programs balance confidentiality, integrity, and availability.

I also learned that security is closely aligned with business objectives rather than existing solely as a technical function.

### How I improved?

Before this room, I mostly viewed cybersecurity as protecting computers from hackers.

Now I understand that the broader goal is protecting information regardless of where it exists.

This changed my perspective from:

> "How do we stop attacks?"

to

> "What information are we protecting, and what would happen if it were exposed, modified, or unavailable?"

##

### Real-world relevance

In a real enterprise:

* Customer databases require confidentiality.
* Financial records require integrity.
* Business applications require availability.

A SOC team helps support these goals by monitoring threats, detecting suspicious activity, investigating alerts, and helping maintain secure operations.

Every security alert ultimately relates to protecting one or more parts of the CIA Triad.

##

## 🛡️ SOC Analyst L1: 

### Tricky Connection

Many beginners focus on attacks, tools, and hacking techniques.

A SOC Analyst focuses on protecting business information.

For example:

* A malware alert is not just malicious software.
* A phishing email is not just a suspicious message.
* A ransomware incident is not just an infected machine.

Each event threatens confidentiality, integrity, or availability.

Understanding this connection helps transform technical observations into business-focused security investigations.

--

### Security Career Hierarchy

<img align="centre" width="100%" height="100%" alt="image" src="https://github.com/user-attachments/assets/6bb02c50-fa9a-4bd7-b3cd-fa70e1e84a2d" />

--

### Next Learning Step

My next room is **Information Security in Cyber Security**.

To strengthen this foundation, I should continue learning:

1. CIA Triad in depth
2. Risk Management Basics
3. Asset Classification
4. Threats and Vulnerabilities
5. Networking Fundamentals
6. Authentication and Authorization
7. Security Policies and Controls

##

## 💼 Critical Thinking Question 

### Question

A company reports that customer records were altered without authorization. The records are still accessible, and no data appears to have been stolen.

Which part of the CIA Triad has been affected, and how would you investigate as a SOC Analyst L1?

### Answer Concept

The primary concern is **Integrity** because the data has been modified without authorization.

My investigation approach would be:

1. Review logs to identify who modified the records.
2. Determine when the changes occurred.
3. Verify whether the changes were authorized.
4. Check for compromised accounts or suspicious access.
5. Review related system events and alerts.
6. Escalate findings according to incident response procedures.

The goal is to identify the source of the modification, assess business impact, and help restore trust in the affected data.

##

## Final Reflection

This room taught me that cybersecurity is not just about technology. The ultimate objective is protecting information and ensuring it remains confidential, accurate, and available.

As an aspiring SOC Analyst L1, understanding the relationship between Information Security and Cybersecurity provides a strong foundation for every future topic I will learn, from networking and log analysis to threat detection and incident response.
