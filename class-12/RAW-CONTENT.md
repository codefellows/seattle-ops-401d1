
#### Day 12 - Intrusion Detection and Prevention Systems (IDS/IPS)

  1. Discussion
    1. Article: [Rapid7 - The Pros and Cons of Network Intrusion Detection Systems](https://blog.rapid7.com/2017/01/11/the-pros-cons-of-intrusion-detection-systems/)
  2. Lecture
    1. Why use IDS, IPS, or HIDS?
      1. Detect and prevent intrusion

    2. What is IDS/IPS?
      1. Network intrusion detection system (IDS)
        1. Detective security control
        2. Finds intruder activity on the network and raises alerts
        3. Often included on the perimeter firewall UTM device
      2. Network intrusion prevention system (IPS)
        1. Same as IDS but also detects and actively prevents intrusion
        2. Example: Snort
      3. Types
        1. Behavioral
        2. Signature-based
    3. What is Snort?
      1. Snort is an open source network intrusion prevention system, capable of performing real-time traffic analysis and packet logging on IP networks. It can perform protocol analysis, content searching/matching, and can be used to detect a variety of attacks and probes, such as buffer overflows, stealth port scans, CGI attacks, SMB probes, OS fingerprinting attempts, and much more.
    4. What is HIDS?
      1. Host-based intrusion detection system (on endpoint)
      2. Example: OSSEC
    5. What is OSSEC?
      1. Open source HIDS
      2. Log-based IDS
      3. Rootkit and malware detection
      4. Active response
      5. Compliance auditing
      6. File integrity monitoring
      7. System inventory
    6. How can we use these systems?

  3. Lab
    1. Deploy Snort on a Ubuntu Linux VM (ref. [Snort example lab](http://webpages.eng.wayne.edu/~fy8421/19sp-csc5290/labs/lab8-instruction.pdf)):
      1. Locate the config file
      2. Write and test a Snort rule that detects when ICMP packets transmitted to its IP from internet and raises an alert to the administrator
      3. Locate the log file
      4. Write and test a Snort rule that detects when a RDP attempt is made to its IP from internet and raises an alert to the administrator

    2. Write rules that detect common types of NMAP scans (ref. [InfosecInstitute](https://resources.infosecinstitute.com/snort-network-recon-techniques/#article))
      1. Write and test a Snort rule to detect aggressive NMAP scanning
      2. Write and test a Snort rule to detect stealth TCP scanning
      3. Write and test a Snort rule to detect decoy scans
    3. Stretch goal:
      1. Adept Snort users should continue down the line of [InfosecInstitute](https://resources.infosecinstitute.com/snort-network-recon-techniques/#article) lab exercises
      2. Students might also tinker with OSSEC
        1. Download and install
        2. Create rules and test them

  4. Assigned Reading
    1. Article - [Medium Blog: What is a VPC?](https://medium.com/tensult/intro-to-vpc-548b69f1bd1f)
    2. Article - [AWS: What is a VPC?](https://docs.aws.amazon.com/vpc/latest/userguide/what-is-amazon-vpc.html)
      1. Read first section only

    3. Slides - [Hardening Resources in AWS](http://www.nwacc.org/programs/conf17/dispensa_slides.pdf)

1.
