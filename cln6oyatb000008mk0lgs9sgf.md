---
title: "How to launch AWS EC2 Instance (Windows)"
datePublished: Sun Nov 27 2022 23:00:00 GMT+0000 (Coordinated Universal Time)
cuid: cln6oyatb000008mk0lgs9sgf
slug: how-to-launch-aws-ec2-instance-windows
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1667646526642/ac26ddAmL.png
tags: cloud, ec2, aws, devops, ec2-instance

---

Hello!

Today we will be launching a Windows EC2 instance using the AWS management console.

**Step 1**

Log in to the AWS account and navigate to the EC2 dashboard Click on Launch instance

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1666819639800/WFek6AlMm.png align="left")

**Step 2**

Here you will be required to input some details and make some selections. Choose a name for your instance Selection an AMI in this case we will choose windows

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1667648837003/g3TM8Gj46.png align="left")

**Step 3**

This is where you select your RAM, CPU, Hard disk etc Select the t2 micro (it's within the free tier)

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1667648940477/CqP62XHEx.png align="left")

**Step 4**

Select an existing key pair or create a new one. for this purpose, we will create a new key pair

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1667649114697/IlAycN6Xd.png align="left")

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1667649165232/I7PYCax7R.png align="left")

Your new keypair has been created

**Step 5**

Leave everything as default Here a default VPC, Security group has been selected by default Leave the storage settings as default too

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1667649306026/ulyu4E62-.png align="left")

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1667649471239/lxDBoLju-.png align="left")

**Step 6**

Here is a summary of our instance Select launch instance

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1667649539345/uN1RKbtQR.png align="left")

Our instance has been launched successfully, Click view all instance

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1667649701717/pYa6dsPgE.png align="left")

**Step 7**

Our instance is running

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1667650115249/P1lMoVJIk.png align="left")

Now let's connect to our instance Click on Connect

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1667650266513/OEpK1QOPh.png align="left")

\*\*Step 8 \*\*

Select RDP Client (Remote Desktop Protocol Client)

Download the RDP file Now we need our key pair so click on Get password

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1667650520149/FrxLa74ni.png align="left")

**Step 9**

We need to upload the key pair we created earlier upload the keypair and click on decrypt

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1667650730541/aWGSUwpus.png align="left")

Now our password is available for use after decryption

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1667650919699/TRysPyCOU.png align="left")

**Step 10**

Launch the RDP client we downloaded earlier

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1667651146272/4F0HT0vud.png align="left")

Click on Connect Enter the password we generated

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1667651254102/RLOO9sPPM.png align="left")

Click yes

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1667651292683/T15BIe7eq.png align="left")

Yes! We have successfully connected to our Windows instance Now our Windows environment is ready

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1667651630808/ycSHpaDo_.png align="left")