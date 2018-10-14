# Radix's Terminal

**Points:** 400

**Description**
> Can you find the password to [Radix's login](radix)? You can also find the executable in /problems/radix-s-terminal_0_b6b476e9952f39511155a2e64fb75248?

**Hints**
> https://en.wikipedia.org/wiki/Base64

## Solution

We know that we're going to be working with Base64 because of the hint. If we open the file in a text editor, we are greeted with a bunch of gibberish (that usually happens when you open these types of files). However, looking through the text we find this:

`cGljb0NURntiQXNFXzY0X2VOQ29EaU5nX2lTX0VBc1lfNDE3OTk0NTF9`

Decoding this using a [Base64 Decoder](https://www.base64decode.org/), we get our flag.

The flag is `picoCTF{bAsE_64_eNCoDiNg_iS_EAsY_41799451}`
