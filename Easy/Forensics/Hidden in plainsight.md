Link: https://play.picoctf.org/practice/challenge/524

We will have to download the image provided and when we open the image, it looks like this

![img](https://github.com/user-attachments/assets/6eec57bc-2f43-467c-8700-ded87c6890d7)

We use the following command `file img.jpg` and see an encoded comment

<img width="1914" height="122" alt="image" src="https://github.com/user-attachments/assets/de39e0eb-57a0-4967-a9d4-604888f6c15b" />

Now we open Cyberchef and we find out that this comment is base64

<img width="1532" height="632" alt="image" src="https://github.com/user-attachments/assets/e7be7ff4-f804-4e63-a9de-a5bd012943f6" />

Now we decode using Base64 to find the decoded messages as `steghide:cEF6endvcmQ=`

<img width="836" height="224" alt="image" src="https://github.com/user-attachments/assets/0b96c5e1-f247-49b1-94e2-30d97338156e" />

From the above decoded message, we got the following information

1. Steghide (a program used to hide data in various kinds of image and audio files) is being used and to recover this hidden data a password should be provided

2. The password looks encoded

 We see that the password is also encoded in base64

<img width="1533" height="253" alt="image" src="https://github.com/user-attachments/assets/37459849-8550-460b-949a-2668f8943a0b" />

We got the password for recovering the data which was hidden using steghide

<img width="715" height="222" alt="image" src="https://github.com/user-attachments/assets/9aca6955-29a9-440f-8b9d-aab30c36860e" />

To recover data, we use the following command `steghide extract -sf img.jpg`

After using the above command, we have to provided the password which we recovered from the encoded comment and  the flag will be saved to flag.txt upon success

<img width="435" height="125" alt="image" src="https://github.com/user-attachments/assets/02bebdba-6301-4c76-ae2d-ff36c9befd56" />

Let's read flag.txt to get out flag `picoCTF{h1dd3n_1n_1m4g3_5d4cba73}`

<img width="433" height="103" alt="image" src="https://github.com/user-attachments/assets/1c916b21-7770-4213-8165-4e13145efeab" />

___________________________________________________________________________
