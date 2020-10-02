#### Day 6 - Data file encryption and hashing (ref. [HowToGeek](https://www.howtogeek.com/67241/htg-explains-what-are-md5-sha-1-hashes-and-how-do-i-check-them/), [Blog Article](https://www.jscape.com/blog/implementing-the-cia-triad-when-transferring-files-through-the-internet))

  1. Notes
    1. This day is all about how to assure confidentiality and integrity at the single-file level. Students spin up a SFTP/SSH server and perform transmissions of hashed files. If time and skill allow, students should practice password cracking here too.
    2. If the organization needs to protect sensitive information, the security professional should be prepared with solutions to facilitate the confidentiality and integrity of a given data.
  2. Lab Review
  3. Daily Systems
  4. Warmup Questions
  5. Lecture
    1. Why might we need to secure a single file or package?
    2. What tools and techniques can we use to protect data files?
    3. How is this process performed?
      1. Single file confidentiality assurance
      1. Password-encrypting single files
      2. Single file integrity assurance
      1. Why is hashing used in security?
          1. Verify the integrity of a file
          2. Create confidentiality of sensitive information, e.g. passwords
      2. What kinds of hashing are used?
          1. MD5, SHA-1, and SHA-256
      3. How is hashing used?
          1. Demonstrate
          1. Download a file from a provider with a hash
          2. Generate a hash
          3. Compare the hash to the provider&#39;s hash
      3. Single file availability assurance
      1. Offsite/Cloud Backup
      2. Failover system
      4. Data in motion
      1. How SFTP/SSH servers provide file transfer confidentiality
      5. Password cracking
      1. Tools
      2. Techniques
          1. Dictionary Attack
          2. Hybrid
          3. Rainbow Table

    4. Demonstration
      1. In Kali Linux, we&#39;ll create a simple MD5 hash and demonstrate how to attack it

  1. Lab
    1. In Kali Linux, hash a simple string and decode the hash with Kali Linux tools
    2. In a Ubuntu Linux VM, extract the password hash file and attempt to crack the password using tools on Kali Linux
    3. In a Windows 10 VM, extract the password hash file and attempt to crack the password using tools in Kali Linux
    4. In AdventureWorks database (from Ops 301), write a SQL query that associates usernames with password hashes. Then, extract the output and attempt to crack the passwords using tools in Kali Linux.

  1.
