---
title: "Launch a WordPress Website in 5 minutes"
datePublished: Sun Mar 12 2023 20:33:55 GMT+0000 (Coordinated Universal Time)
cuid: clf5usmfx000409mkfbaz69w1
slug: launch-a-wordpress-website-in-5-minutes
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1668632348130/vtFT7nAsF.jpg
tags: wordpress, website-design

---

Get your website up and running in 5 minutes with these few steps

Let's get started!

**Step 1**

*   Login to the Amazon console and Launch Lightsail
    
*   Click on create instance
    

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1667661251567/MC08yApSF.png align="left")

**Step 2**

*   Select a Region
    
*   Select an Availability Zone
    

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1667661910101/r89I_P1gX.png align="left")

**Step 3**

*   Choose an instance image
    
*   Select Linux/Unix as the platform.
    
*   Select WordPress as the blueprint.
    

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1667673404569/SOxd4UYSo.png align="left")

**Step 4**

*   Choose an instance plan
    

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1667673660573/L5lZyBs38.png align="left")

**Step 5**

*   Specify a name for the instance
    
    ![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1667678851260/1UHo6BPTc.png align="left")
    
*   Our instance has been launched successfully
    

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1667680554924/TAV_q7rq8.png align="left")

**Step 6**

*   Let's connect to our instance
    
*   Choose the SSH quick-connect icon for your WordPress instance.
    
*   After the browser-based SSH client window opens, enter the following command to retrieve the default application password:
    

***cat $HOME/bitnami\_application\_password***

*   Keep the password displayed on the screen. You use it later to sign in to the administration dashboard of your WordPress website
    

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1667679353049/L6MYTlmtN.png align="left")

**Step 7**

*   Sign in to the admin console of WordPress
    
*   Copy the link below to a web browser
    

```plaintext
http://PublicIpAddress/wp-login.php
```

*   Replace *PublicIpAddress* with the public IP address of your WordPress instance.
    
*   Log in to your instance
    
*   In the username field enter "user"
    
*   In the Password box, enter the default password obtained earlier then login
    

Viola!

You are now signed in to the administration dashboard of your WordPress website where you can perform administrative actions.

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1667680456565/CIwpPCTf7.png align="left")