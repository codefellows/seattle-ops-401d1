#### Day 13 - Cloud Architecture Security

  1. Notes
    1. Today you will configure an AWS Virtual Private Cloud (VPC) to be used for the next couple days to apply your network security skills and knowledge to a cloud environment.
  2. Discussion
    1. Article - [Medium Blog: What is a VPC?](https://medium.com/tensult/intro-to-vpc-548b69f1bd1f)
    2. Article - [AWS: What is a VPC?](https://docs.aws.amazon.com/vpc/latest/userguide/what-is-amazon-vpc.html)
      1. Read first section only

    3. Slides - [Hardening Resources in AWS](http://www.nwacc.org/programs/conf17/dispensa_slides.pdf)

  3. Lecture
    1. Why is cloud security important?
    2. What are some key considerations when securing cloud environments?
      1. Cloud Service Models
      1. Private cloud \&lt;-- _Today&#39;s lab!_
      2. Public cloud
      3. Hybrid cloud

    3. What are the types of cloud services?
      1. IaaS ← _Today&#39;s lab!_
        1. Examples: DigitalOcean, Linode, Rackspace, Amazon Web Services (AWS), Cisco Metapod, Microsoft Azure, Google Compute Engine (GCE)
      2. PaaS
        1. Examples: AWS Elastic Beanstalk, Windows Azure, Heroku, Force.com, Google App Engine, Apache Stratos, OpenShift
      3. SaaS
        1. Examples: Google Apps, Dropbox, Salesforce, Cisco WebEx, Concur, GoToMeeting
    4. Why does cloud service type matter?
      1. Determines user scope of responsibility
    5. What is a Virtual Private Cloud (VPC)?
    6. How do we create a VPC on AWS?
    7. What is AMI hardening and why is it important?
    8. How do we harden AWS AMIs?
      1. Select a trusted AMI as a good foundation
      2. Secure all services on the machine
        1. Patch the OS, applications
        2. Use best practices on all services
      3. Remove unnecessary users
      4. Restrict access to the instance
        1. Use key-based SSH
        2. Remove SSH root completely
      5. Close unnecessary ports

  4. Lab
    1. In today&#39;s lab students will create a VPC, deploy a CentOS VM on it, and take steps to harden CentOS.
    2. Create a VPC
      1. Complete [Introduction to Amazon Virtual Private Cloud (VPC)](https://amazon.qwiklabs.com/focuses/279?parent=catalog)
      2. Topics:
      1. Create an Amazon VPC using the VPC Wizard
      2. Explore the basic components of a VPC including
          1. Public and private subnets
          2. Route tables and routes
          3. NAT gateways
          4. Network ACLs
          5. Elastic IPs

    3. Install AMIs on VPC and harden them
      1. There are CIS-compliant AMIs that are prehardened but for the learning experieince we&#39;ll use regular Ubuntu images for this exercise
      2. Ubuntu AMI hardening (ref. [BobCares Article - AMI Hardening](https://bobcares.com/blog/amazon-linux-ami-hardening/))
        1. Spin up a regular (not pre-hardened) Ubuntu Server 16.04 AMI in AWS EC2 . This one should be free tier.

![](RackMultipart20200908-4-1mqab9e_html_822331489fdb080a.png)

        1. Enable [AWS Security Hub](https://aws.amazon.com/security-hub/getting-started/)
        2. Apply hardening practices to your AMI
          1. Select a trusted AMI as a good foundation
          2. Secure all services on the machine
          3. Remove unnecessary users
          4. Restrict access to the instance
          5. Close unnecessary ports
            1. We&#39;ll use this machine for strictly for SFTP server as an example
    1. Stretch Goal
      1. 45 mins - [Introduction to AWS Identity and Access Management (IAM)](https://amazon.qwiklabs.com/focuses/10408?parent=catalog)
        1. Topics:
          1. Exploring pre-created IAM Users and Groups
          2. Inspecting IAM policies as applied to the pre-created groups
          3. Following a real-world scenario, adding users to groups with specific capabilities enabled
          4. Locating and using the IAM sign-in URL
          5. Experimenting with the effects of policies on service access
    2. Assigned reading
      1. PDF - [AWS: What is Traffic Mirroring?](https://docs.aws.amazon.com/vpc/latest/mirroring/vpc-tm.pdf#traffic-mirroring-how-it-works)

1.
