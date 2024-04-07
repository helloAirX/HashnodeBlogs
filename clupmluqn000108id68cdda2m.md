---
title: "Create an Audio Transcript with Amazon Transcribe"
datePublished: Sun Apr 07 2024 14:35:41 GMT+0000 (Coordinated Universal Time)
cuid: clupmluqn000108id68cdda2m
slug: create-an-audio-transcript-with-amazon-transcribe

---

**Amazon Transcribe** is an automatic speech recognition (ASR) service offered by AWS

It enables developers to add speech-to-text capability to their applications. It uses machine learning models to convert audio to text. Amazon Transcribe is a pay-as-you-go service; pricing is based on seconds of transcribed audio, billed on a monthly basis.

Step 1

* Launch the AWS Management console
    
* Launch S3 and create a bucket
    

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1667667980480/YdwcBFM3B.png align="left")

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1667667839227/n87IXJxnK.png align="left")

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1667667906365/8VuyAf0aN.png align="left")

**Step 2**

* Upload your audio file to the bucket
    

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1667668384922/jSccBp8yb.png align="left")

* Select the audio file and copy the S3 url link
    

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1667668485028/AnalEdHHT.png align="left")

**Step 3**

* Launch Amazon Transcribe
    
* Create a transcript
    

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1667668872943/o7JG0oAkV.png align="left")

**Step 4**

* Specify job name
    
* Leave language as default
    
* Leave model as default
    

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1667668989251/VJ1NhBnvt.png align="left")

**Step 5**

* Paste the S3 url in the input field
    
* Leave the default output location
    
* Leave the subtitle file format *(Optional)*
    
* click next
    

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1667669274015/dFYv2GkQu.png align="left")

* Leave everything as default and click create job
    

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1667669507741/VnedkxnsL.png align="left")

* Our transcription job is done
    
* Be sure the status reads *complete*
    

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1667669620627/AQb_CArZf.png align="left")

* Click on the complete job in the name column
    
* Scroll down to see the transcription preview
    

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1667669925033/nbX_8u-YG.png align="left")

Congratulation! We have successfully transcribed our audio to text

Click here to translate your result into a different language [How to translate into different language](airxcloud.com)