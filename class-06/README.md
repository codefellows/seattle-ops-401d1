# Data file encryption and hashing

## Overview

Today you will learn how to assure (and attack) confidentiality and integrity at the single-file level. You will practice the exfiltration and transmissions of hashed files. If the organization needs to protect sensitive information, the security professional should be prepared with solutions to facilitate the confidentiality and integrity of a given data.

## Learning Objectives

### Students will be able to

#### Describe and Define

- Purpose and application of hash algorithms
- Hash algorithms
  - MD5
  - SHA-1
  - SHA-256
- Password cracking tools and techniques
  - Dictionary attack
  - Hybrid
  - Rainbow Table

#### Execute

- Hash dump various OS password files
- Hash dump a SQL Server DB
- Decode various hashes using password cracking tools

## Today's Outline

- Course overview
- Review: Class 05 Lab
- Review: Class 05 Ops Challenge
- Demo: Class 06 Ops Challenge
- Discussion: Data file encryption and hashing
- Lecture: Data file encryption and hashing
- Demo: Data file encryption and hashing

## Resources

### Downloads

- [Microsoft SQL Server Management Studio 18.6 - 535MB download](https://docs.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms?view=sql-server-ver15)

### References

- [Linux SFTP Command](https://www.computerhope.com/unix/sftp.htm)
- [How to set up an SFTP server on Linux](https://www.techrepublic.com/article/how-to-set-up-an-sftp-server-on-linux/)
- [How to Use Linux SCP Command](https://linuxhint.com/linux_scp_command/)
- [How to Unshadow the file and dump Linux password Beginner’s Guide](https://www.cyberpratibha.com/unshadow-the-file-and-dump-linux-password/)
- [How to Crack Passwords with John the Ripper](https://medium.com/@sc015020/how-to-crack-passwords-with-john-the-ripper-fdb98449ff1)
- [Microsoft: AdventureWorks sample databases](https://docs.microsoft.com/en-us/sql/samples/adventureworks-install-configure?view=sql-server-ver15&tabs=ssms)

## Feature Tasks and Requirements

### Part 1: Staging

Prepare the following operating systems for today's lab:
- Deploy a Linux VM on a cloud provider of your choosing. Ubuntu Linux 20.04 Focal Fossa works fine for this.

  > Tip: AWS Lightsail has some very fast, easy Linux AMIs to spin up for this segment of the lab.

- In your Linux VM install OpenSSH
- In Microsoft Azure, deploy the AdventureWorks sample SQL database
- On your local PC install Microsoft SQL Server Management Studio (SSMS) and establish connectivity to your AdventureWorks SQL DB.

The remaining lab requirements will be unlocked at noon on Class-06.
