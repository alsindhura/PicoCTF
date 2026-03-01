We download the file provided in the challenge and extract it

And we see multiple files inside this folder 

<img width="1340" height="987" alt="image" src="https://github.com/user-attachments/assets/1bd5a2e5-1b46-46a5-a5bd-a6b8debb9e61" />

We cannot manually go and search each and every file so we use `grep`

We can use the following command to get us the flag using the picoCTF pattern

`grep -r "picoCTF"`

or 

`grep -r "picoCTF" big-zip-files/` (if we are not in the folder)

And we can see the flag which is buried inside `big-zip-files/folder_pmbymkjcya/folder_cawigcwvgv/folder_ltdayfmktr/folder_fnpfclfyee/whzxrpivpqld.txt`

<img width="1332" height="125" alt="image" src="https://github.com/user-attachments/assets/dad0b1ae-f73a-42ad-af95-55e444a8e27f" />

Flag: `picoCTF{gr3p_15_m4g1c_ef8790dc}`
