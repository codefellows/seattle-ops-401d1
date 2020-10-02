#### Day 11 - Network Packet Analysis with Wireshark

  1. Notes
    1. Wireshark is used in a wide range of scenarios and not strictly for security reasons. However, this tool is so versatile it has major applications in both offensive and defensive security, where it can be used to view packets in their entirety. This is a very useful ability that you may also discover on other network appliances, especially UTMs. Because Wireshark, like NMAP, is a ubiquitous security tool featured in security certifications like CEH, it will help a student&#39;s career to get a jumpstart on it here.
    2. Video - [Intro to Wireshark Basics](https://www.youtube.com/watch?v=jvuiI1Leg6w)
    3. Article - [Using Wireshark to steal passwords](https://blog.packet-foo.com/2016/07/how-to-use-wireshark-to-steal-passwords/)
    4. Advanced analysis challenges at [http://www.malware-traffic-analysis.](http://www.malware-traffic-analysis.net/)[net](http://www.malware-traffic-analysis.net/)[/](http://www.malware-traffic-analysis.net/)
  2. Announcements
  3. Code Review
  4. Daily Systems
  5. Warmup Questions
    1. What is a packet?
  6. Lecture
    1. Why perform network packet analysis?
      1. Sniffing traffic
      1. Defensive security
      2. Offensive security

    2. What is a packet composed of?
    3. What is involved in analyzing a packet?
      1. Stages of a network session
        1. SYN \&gt; SYN/ACK \&gt; ACK
      2. HTTP post codes
        1. HTTP GET
        2. HTTP OK
      3. What is &quot;promiscuous mode&quot;
        1. Wireshark default setting - Captures everything.
      4. FTP vs SFTP
    4. How do we use Wireshark to analyze a packet?
      1. Install Wireshark
      2. View current connections

  1. Lab
    1. Perform **network packet analysis** (For instructor only: ref. [Intro to Wireshark Basics](https://www.youtube.com/watch?v=jvuiI1Leg6w))
      1. Each student downloads and installs Wireshark
      2. Break class into teams of two
      3. Point Wireshark to your computer&#39;s active network connection
      4. Tasks will increase in difficulty:
      1. Lab scenario 1
          1. CHALLENGE
          1. Send an ICMP packet to 8.8.8.8 and capture the packet with Wireshark. Take a screenshot of your ICMP packet and paste to your deliverable
      2. Lab scenario 2
          1. CHALLENGE
          1. Use Wireshark to record an HTTP GET request to [https://1112.net/lastpage.html](https://1112.net/lastpage.html) to capture the HTML text and tag contents of the page. Take a screenshot of your HTTP OK packet alongside your browser&#39;s inspection dump and paste into your deliverable.
          2. SOLUTION
          1. After navigating to the page, turn on recording and hit refresh on the browser. Stop recording.
          2. Compare the inspected site contents with the HTTP OK packet contents; they should match.
          3. Right click a packet and &quot;Follow TCP Stream&quot; to show entire conversation with site
          4. After closing you should be able to see the entire SYN/ACK handshake process on all packets
      3. Lab scenario 3
          1. CHALLENGE
          1. Deploy an FTP server external to your PC. Create an account with credentials you&#39;ve never used before. Dumb credentials are fine.
          2. Using Wireshark, demonstrate why FTP is not a secure protocol.
          2. SOLUTION
          1. Bring up the FTP login SSH CLI.
          2. Turn on Wireshark packet capture recording.
          3. Login to the FTP with credentials.
          4. Stop Wireshark recording.
          5. Packets will contain credentials.
          6. Save a screencap of your credentials (assuming not shared/private to your accounts) to the deliverable.

      1. Students navigate to [http://www.malware-traffic-analysis.net/](http://www.malware-traffic-analysis.net/)
      2. Assign each team a single scenario from Malware Traffic Analysis site
  1. Assigned Reading
    1. Article: [Rapid7 - The Pros and Cons of Network Intrusion Detection Systems](https://blog.rapid7.com/2017/01/11/the-pros-cons-of-intrusion-detection-systems/)

  1.