We open the link provided and see something like this

<img width="955" height="361" alt="image" src="https://github.com/user-attachments/assets/72b9d000-5f28-415a-922b-b1e69b298067" />

We are given the credentials and we sign in with the same

<img width="1175" height="131" alt="image" src="https://github.com/user-attachments/assets/94233a54-8a05-4a9b-80ff-b67797d74ab4" />

Now we open Dev tools and go to Storage

<img width="1913" height="441" alt="image" src="https://github.com/user-attachments/assets/02fbba17-bd8b-4315-b04c-6da99ae50f6a" />

Here, we can see a token 

```
eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.
eyJhdXRoIjoxNzcyMTAzNjYzNjAyLCJhZ2VudCI6Ik1vemlsbGEvNS4wIChYMTE7IExpbnV4IHg4Nl82NDsgcnY6MTQwLjApIEdlY2tvLzIwMTAwMTAxIEZpcmVmb3gvMTQwLjAiLCJyb2xlIjoidXNlciIsImlhdCI6MTc3MjEwMzY2NH0.
imVXWUSgRqQzMLl4Qgz2OkUm3lb24I6cP2lN_Ow0kgo
```

We go to [cyberchef](url) and choose `JWT decode`

<img width="1528" height="274" alt="image" src="https://github.com/user-attachments/assets/d0ef9ae4-b820-4509-a746-c32f25f3190a" />

We can see from the above picture that currently the role is `user` and we can try changing this to `admin`

Before changing the role, we choose `JWT Sign` and choose the algo from `HS256` to `None` and then change the role

<img width="1534" height="363" alt="image" src="https://github.com/user-attachments/assets/0d5f14c9-de69-4ce1-b2a1-866d924ee7f9" />

```
eyJhbGciOiJub25lIiwidHlwIjoiSldUIn0.
eyJhdXRoIjoxNzcyMTAzNjYzNjAyLCJhZ2VudCI6Ik1vemlsbGEvNS4wIChYMTE7IExpbnV4IHg4Nl82NDsgcnY6MTQwL
jApIEdlY2tvLzIwMTAwMTAxIEZpcmVmb3gvMTQwLjAiLCJyb2xlIjoiYWRtaW4iLCJpYXQiOjE3NzIxMDM2NjR9.
```

And we paste this new token in the Storage -> Token area

<img width="1132" height="443" alt="image" src="https://github.com/user-attachments/assets/24540d64-92a0-4297-b3a4-5a02703fb6c1" />

Lastly, we refresh the page and see the flag now

<img width="733" height="161" alt="image" src="https://github.com/user-attachments/assets/4f5bb56a-a29f-46d4-812c-a3ced76a3757" />


Flag: `picoCTF{succ3ss_@u7h3nt1c@710n_72bf8bd5}`


