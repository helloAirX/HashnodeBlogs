---
title: "How to set up an Elastic Block Store (EBS) on AWS"
datePublished: Tue Dec 26 2023 23:00:00 GMT+0000 (Coordinated Universal Time)
cuid: clt4umc7b00070ajsd0z9351l
slug: how-to-set-up-an-elastic-block-store-ebs-on-aws
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1709067159882/64a9aefc-c815-420a-8aa8-03d6a4d19640.jpeg

---

In this article we will learn how to create and configure an Elastic Block Store volume and also attach it to an EC2 instance.

**Note:** The EC2 and EBS volume must be in the same availability zone.

**We need to first create an EC2 instance**

* Log in to your AWS Console.
    
* Navigate to the EC2 dashboard
    
* Click on *"Launch Instance"* and enter a name for the EC2 E.g. Test Sever.
    
* Choose an Amazon Machine Image (AMI) of your choice. E.g. Amazon Linux
    
* Choose an instance type (Select one within the free tier)
    
* Create a key pair or you can continue without a key pair (Not recommended)
    
* Create a security group or choose the default one
    
* Configure the storage as seen in the image below
    
* Leave everything else as default and click on *"Launch instance"*
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1708898054161/d2489892-1d0f-4ad2-b171-016974d2e599.png align="center")
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1708898086144/388fdedf-b911-4c04-b08e-d4aca0ed5448.png align="center")
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1708898135721/88fe284a-79d0-49f0-9696-26e3fe94d202.png align="center")
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1708898153836/80b96dd5-916a-4d29-8d71-2b990e5354c3.png align="center")
    
    We now need to launch our instance and connect to it and proceed to create an EBS volume and attach it to our EC2
    

**Let's create an EBS Volume**

* In the EC2 dashboard scroll down and click on ***"volumes"*** under Elastic Block Store category.
    
* ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1708899174913/2aaa293f-2629-4bd6-bf2b-21a84c8df15a.png align="center")
    
* Click on ***"create volume"***
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1708899107680/71a0192a-a8b4-41c3-8039-d0391193fd39.png align="center")
    
* Specify the volume type
    
* Specify the size
    
* Specify the availability zone (Same as the EC2 instance we created earlier)
    
* Configure as seen in the image below.
    
* Click on ***"Create volume"***
    
* ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1708899278422/5bca9e61-afa7-429a-82a8-3e1e3d118421.png align="center")
    

**Now Let's attach the EBS volume to the EC2**

* Select the EBS volume we just created .
    
* Click on ***"Actions"*** and then click on ***"Attach volume."***
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1708899660415/99966371-1ba4-4784-b67a-db8b3f2290e7.png align="center")
    
* Click on the instance and choose the instance you wish to attach the volume from the drop down (The EC2 created earlier will show)
    
* Specify the device name for the volume E.g. /dev/sdf
    
* Click on ***"Attach volume"*** to attach the volume to the EC2 instance.
    
* ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1708900395383/1a0f30b5-b5a3-4730-a6fc-6610e127a4da.png align="center")
    

**It's time to connect to the EC2 Instance and mount the EBS**

* Select the EC2 and click on ***"Connect"***
    
* Connect using the EC2 instance connect
    
* Viola! We are connected to the EC2 terminal
    
* ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1708900519130/e50dd124-096a-4eca-b474-fa1e5b40184f.png align="center")
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1708900537473/977d7270-0661-4e33-8508-ff9e1b3fe29a.png align="center")
    
    We need to run some commands on the EC2 terminal
    
    * Use the ***"lsblk"*** command to list the available disk drives
        
    * Once the attached EBS volume has been identified i.e the 100G volume (As seen in the image)
        
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1708900670525/50d0f5f0-925a-4003-a3ca-b54d88a1c826.png align="center")
    
* Use the ***"sudo mkfs -t ext4 /dev/xvdf"*** to format the EBS volume.
    
* ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1708901298079/12742074-2028-4563-8b58-7359b6f67f52.png align="center")
    
    Use the "***mkdir"*** command to create a mount point directory for the volume.
    
* Use ***"sudo mount /dev/xvdf /data"*** to mount the volume at the mount point directory we just created.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1708901604884/70d6a950-603a-458c-8043-6e3e07597c06.png align="center")
    
    Yes! We have successfully mounted the EBS volume!
    
    Now let us navigate to the mounted directory and create a test file to be sure we can write to the EBS volume
    
* Use ***"cd /data"*** to navigate.
    
* Use ***"sudo touch filetext.txt"*** to create a test.
    
* Use ***"ls"*** to list the content of the directory to be sure the file we just created is there
    

You can unmount the EBS volume if needed by using the ***"sudo unmount /data"*** command

**You can also delete the EBS volume by navigating to the dashboard**

* Select the EBS volume
    
* Click on "**Actions"** and click ***"Detach volume"***
    
* ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1709066268319/1d5e9e12-72f1-4752-8822-9f5e8ad5da8d.png align="center")
    
* Once you are done with the process, Please terminate the EC2 instance to avoid unnecessary charges
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1709066633872/fbcfa30c-32b1-48ee-a769-23fd6ed734c7.png align="center")
    
* Navigate to the EC2 dashboard, select the instance
    
* Click on **"Instance state"** and click on **"Terminate instance"**
    

Viola! We have completed our project.

We have learnt how to configure an EBS volume and attach it to an EC2 instance.