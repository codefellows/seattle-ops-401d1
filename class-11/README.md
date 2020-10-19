# Network Packet Analysis with Wireshark

## Overview

Wireshark is used in a wide range of scenarios and not strictly for security reasons. However, this tool is so versatile it has major applications in both offensive and defensive security, where it can be used to view packets in their entirety. This is a very useful ability that you may also discover on other network appliances, especially UTMs. Because Wireshark, like NMAP, is a ubiquitous security tool featured in security certifications like CEH, it will help your career to get a jumpstart on it here. Today you will perform network packet analysis using Wireshark.

## Learning Objectives

### Students will be able to

#### Describe and Define

- Sniffing
- Stages of a network session
  - SYN > SYN/ACK > ACK
- HTTP methods
  - HTTP GET
  - HTTP OK
- Network adapter promiscuous mode
- FTP
- SFTP

#### Execute

- Perform network packet analysis with Wireshark

## Today's Outline

- Course overview
- Review: Class 10 Lab
- Demo: Class 11 Ops Challenge
- Discussion: Network Packet Analysis with Wireshark
- Lecture: Network Packet Analysis with Wireshark
- Demo: Network Packet Analysis with Wireshark

## Resources

### Downloads

GNS3 will request these files for hosting Kali Linux. These links are available via GNS3 template creation wizard.

- [Kali 2019.3 ISO 2.8GB Download](http://cdimage.kali.org/kali-2019.3/kali-linux-2019.3-amd64.iso)
- [kali-linux-persistence-1gb.qcow2 33.9MB Download](https://sourceforge.net/projects/gns-3/files/Qemu%20Appliances/kali-linux-persistence-1gb.qcow2/download)

## Feature Tasks and Requirements

### Part 1: Staging

Wireshark, a tool used in today's lab, comes bundled with Kali Linux.
- Install Filezilla on your Kali Linux VM and point it to the FTP server at [DLP Test](https://dlptest.com/ftp-test/). Alternatively you may host an FTP server locally if you prefer to connect to that instead.
- To execute part 4, you'll need the ability to deploy Wireshark to a computer that is plugged into a hub or switch along with two other computers. This is achievable either in GNS3, in cloud, or physically.

