![exit](https://github.com/user-attachments/assets/bdf6eeb9-7d83-4d3f-8b1c-393d89cf5998)Download the image

We find that
We were given a red image.
It looked boring. Just red. Nothing special.

We try to use the tool called exiftool
exiftool is a command-line application for reading, writing, and editing metadata in files — especially image, audio, video, and document files.
We get this data for the downloaded image

`exiftool red.png`

![exit](https://github.com/user-attachments/assets/2ec5a221-edaa-46c7-9169-033a6c1e947c)

and we see the first letters of each line of the poem 
`C H E C K L S B`

So now we’re told: the hidden data is in the Least Significant Bits of the image.
We’ll need a tool like zsteg or similar to extract it.
zsteg is a command-line tool used to detect and extract hidden data embedded in PNG and BMP images using Least Significant Bit (LSB) steganography and similar techniques.

`zsteg red.png`
![zsteg](https://github.com/user-attachments/assets/cd3cc713-46dc-40de-ac65-63bdd88bd694)

We find a Hidden Base64 String which is repeated so we add it to a text file
└─$ echo cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ== > hash.txt 

and then we decode it and get the flag
└─$ base64 hash.txt -d
`picoCTF{r3d_1s_th3_ult1m4t3_cur3_f0r_54dn355_}`  

![flag](https://github.com/user-attachments/assets/c4a0c2d0-7640-44dd-97e6-9e9a2488dd41)
