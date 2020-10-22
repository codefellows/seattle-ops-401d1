# Ops Challenge: Brute Force Attacks 

## Overview

Many attack techniques exist to circumvent a security defense, such as password-based authentication. One of the classic attack techniques is something called "brute force," where the attack tool repeatedly attempts to authenticate until successful.

Today you will practice compromising a SSH server using brute force tools.

## Resources
- [How to Install SSH on Ubuntu 20.04](https://devconnected.com/how-to-install-and-enable-ssh-server-on-ubuntu-20-04/){:target="_blank"}
- [Brute-force attacks with Kali Linux](https://medium.com/@Pentestit_ru/brute-force-attacks-using-kali-linux-49e57bb89259){:target="_blank"}
- [How To Gain SSH Access to Servers by Brute-Forcing Credentials](https://null-byte.wonderhowto.com/how-to/gain-ssh-access-servers-by-brute-forcing-credentials-0194263/){:target="_blank"}

### Part 1: Staging

First prepare your lab environment.

- Standup your target, a SSH server, locally using a virtualization platform like Virtualbox.
  - For a more "black box" experience today, consider deploying [Metasploitable 2](https://information.rapid7.com/download-metasploitable-2017-thanks.html){:target="_blank"}.
  - Ensure that Kali Linux shares a subnet with your target.
- Identify the following tools on your Kali Linux distribution:
  - Patator
  - THC Hydra
  - Medusa
  - Metasploit
  - BurpSuite
  - Nmap Scripting Engine (NSE)

### Part 2: Attack SSH using Brute Force

Next, try operating these tools and get a feel for their capabilities and limitations.

- Select three of the five tools listed in Part 1. 
- For each tool, use its brute force attac technique to determine the SSH password of your target system.
- Document and screenshot steps taken for your submission.

### Part 3: Reporting

Time to recap and summarize each of your tests. For each test:
- Describe the advantages and disadvantages of using this tool.
- How many authentication attempts did your tool make against the SSH server?
- Share a screenshot of a successful attack you made today and include your thoughts on the tool in a Slack post to the class Slack channel.

## Submission Instructions

1. Create a new blank Google Doc. Include above assignment submission text and images within this Google Doc.
1. Name the document according to your course code and assignment.
   - i.e. `seattle-ops-401d1: Reading 01` or `seattle-ops-401d1: Lab 04`.
1. Add your name & date at the top of the Google Doc.
1. Share your Google Doc so that "Anyone with the link can view".
1. Paste the link to your Google Doc in the discussion field below and share an observation from your experience in this lab.

