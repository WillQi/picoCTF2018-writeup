# caesar cipher 1

**Points:** 250

**Description**
> Can you help us decrypt this message? We believe it is a form of a caesar cipher. You can find the ciphertext in /problems/caesar-cipher-2_4_23c82ed24f4436e96acc1f9f22dc8799 on the shell server.

**Hints**
> You'll have figure out the correct alphabet that was used to encrypt the ciphertext from the ascii character set

> [ASCII Table](https://www.asciitable.com/)


## Solution

When we open the ciphertext file, we see that the ciphertext reads `d]Wc7H:oW5YgUFS7]D\9fGS^iGHSUF9bHSg9WIf9q`. We also know that we're going to be using a version of the caesar cipher with ASCII rather than just the alphabet. We can assume that the first eight characters must be `picoCTF{` and that the last one must be `}` since the question doesn't mention an irregular flag format. Therefore, the shift must be 12 (`d`'s decimal code is `100`, `p`'s is `112`). 

By writing a quick Python script, we can decipher our flag.

```python
inputString = "d]Wc7H:oW5YgUFS7]D\9fGS^iGHSUF9bHSg9WIf9q"
decrypted = ""
for i in range(len(inputString)):
    decrypted = decrypted + chr(ord(inputString[i]) + 12)
print("Decrypted String: " + decrypted)
```

The flag is `picoCTF{cAesaR_CiPhErS_juST_aREnT_sEcUrE}`
