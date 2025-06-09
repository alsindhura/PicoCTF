CTF Challenge Link: https://play.picoctf.org/practice/challenge/460?difficulty=1&page=2 

We find that we were given a red image and we download it.
It looked boring. Just red. Nothing special.

![red](https://github.com/user-attachments/assets/5b1065ff-2ecb-4e19-a917-9583e949a2f5)


We can use the tool called exiftool. 
Exiftool is a command-line application for reading, writing, and editing metadata in files — especially image, audio, video, and document files.
We get this data from the downloaded image after running: 

`exiftool red.png`

![exit](https://github.com/user-attachments/assets/2ec5a221-edaa-46c7-9169-033a6c1e947c)

The metadata showed a poem:
```
Crimson heart, vibrant and bold,
Hearts flutter at your sight.
Evenings glow softly red,
Cherries burst with sweet life.
Kisses linger with your warmth.
Love deep as merlot.
Scarlet leaves falling softly,
Bold in every stroke.
```

the first letters of each line spelled: `C H E C K L S B` and it looks like a clue

Since the hint mentioned “Least Significant Bits,” We have decided to use `zsteg`, a tool that can find hidden data stored in the least important bits of image pixels.

`zsteg red.png`
![zsteg](https://github.com/user-attachments/assets/cd3cc713-46dc-40de-ac65-63bdd88bd694)

We find a Hidden Base64 String which is repeated several time and we add only single instance of this string to a text file called hash.txt
└─$ echo cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ== > hash.txt 

and then we decode it and get the flag
└─$ base64 hash.txt -d
`picoCTF{r3d_1s_th3_ult1m4t3_cur3_f0r_54dn355_}`  

![flag](https://github.com/user-attachments/assets/c4a0c2d0-7640-44dd-97e6-9e9a2488dd41)
