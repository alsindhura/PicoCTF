We download the file given in the question

And now we try to find the file `uber-secret.txt`

I am going to use the find command to locate this file 

`find /home/dell/Documents/files -type f -name uber-secret.txt 2>/dev/null`

Note: /home/dell/Documents/files is the path where I have extracted the zip folder

<img width="1013" height="132" alt="image" src="https://github.com/user-attachments/assets/57a9975b-3feb-484d-978d-6a08a499bdc6" />

We got the path for this file `files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt`

We will now navigate to this path and get our flag

<img width="1023" height="145" alt="image" src="https://github.com/user-attachments/assets/a55cc4e0-4cc6-4716-9a2d-bc9adc3ad0c6" />

Flag: `picoCTF{f1nd_15_f457_ab443fd1}`

_____________________________________________________
