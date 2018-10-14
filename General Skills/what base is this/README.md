# what base is this?

**Points:** 200

**Description**
> To be successful on your mission, you must be able read data represented in different ways, such as hexadecimal or binary. Can you get the flag from this program to prove you are ready? Connect with `nc 2018shell1.picoctf.com 15853`

**Hints**
> I hear python is a good means (among many) to convert things.

> It might help to have multiple windows open

## Solution

When we connect to the shell, we are greeted with easily recognizable binary code. There is a time limit of 30 seconds, so we need to decode quickly. The coded word also changes every time. We used [this decoder](https://cryptii.com/pipes/binary-decoder) to decode the binary code.

Next, we are given a hex code. We used [this decoder](http://www.convertstring.com/EncodeDecode/HexDecode) to decode it.

Finally, we are given octal code. We used [this decoder](http://www.unit-conversion.info/texttools/octal/) to decode it.  

Binary code is base 2, hexadecimal is base 16 and octal is base 8. After entering in the octal code, we are given our flag.

The flag is `picoCTF{delusions_about_finding_values_3cc386de}`
