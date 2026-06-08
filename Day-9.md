
# Room Walkthrough: [Common Attacks](https://tryhackme.com/room/commonattacks)

## 🎯 Day 9 Objective

As part of my SOC Analyst L1 learning journey, this room introduced some of the most common cyber attacks that target both individuals and organizations.

> Before learning advanced detection and incident response, I wanted to understand how attackers typically gain access, spread malware, steal credentials, and compromise systems.

This room combined real-world case studies, practical exercises, and defensive security practices to help me understand both attacks and the controls used to prevent them.

---


### Who is this for?

* SOC Analysts
* Security Analysts
* IT Support Teams
* System Administrators
* Anyone using computers and online accounts

### What is it?

This room introduces common cyber attacks such as:

* Social Engineering
* Phishing
* Malware
* Ransomware
* Password Attacks
* Authentication Abuse

It also covers defensive practices such as MFA, backups, updates, and password managers.

### Where does this apply?

* Corporate networks
* Cloud environments
* Personal devices
* Government systems
* Educational institutions

### When should it be learned?

Before learning advanced monitoring and incident response.

Understanding how attacks happen makes it easier to recognize suspicious activity later.

### Why is it important?

Most cyber incidents start with common attack methods rather than highly sophisticated techniques.

Understanding these attacks helps reduce risk and improve security awareness.

### How does it work?

Attackers often exploit:

* Human behavior
* Weak passwords
* Unpatched systems
* Lack of backups
* Poor authentication controls

Organizations defend against these risks using layered security controls.

---

### What confused me?

Before this room, I thought malware and ransomware were usually delivered through advanced hacking techniques.

What confused me was how often attackers succeed using very simple methods:

* A phishing email
* A malicious USB device
* A weak password
* A missing software update

The Stuxnet case especially surprised me because the target network was isolated from the internet, yet attackers still found a way inside through human behavior.

### What I learned?

Key lessons from this room:

* Social engineering often targets people instead of technology.
* Phishing remains one of the most successful attack methods.
* Ransomware can spread rapidly across vulnerable systems.
* Password hashing protects stored passwords.
* Multi-Factor Authentication adds an important security layer.
* Backups are critical for recovery after an attack.
* Security patches prevent known vulnerabilities from being exploited.

I also learned that many major cyber incidents could have been reduced or prevented through basic security practices.

### How I improved?

Before this room, I focused mainly on attackers and malware.

Now I understand that security is also about reducing opportunities for attackers.

My thinking shifted from:

> "How does malware infect a system?"

to

> "What weakness allowed the malware to succeed?"

This mindset is much closer to how a SOC Analyst investigates incidents.

### Real-World Relevance

In a real enterprise:

* Employees receive phishing emails daily.
* Weak passwords lead to account compromise.
* Unpatched systems create attack opportunities.
* Ransomware can disrupt business operations.
* Missing backups can turn an incident into a disaster.

SOC teams continuously monitor for these threats and help organizations detect and respond before damage spreads.

---

### Task 1: Introduction
[<img width="1200" height="1453" alt="image" src="https://github.com/user-attachments/assets/7dbeb33b-79f4-4e18-8e27-2a1934a3dc74" />](https://www.infosectrain.com/blog/how-to-prevent-the-most-common-cyber-attacks)

**Question:** Let's get started!

**Answer:** No answer required.

**Key Takeaway:** Understanding common attacks is essential before learning detection and incident response.

---

### Task 2: Social Engineering
The manipulation of individuals to divulge sensitive information, through various forms of communication
<img width="1400" height="669" alt="image" src="https://github.com/user-attachments/assets/2c3860f3-074f-427a-a527-4b23b3f57a75" />


**Question:** What was the original target of Stuxnet?

**Answer:** The Iran Nuclear Programme

**Explanation:**

The most important lesson was not the malware itself, but the infection method.

Attackers used malicious USB devices because the target network was isolated from the internet.

**SOC Perspective:** Human behavior can become an attack path even when technical controls are strong.

---

### Task 3: Phishing

<img width="650" height="450" alt="image" src="https://github.com/user-attachments/assets/e38afc48-1a7a-475c-8346-fab21390923e" />
There are three primary types of phishing attacks:

| Attack Type | Definition|
|-------------|------------------------------------------------------------------------------|
|**General Phishing**:|A simple, mass phishing attack which doesn't target anyone in particular, although they may aim for large groups (e.g. PayPal users, or Amazon customers). These large-scale campaigns are usually simple and are generally (but not always) fairly easy to spot as the messages and malicious sites are often not very well crafted and frequently contain many immediately visible errors.|
|**Spearphishing**:|More targeted than general phishing, spearphishing aims for an individual or small group (e.g. employees of a specific company). Spearphishing campaigns are generally better crafted than the correspondence and malicious sites used in general phishing as they are designed to target a particular group, often as part of a more extensive campaign against the target.|
|**Whaling**:|Even more specific than spearphishing, whaling targets high-value individuals (e.g. a C-Suite executive in a target company). The messages are generally extremely well crafted and tend to be very hard to spot.|

**This process is shown in the following diagram:**
<img width="1082" height="744" alt="image" src="https://github.com/user-attachments/assets/948a1364-49c4-4d5e-819d-006a9980920a" />
* The attacker sends out a malicious phishing email campaign

* Prospective victims receive the emails — some of them open the email and click the link

* The victims enter their credentials into the attacker's fake web page

* The web page stores the credentials or sends them directly to the attacker

* The attacker uses the credentials to access the site, thus taking over the victims' accounts

**Question:** What is the flag?

**Answer:** THM{I_CAUGHT_ALL_THE_PHISH}

**Explanation:**

This exercise demonstrated how attackers disguise malicious messages as legitimate communications.

**SOC Perspective:** Many incidents begin with a successful phishing attempt.

---

### Task 4: Malware and Ransomware
Despite the steady advance of antivirus software solutions, malware (and ransomware in particular) is an ever-growing threat.
<img width="1200" height="897" alt="image" src="https://github.com/user-attachments/assets/5928b605-1679-4235-bc97-7a090e4ca411" />

**Question:** What currency did the WannaCry attackers request payment in?

**Answer:** Bitcoin

**Explanation:**

Cryptocurrency provides attackers with a way to receive payments without traditional banking systems.

**SOC Perspective:** Ransomware investigations often involve identifying the infection source and limiting spread.

---

### Task 5: Passwords and Authentication

For better or worse, passwords are an integral part of most authentication systems. We use passwords to protect everything, from our social media accounts to our banking applications. Unfortunately, despite their significant importance, it is still all-too-easy to create and use an insecure password, and even easier to take other actions that lower the overall security of the system.
<img width="433" height="116" alt="image" src="https://github.com/user-attachments/assets/b50ac5ea-91e6-449f-b434-1d3d40c26177" />

**Question:** Look at the "Current Word / Hash" section of the hash cracker.
Notice that for each word in the list you entered, the cracker is creating an MD5 hash of the word then comparing it to the Target Hash. If the two hashes match then the password has been found!
The hash cracker should find the password that matches the target hash very quickly.
What is the password?

**Answer:** TryHackMe123!

**Explanation:**

This task demonstrated password cracking and the importance of password hashing.

**Key Lesson:**

* Plain-text passwords are dangerous.
* Strong hashing improves security.
* Weak passwords are easier to crack.

---

### Task 6: MFA and Password Managers
In the previous task, we looked at some of the common attacks made against passwords and authentication systems. We also looked at what makes a password weak or strong. This task will cover some of the extra steps that you can take to enhance your password security through the use of password managers and multi-factor authentication.
<img width="800" height="1047" alt="image" src="https://github.com/user-attachments/assets/25a91cff-41dc-4d6d-947b-715b48731ec6" />

**Question:** Which should be used as a second authentication factor?

**Answer:** App

**Explanation:**

Authenticator applications are generally more secure than SMS-based authentication because SMS messages can be intercepted or redirected.

**SOC Perspective:** MFA significantly reduces the risk of account compromise.
<img width="666" height="382" alt="image" src="https://github.com/user-attachments/assets/7587c5f4-3a13-4aa4-9a60-e63045f44590" />

---

### Task 7: Public Network Safety
The internet plays a gargantuan role in modern life, with most people being connected in some way virtually constantly. As such, most public spaces (e.g. cafés, restaurants, public transport) are fully equipped with public WiFI to let people catch up on email (or, equally likely, play the latest hit mobile game). What many people don't realise is that expecting public WiFi to be available can prove to be very dangerous indeed.
<img width="941" height="407" alt="image" src="https://github.com/user-attachments/assets/ebb20705-0ddd-461e-ade9-546cd69d44a4" />

**Key Takeaway:**

Public networks should never be automatically trusted.

Sensitive activities should be performed using secure connections and appropriate protections.
<img width="1168" height="2560" alt="image" src="https://github.com/user-attachments/assets/6fd4b8c3-aed5-4225-82e4-4060e606225e" />

---

### Task 8: Backups
Backups are arguably the single most important defensive measure you can take to protect your data. No matter what happens, if you have taken appropriate steps to back your information up, you will always be able to recover almost regardless of the severity of the damage.

Whether the data in question is all-important business-critical data at work or the family photos at home, backups are a simple insurance measure that pays for itself many times over should the worst come to pass.
<img width="1715" height="875" alt="image" src="https://github.com/user-attachments/assets/f3a2c6ae-b701-4389-ada8-9c298d63e6a3" />
* You should always keep at least three up-to-date copies of your data; this can include the original copy, but all copies must be maintained.

* Backups should be stored on at least two different storage mediums; for example: a cloud backup and a USB device. This can include a hard drive on your PC.

* One (or more) backups should be stored "off-site". Cloud services such as Google Drive are ideal for personal use in this regard.
* 
**Question:** What is the minimum number of up-to-date backups?

**Answer:** 3

**Question:** How many should be stored in another location?

**Answer:** 1

**Explanation:**

This follows the well-known backup strategy designed to improve recovery after system failure or ransomware attacks.

---

### Task 9: Updates and Patches
Updates are an essential part of the software development lifecycle; they allow developers to add new features, fix bugs and otherwise simply alter aspects of the product. When vulnerabilities are discovered in software, the developers usually release special updates called patches that contain a fix for the vulnerability or otherwise "patch" the security issue.
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/f2a4ba12-9809-4c7e-aac1-b435afe959f1" />

Unfortunately, all software eventually loses support from its maintainers, becoming deprecated and no longer receiving updates (e.g. Windows 7) — this is referred to as the software being EOL (End Of Life). 
<img width="1350" height="759" alt="image" src="https://github.com/user-attachments/assets/bb88c89d-7681-4ee2-b464-a64ba621d832" />

**Question:** Complete the Blue Room

**Answer:** No answer required.

**Explanation:**

The EternalBlue vulnerability demonstrated how dangerous unpatched systems can become.

WannaCry successfully spread because many organizations failed to install available security updates.

**SOC Perspective:** Vulnerability management is a critical security control.

---

### Task 10: Conclusion
To conclude: there are many different options for a malicious attacker to target both individuals and sweeping groups; however, there are remediations for every attack.
**Key Takeaway:**

Every common attack has defensive controls that can significantly reduce risk when implemented correctly.

---

## 🛡️ SOC Analyst L1: Mindset

### Tricky Connection

Many beginners focus on the malware.

SOC Analysts focus on the attack chain.

For example:

* Malware is not the beginning.
* Ransomware is not the beginning.
* The phishing email, weak password, missing patch, or malicious USB device is often the beginning.

A SOC Analyst learns to identify:

* Initial Access
* Credential Abuse
* Malware Execution
* Lateral Movement
* Impact

Understanding the full attack chain helps investigators find the root cause rather than only the final symptom.

### Next Learning Steps

To strengthen this foundation, I should continue learning:

1. Networking Fundamentals
2. Normal vs Abnormal Network Traffic
3. Windows Event Logs
4. Phishing Analysis
5. Malware Behavior Basics
6. Authentication Logs
7. Incident Response Process
8. MITRE ATT&CK Framework

---

## Critical Thinking

### Question

A user reports that several files on their workstation have suddenly become inaccessible and now display a message demanding payment in Bitcoin.

As a SOC Analyst L1, what would be your first actions?

### Answer Concept

My investigation approach would be:

1. Identify whether ransomware activity is occurring.
2. Isolate the affected workstation from the network.
3. Collect relevant alerts, logs, and indicators.
4. Determine whether other systems show similar activity.
5. Identify the initial infection vector.
6. Escalate according to incident response procedures.
7. Support containment and recovery efforts.

The goal is to prevent further spread, preserve evidence, and help the organization recover safely.

---

## Final Reflection

This room showed me that most cyber attacks do not begin with sophisticated exploits. They often begin with simple mistakes, weak security practices, or unpatched systems.

As an aspiring SOC Analyst L1, this room helped me understand the relationship between common attacks and the defensive controls used to stop them. More importantly, it taught me to think beyond the malware itself and focus on the complete attack chain, which is a critical skill for security investigations.
