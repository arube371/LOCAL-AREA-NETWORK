# LOCAL-AREA-NETWORK


Question One (20 Marks)
Focus: IP addressing and subnetting

Given IP address: 172.16.0.0/16

(a) Identify class

(b) Identify network portion and host portion

(c) Calculate number of subnets and hosts per subnet

(d) Find the new subnet mask for 172.16.0.0/17

(e) Calculate network and broadcast addresses for 172.16.0.17

(f) Determine the range of valid host addresses.

Question Two (20 Marks)
Focus: Network security and firewalls

Scenario: Small Business Ltd wants to secure its network.

(a) Discuss different types of network attacks.

(b) Evaluate security practices for protection.

(c) Discuss firewall techniques for network access control.

(d) Explain network security framework for the company.

Question Three (20 Marks)
Focus: Binary, hexadecimal and IPv6 addressing

Convert and interpret:

(a) Convert binary → decimal (e.g., 10100001.00000000.00000001.00000001)

(b) Subnet mask conversion

(c) IPv6 representation (e.g., #fe80::290:5cff:fe21:637f)


QUESTION ONE (20 Marks)
Topic: IP Addressing and Subnetting

You’re given:

IP address = 172.16.0.0/16

Summary of tasks:
Identify IP class:

172.16.0.0 falls in Class B (range: 128.0.0.0 – 191.255.255.255).

Default subnet mask: 255.255.0.0

Network and host portions:

Network: first 16 bits (172.16)

Host: last 16 bits (0.0)

Calculate subnets and hosts per subnet:

Depends on borrowed bits.

If subnet mask changes from /16 to /17:

Borrowed bits = 1

Number of subnets = 2¹ = 2

Hosts per subnet = 2¹⁵ - 2 = 32,766

Find new subnet mask for /17:

255.255.128.0

Network & broadcast addresses for 172.16.0.17:

Network: 172.16.0.0

Broadcast: 172.16.127.255

Range of valid hosts:

172.16.0.1 → 172.16.127.254


QUESTION TWO (20 Marks)
Topic: Network Security and Firewalls

Scenario: A small business wants to protect its data and network.

Summary of tasks:
Types of network attacks:

Malware (viruses, worms, trojans)

Phishing and social engineering

Denial of Service (DoS)

Man-in-the-middle

Spoofing, sniffing, password attacks

Security practices:

Use strong passwords & authentication

Regular system updates

Use of antivirus software

Encryption of sensitive data

Employee cybersecurity training

Firewall techniques:

Packet filtering

Stateful inspection

Proxy firewall

Next-generation firewalls (NGFW)

Access Control Lists (ACLs)

Network security framework:

Policy & risk management

Prevention, detection, response

Regular auditing and monitoring

Backup and disaster recovery planning


QUESTION THREE (20 Marks)
Topic: Binary, Hexadecimal & IPv6 Conversion

You’re asked to convert, interpret, and explain binary and hexadecimal addresses.

Summary of tasks:
Binary to Decimal conversion:
Example:

10100001.00000000.00000001.00000001
→ 161.0.1.1

Subnet mask conversion:

Example: 11111111.11111111.11100000.00000000
→ 255.255.224.0 (/19)

IPv6 Addressing:
Example: #fe80::290:5cff:fe21:637f

IPv6 uses hexadecimal notation

Allows 128-bit addresses

Includes link-local, global unicast, multicast, etc.

Section	Key Focus	Core Skills Tested
Q1	IP Addressing & Subnetting	Classful & CIDR addressing, host/subnet calculation
Q2	Network Security	Attacks, firewalls, best practices
Q3	Address Conversion	Binary, decimal, IPv6 understanding
Would you like me to make a ready-to-print summary sheet (PDF) of this exam for quick revision (one page format)?

Thought for 10s
Great — here’s a clear, fully worked solution to Question 1 (all subparts) using the given IP 172.16.0.0/16. I’ll show the reasoning and intermediate binary where helpful.

Question 1 — Given IP: 172.16.0.0/16
(a) Identify the IP class
172.16.0.0 is in the range 128.0.0.0 – 191.255.255.255 → Class B.

Default mask for Class B: 255.255.0.0 (i.e. /16).

(b) Network portion and host portion
With /16 the network portion = the first 16 bits → corresponds to 172.16 (i.e. 172.16.0.0 network).

Host portion = last 16 bits → the .0.0 part (16 bits available for hosts).

(c) Number of subnets and hosts per subnet
We can answer this for two cases: (1) using the default /16 and (2) when subnetted to /17 (the exam asks about /17 later).

Case 1 — Default /16 (no extra subnetting):

Host bits = 32 − 16 = 16

Usable hosts per network = 2¹⁶ − 2 = 65,534 (subtract network & broadcast)

Case 2 — Subnet mask /17 (one bit borrowed from host portion):

New mask = /17 (so borrowed bits = 1 from host portion)

Number of subnets created from /16 → 2^(borrowed bits) = 2¹ = 2 subnets.

Host bits remaining = 32 − 17 = 15

Usable hosts per subnet = 2¹⁵ − 2 = 32,766

(d) New subnet mask for 172.16.0.0/17
CIDR: /17

Dotted decimal mask: compute:

/16 = 255.255.0.0

/17 adds one 1 to the third octet: binary mask = 11111111.11111111.10000000.00000000

So dotted decimal = 255.255.128.0

Binary mask shown:

/17 = 11111111.11111111.10000000.00000000
     255.255.128.0
(e) For the host address 172.16.0.17 (assuming /17), calculate the Network and Broadcast addresses (and show reasoning)
We have /17 → subnet block size in the third octet = 128 in the third octet (because mask 255.255.128.0). Subnet ranges for the 172.16.0.0/16 space subdivided by /17:

Subnet 0: 172.16.0.0 — 172.16.127.255

Subnet 1: 172.16.128.0 — 172.16.255.255

Given IP = 172.16.0.17 → it lies in the first /17 subnet (172.16.0.0 to 172.16.127.255).

Network address = 172.16.0.0

Broadcast address = 172.16.127.255

(You can also compute: block size = 2^(8 − 1) in the 3rd octet = 128 → subnets start at 0, 128, 256(=wrap).)

(f) Range of valid (usable) host addresses in that /17 subnet
First usable host = network + 1 = 172.16.0.1

Last usable host = broadcast − 1 = 172.16.127.254

So the usable host range is:
172.16.0.1 → 172.16.127.254

Quick summary (numbers)
IP class: B

Default mask: 255.255.0.0 (/16)

If kept /16: 65,534 usable hosts per network.

If subnetted to /17:

New mask: 255.255.128.0 (/17)

Number of subnets (from original /16 → /17): 2

Usable hosts per /17 subnet: 32,766

For 172.16.0.17 (in /17):

Network: 172.16.0.0

Broadcast: 172.16.127.255

Usable hosts: 172.16.0.1 – 172.16.127.254

If you want, I can:

show these addresses in binary, or

produce a small table of subnets (the two /17 blocks) ready for printing, or

solve follow-up variations (e.g., subnet to /19 or /20 and compute subnets/hosts). Which next?

You said:
Solve question 2
ChatGPT said:

Thought for 5s
Great — here’s a complete, exam-style solution to Question 2 with clear explanations and practical recommendations for ABC Ltd. I split it by sub-parts and include examples and specific measures the small business can use.

Question 2 — Network security for ABC Ltd (full solution)
Scenario reminder: ABC Ltd operates an online retail store and stores sensitive customer data. It has recently faced security challenges in its network infrastructure.

(a) Discuss different types of network attacks and explain how each attack works. (≈5 marks)
Malware (virus, worm, trojan)

How it works: Malicious software is delivered (email attachment, download, USB). Viruses attach to files, worms self-replicate across networks, trojans hide as legitimate programs.

Impact: Data theft, disruption, persistence/backdoors.

Phishing & social engineering

How it works: Attackers trick employees/customers into revealing credentials or clicking malicious links via fraudulent emails, sites, or calls.

Impact: Credential theft, financial loss, unauthorized access.

Denial of Service (DoS) / Distributed DoS (DDoS)

How it works: Attackers flood a server or network with traffic (single source or many botnet sources) to exhaust resources and make services unavailable.

Impact: Downtime, lost revenue, reputational damage.

Man-in-the-Middle (MitM)

How it works: Attacker intercepts communication between two parties (e.g., via ARP spoofing, rogue Wi-Fi) and can eavesdrop or alter data.

Impact: Data interception, session hijacking, credential theft.

IP/MAC Spoofing and Session Hijacking

How it works: An attacker forges IP or MAC addresses to masquerade as a trusted host or hijack a session token.

Impact: Unauthorized access, bypassing simple access controls.

Sniffing / Eavesdropping

How it works: Passive capture of network traffic using tools (on insecure networks or via compromised switches).

Impact: Exposure of unencrypted credentials and private data.

Brute-force and credential attacks

How it works: Automated attempts (password guesses) or credential stuffing (reused passwords from breaches).

Impact: Account compromise, privilege escalation.

SQL injection / web application attacks (relevant to online retail)

How it works: Malicious input submitted to web forms or APIs that manipulate backend SQL, allowing attacker to read/modify the database.

Impact: Data breach, theft of customer records, unauthorized transactions.

(b) Evaluate best practices for securing ABC Ltd’s small business network against these attacks. (≈5 marks)
Technical controls

Network segmentation

Separate public web servers (DMZ) from internal systems (database, admin). Limits lateral movement if one segment is compromised.

Firewalls & perimeter defenses

Use a firewall to control inbound/outbound traffic; implement ACLs to restrict unnecessary services and ports.

Intrusion Detection/Prevention (IDS/IPS)

Deploy IDS/IPS to detect and automatically block suspicious traffic patterns (signatures & anomalies).

Encryption

Use TLS (HTTPS) for all customer-facing services and encrypt sensitive data at rest (e.g., customer PII, payment data). Use VPNs for remote admin access.

Strong authentication & MFA

Require multi-factor authentication (MFA) for all staff, especially for admin and payment systems. Enforce strong password policies.

Regular patching & asset management

Maintain an inventory of devices and apply OS/application patches promptly to close known vulnerabilities.

Endpoint protection

Install reputable anti-malware/EDR on servers and endpoints to detect ransomware and advanced threats.

Secure development practices

Implement input validation, parameterized queries, and regular code reviews to prevent SQL injection and XSS in the web store.

Backups & recovery

Regular offline/offsite backups of critical data, tested restore procedures, and immutable backups to recover from ransomware.

DDoS mitigation

Use cloud-based DDoS protection or a scrubbing service for the public website and APIs.

Organizational controls
11. Security policies & access control
- Clear policies for least privilege access, account lifecycle (onboarding/offboarding), and role-based access control.

Employee training & phishing simulations

Regular awareness training and simulated phishing to reduce social engineering risk.

Logging, monitoring & incident response

Centralized logging (SIEM where possible), regular review of logs, and an incident response plan with roles and communication steps.

Vendor and third-party risk management

Assess and monitor hosting/payment providers; ensure PCI compliance if handling card payments.

Practical prioritized roadmap for ABC Ltd

Immediate: Enforce MFA, patch critical servers, deploy web TLS, enable backups.

Short term (weeks): Network segmentation, endpoint protection, firewall rules tightened.

Medium term (months): IDS/IPS, security policies, staff training, incident response plan.

(c) Explain the AAA framework (Authentication, Authorization, Accounting) and how services can help manage access control on ABC Ltd’s network devices. (≈5 marks)
1. Authentication

Definition: Proving identity (who you are).

Examples: Passwords, MFA (SMS/Authenticator app), certificates, SSH keys.

For ABC Ltd: Use centralized authentication (RADIUS, TACACS+, LDAP/Active Directory) for employees and admins so credentials are managed centrally and can be revoked quickly.

2. Authorization

Definition: Determining what an authenticated user is allowed to do (permissions).

Examples: Role-based access control (RBAC), ACLs on routers/switches, application permissions.

For ABC Ltd: Implement least-privilege — e.g., web app admins can deploy code but cannot access payment DB unless explicitly authorized. Use network device role profiles (admin vs. read-only).

3. Accounting (auditing / logging)

Definition: Recording actions for auditing, forensics, and billing.

Examples: Syslog records, RADIUS/TACACS+ accounting, SIEM alerts, access logs.

For ABC Ltd: Enable logging of administrative logins, configuration changes, and access to sensitive systems. Retain logs in a secure, tamper-evident location for incident investigations.

How AAA services help practically

Centralized control: Using RADIUS/TACACS+ integrated with AD/LDAP allows consistent auth and authorization policies across VPNs, Wi-Fi, routers, and switches.

Accountability: Accounting logs show who did what and when — essential for investigating breaches or compliance.

Rapid revocation & onboarding: New hires and terminated staff are managed centrally, avoiding orphaned accounts on devices.

(d) Discuss different firewall techniques used to control access to a network. (≈5 marks / 4 marks as in paper)
Packet Filtering Firewall (stateless)

How it works: Inspects packet headers (IP, port, protocol) and applies rules to allow/deny.

Pros: Fast, simple.

Cons: Cannot track connection state or inspect payloads; vulnerable to spoofing.

Stateful Inspection Firewall

How it works: Tracks connection state (TCP handshake) and makes decisions based on state and context.

Pros: Better at blocking forged packets and ephemeral ports misuse.

Cons: More resource use; still limited at application layer.

Proxy (Application-Level) Firewall

How it works: Acts as an intermediary (proxy) for traffic at the application layer (HTTP, FTP). Can inspect payloads and enforce application policies.

Pros: Deep inspection, content filtering, better logging.

Cons: Greater latency and resource overhead.

Next-Generation Firewall (NGFW)

How it works: Combines stateful inspection with deep packet inspection, application awareness, intrusion prevention, and often TLS inspection.

Pros: Granular controls per application/user, integrated threat intelligence.

Cons: Cost and complexity; needs tuning.

Unified Threat Management (UTM)

How it works: A bundled device that offers firewall, antivirus, IPS, web filtering, VPN in one box (popular for small businesses).

Pros: Easy to manage, cost-effective for small setups.

Cons: Single point of failure; may be less flexible than best-of-breed solutions.

Circuit-level gateways

How it works: Operates at the session layer, validating TCP/UDP sessions without inspecting payload content (e.g., SOCKS).

Pros: Efficient for some proxy use.

Cons: Limited application insight.

Which to use for ABC Ltd (recommendation):

For a small online retailer: a managed NGFW or UTM at the perimeter (with web filtering, IPS, and TLS inspection) plus host-based firewalls on servers. Place public web servers in a DMZ with restrictive inbound rules; allow only required ports (HTTP/HTTPS) to web servers and only the database server to accept connections from the web server IPs.

Short concluding recommendations (practical checklist)
Enforce MFA and strong passwords for all staff.

Segment network: DMZ for web servers, separate admin & POS networks.

Use HTTPS/TLS, encrypt sensitive data at rest.

Deploy NGFW/UTM with IDS/IPS and centralized logging.

Implement AAA using RADIUS/TACACS+/AD and enable accounting.

Keep software patched, run regular backups, and train staff on phishing.

Have an incident response plan and test recovery procedures.

If you want, I can:

turn this into an exam-style answer with point allocations and concise wording for quick marking, or

create a checklist/one-page action plan ABC Ltd can implement this week. Which would you prefer?




No file chosenNo file chosen
ChatGPT can make mistakes. Check important info.
