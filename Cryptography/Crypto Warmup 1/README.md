# Crypto Warmup 1

**Points:** 75

**Description**
> Crpyto can often be done by hand, here's a message you got from a friend, `llkjmlmpadkkc` with the key of `thisisalilkey`. Can you use this [table](../Crypto%20Warmup%201/table.txt) to solve it?.


**Hints**
> Submit your answer in our competition's flag format. For example, if you answer was 'hello', you would submit 'picoCTF{HELLO}' as the flag.


> Please use all caps for the message.

## Solution

We are given a file called `table.txt`, so let's open that. We opened files using Visual Studio Code because it had better formatting compared to something like Notepad.

Here is our table:  

![VS Table](../Crypto%20Warmup%201/tablevs.PNG)

We recognized this as Vigenère Cipher. Rather than decode it by hand like the problem suggests, we can use an online decoder. This is easy to decode because we are also given the key, `thisisalilkey`.

Using [this website, Dcode](https://www.dcode.fr/vigenere-cipher), we can enter in our key and our ciphertext. Then, we are given the text `secretmessage`.

Now, all we need to do is format it for the flag.

The flag is `picoCTF{SECRETMESSAGE}`
