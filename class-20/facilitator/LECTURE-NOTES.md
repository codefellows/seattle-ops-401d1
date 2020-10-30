# Lecture Notes Class 20

Today we're holding off on any new assignments to allow student teams to complete Midterm Project Prep #4, which is their project plan in their PM tool.

## Today's Outline

- Course Overview
  - Review where we're at and talk about what we're going to do today.

- Review: Class 19 Lab
  - Budget about 30 mins to go over Lab: Class 18.

- How to setup and access HackTheBox
  - This chunk of time is basically a wildcard for something fun and relevant that students want to do in class together.
  - Pull up your reference notes on [How to get a HackTheBox Invitation](https://codeburst.io/hack-the-box-how-to-get-invite-code-56e369fc8dae).
    - Follow these steps to gradually clue students into how to get an invitation. Keep this an in-class workshop.
  - After students are logged in, show them how to establish a VPN connection to their target box from a Kali Linux VM.
    - On Kali Linux: 
      - Download the VPN connection pack from HTB > Main > Dashboard > VPN Connection.
      - Install OpenVPN.
        - `sudo apt update`
	- `sudo apt install openvpn`
      - Connect to HackTheBox using OpenVPN: `sudo openvpn #{username.ovpn}`
      - `ip a` will show you that you've been assigned a new IP address over the tunnel.
      - From HackTheBox site, "Join" a machine. 
        - Example machine we can use is "Buff".
	- Verify by pinging the machine.
	- Now we can do fun stuff like Nmap Intensive Scan against the target system.
	- Solution writeups in case students want to go further:
	  - [Writeup 1](https://hackingwebservice.wordpress.com/2020/07/29/hackthebox-walkthrough-buff-machine/)
	  - [Writeup 2](https://medium.com/@romnenko/htb-buff-writeup-f6f94f66c24d)

- Review: Term 1
  - What is information assurance?
  - What is a security audit?
  - If a business has no security standard, what is a good one to start with?
    - NIST Cybersecurity Framework
  - What compliance deals with credit card information?
    - PCI-DSS
  - You need to quickly audit a client company against a specific NIST standard. What do you do?
    - CSET
  - What kind of system can we use to monitor systems uptime in an environment?
    - ISCM, e.g. Nagios
  - What is privilege creep?
  - What is SSO?
  - What is (and is not) MFA?
    - Have, Are, Know
  - How can we protect data at rest?
    - FDE, Single file encryption
  - How can we protect data in motion?
    - SSL, TLS, PGP, DLP
  - Explain public key encryption.
    - Example OpenSSL
  - What is PKI? Give an example.
    - HTTPS
  - What are some documents associated with a data security policy?
    - AUP
    - BYOD policy
  - What network port handles encrypted web traffic? Unencrypted web traffic?
  - What does Wireshark do?
    - Packets can be sniffed, for better or worse
  - What is promiscuous mode?
  - What is PCAP/WinPCAP?
  - What is traffic mirroring?
  - What is an IPS and an IDS?
  - How is encryption used offensively?
    - Evading detection
    - Ransomware (denial of service)
  - What is risk? How can we calculate and define risk?
    - Quantitative: ALE = SLE x ARO
    - Qualitative: DREAD
  - Why do we care about threats?
  - What is threat modelling?
    - Cyber Kill Chain, DFD, STRIDE
  - Why do we care about automation in security?
  - What languages are security tools written in?

- Looking ahead: Term 2
  - Break down the term 2 gameplan, the tools in **bold** have received special callouts from security industry professionals and come especially recommended for Junior SOC professionals.
    - Week 6: Incident Response
      - **SIEM**
	- Example: Splunk
      - **ELK Stack**
	- Security Onion is an all-in-one VM that contains the entire ELK (Elasticsearch, Logstash, and Kibana) stack.
       - **[SOAR platforms](https://www.criticalstart.com/what-is-soar/):**
	  - Examples: Siemplify, LogRhythm
	  - Security Orchestration, Automation, and Response are technologies that allow orgs to monitor, define, prioritize, and drive incident response activities. More advanced than SIEM alone.
	  - SOAR combines Security Orchestration and Automation (SOA), Threat Intelligence Platforms (TIP), and Incident Response Platforms (IRP) together to manage security threats, and it can eliminate much of the manual data collection process.
	  - One-stop shop for analysis and development of automated responses to threats. Different from a SIEM in that it features the latter.
    - Week 7: Malware and Appsec
      - **VirusTotal**
	- Malware signature repository
      - **[Yara](https://blog.malwarebytes.com/security-world/technology/2017/09/explained-yara-rules/)**
	- Developing custom rules to detect malware
    - Week 8: Vulnerability Analysis
      - **Nessus**
      - **Burp Suite**
      - OWASP ZAP
      - Social Engineering
    - Week 9: Penetration Testing
      - Target evaluation
      - Evasion
      - Exploitation
      - Reporting
    - Week 10: Final Project
  - Tools used in the modern SOC
 
- Midterm Project Kickoff

That's it! Happy Friday and have a great weekend! We'll see you in project week.

