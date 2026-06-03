         
# [Room](https://tryhackme.com/room/hello): [OpenVPN](https://tryhackme.com/room/openvpn)

## 🎯 Objective

As I begin my cybersecurity journey toward becoming a SOC Analyst L1, I decided to start with the OpenVPN room. Before learning advanced security concepts, I wanted to understand how I securely connect to training labs and remote environments. This room helped me learn the basics of VPNs and why they are important in cybersecurity.

> **Day 0 Mindset:** Before attacking, defending, or investigating systems, I need to understand how devices communicate securely across networks.

---

### Who is this for?

* Cybersecurity beginners
* SOC Analyst aspirants
* Network and system administrators
* Anyone using remote labs or secure corporate access

### What is it?

OpenVPN is a VPN (Virtual Private Network) solution that creates an encrypted tunnel between a device and a remote network.

### Where does this apply?

* Corporate remote access
* Security Operations Centers (SOC)
* Cloud environments
* Remote cybersecurity labs such as TryHackMe

### When should I learn this?

* At the beginning of a cybersecurity journey
* Before learning network analysis, packet investigation, and SOC monitoring

### Why is it important?

Without encryption, network traffic can be intercepted or monitored by unauthorized parties. VPNs help protect data confidentiality and secure communication.
<img width="100%" height="50%" alt="image" src="https://github.com/user-attachments/assets/32d69864-64f2-45a9-b913-918fc77ade86" />

### How does it work?

A VPN client uses a configuration file to connect securely to a VPN server. Once connected, traffic travels through an encrypted tunnel, allowing access to remote resources as if the device were part of that network.
<img width="100%" height="50%" alt="openvpn_image" src="https://github.com/user-attachments/assets/d378aecd-1a97-487f-ac7a-d63b94242a28" />

---

### What confused me?

My biggest confusion was understanding:

* How does OpenVPN encryption actually work?
* What exactly is inside the `.ovpn` configuration file?
* Does the configuration file contain passwords or sensitive credentials?
* How does my machine become part of another network after connecting?

Initially, I thought the configuration file was just a simple setup file. After exploring further, I realized it contains important connection details such as:

* VPN server information
* Connection settings
* Encryption parameters
* Certificates or certificate references
* Authentication methods

This made me realize that configuration files should be handled carefully because they may contain information that helps establish trust and authentication with the VPN server.

### What I learned?

Key takeaways from this room:

* VPN stands for Virtual Private Network.
* OpenVPN creates a secure encrypted tunnel between client and server.
* The `.ovpn` file acts as a blueprint that tells the client how to connect.
* Encryption helps protect data from interception while it travels across networks.
* VPNs are commonly used in enterprise environments to provide secure remote access.
* Many cybersecurity platforms use VPNs to allow access to isolated lab environments.

### How I improved?

Before this room, I simply followed connection instructions without understanding what was happening in the background.

After completing the room:

* I understand why VPN connections are required.
* I pay more attention to configuration files and connection settings.
* I started thinking about network trust, authentication, and encryption rather than just "connecting and moving on."

This small mindset shift helped me move from being a user of technology to someone who wants to understand how it works.

### Real-world relevance

In a real enterprise environment:

* Employees use VPNs to access internal resources remotely.
* Security teams connect securely to monitoring systems.
* Administrators manage servers through protected network channels.
* Organizations use VPNs to reduce exposure of internal services to the public internet.

Understanding VPN fundamentals helps SOC analysts investigate authentication logs, remote access activity, VPN-related alerts, and suspicious login events.

---

## 🛡️ SOC Analyst L1: Mindset 

### Tricky Connection

A beginner often asks:

> "How do I connect to the VPN?"

A SOC Analyst asks:

> "Who connected, from where, at what time, and was that connection normal?"

That difference represents the shift from using a technology to analyzing it.

For example:

* Normal user activity → Employee connects from an approved location.
* Suspicious activity → VPN login from an unusual country or at an unusual time.
* Potential compromise → Multiple failed logins followed by a successful connection.

As a future SOC Analyst, I should not only understand how VPNs work but also how VPN activity appears in logs and security monitoring tools.

### Next Concepts to Explore

Since my next room is **"Careers in Cyber"**, the logical learning path is:

1. Cybersecurity Career Paths
2. SOC Analyst Responsibilities
3. Networking
4. Log Analysis Basics
5. SIEM Fundamentals
6. Normal vs. Abnormal Network Traffic

These topics connect directly to entry-level SOC work.

---

## 💼 Critical Thinking Question 

### Question

Your organization uses a VPN for remote access. An alert shows that a user successfully connected to the VPN at 2:00 AM from a country they have never accessed from before. As a SOC Analyst L1, what would you do?

### Answer Concept

First, I would not immediately assume malicious activity.

My investigation process would be:

1. Review VPN authentication logs.
2. Verify the source IP address and geolocation.
3. Check whether the user normally works during those hours.
4. Review previous login history for comparison.
5. Look for multiple failed login attempts before the successful connection.
6. Check if additional suspicious activity occurred after login.
7. Contact the user or escalate according to the incident response process if the activity appears abnormal.

The goal is to collect evidence, validate assumptions, and determine whether the event represents legitimate access or a potential account compromise.

---

### Final Reflection

This room was simple, but it introduced an important foundation. Before learning threat detection, incident response, or SIEM tools, I needed to understand how secure connectivity works.

My biggest takeaway is that cybersecurity starts with understanding networks, trust, and communication. OpenVPN showed me that even a basic connection process has security concepts hidden underneath it, and those concepts directly connect to the daily work of a SOC Analyst L1.
