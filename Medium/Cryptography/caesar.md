We are asked to download a file named `data.enc`

And when we view the contents of the file, we see a caesar ciphertext `picoCTF{hwtxxnslymjwzgnhtswlvhsgdv}`

<img width="432" height="105" alt="image" src="https://github.com/user-attachments/assets/ccea1f64-b5be-4f23-86b7-f74b85c03c0b" />

We only try to get decrypt the contents within {} because the word `picoCTF` before {} is correct part of the flag and doesn't require decrypting

We can try this [online tool](https://raw.org/tool/caesar-cipher/) for decrypting

<img width="637" height="678" alt="image" src="https://github.com/user-attachments/assets/f6a53375-66cd-43d6-b538-1fbe74551b3a" />

We keep changing the key until the decrypted text looks like plaintext

And at key `21` we finally be able to see the plaintext

<img width="598" height="698" alt="image" src="https://github.com/user-attachments/assets/c6d88af9-938b-4bf8-8190-ba5a5bf5c581" />

Note: We have only decrypted the contents inside {} and we need to add `picoCTF` before this decrypted plaintext

Flag: `picoCTF{crossingtherubiconrgqcnbyq}`

_______________________________________

