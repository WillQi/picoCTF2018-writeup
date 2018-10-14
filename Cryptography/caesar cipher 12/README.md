# caesar cipher 1

**Points:** 150

**Description**
> This is one of the older ciphers in the books, can you decrypt the [message](ciphertext)? You can find the ciphertext in `/problems/caesar-cipher-1_1_6fbf7a9ce0aac23bab1c37836cc20c3b` on the shell server.


**Hints**
> caesar cipher [tutorial](https://learncryptography.com/classical-encryption/caesar-cipher)


## Solution

When we open the ciphertext.txt file, we see the encrypted flag `picoCTF{vgefmsaapaxpomqemdoubtqdxoaxypeo}`. We don't know the shift, so we can either try each caesar cipher or program something that does it for us.

Since we had enough time, we just did it manually using [this website](https://cryptii.com/pipes/caesar-cipher) by testing each shift. Eventually, we go to a shift of 14 and our decoded flag.

(Although, we plan on creating some programs for cryptography for our next CTF!)

The flag is `picoCTF{justagoodoldcaesarcipherlcolmdsc}`
