# Super Safe RSA

**Points:** 350

**Description**
> Dr. Xernon made the mistake of rolling his own crypto.. Can you find the bug and decrypt the message? Connect with `nc 2018shell1.picoctf.com 1317`.

**Hints**
> Just try the first thing that comes to mind.

## Solution

Connecting to the shell outputs the following message:

```
c: 6174458954004155103273409312035455859655484552895151362802170114671335859548232                                         
n: 14290696247301666369138484476332938872986473844717355788126318979675968794821391                                        
e: 65537
```

The first thing that came to my mind was _"Huh... That is a small n value."_

Using an [online integer factorization calculator](https://www.alpertron.com.ar/ECM.HTM), we can get some very useful calculations. Normally, this wouldn't be possible with a large `n` value (it would take ages), but the one in this problem is small so it takes a few minutes.

This tool gives us `tot(n)`, which is `14290696247301666369138484476332938872884761206903858595975061985403322751547992`. 

We can use this to calculate `d` by plugging `tot(n)` and `e` into the formula `e^-1 mod totient(n)`. This gives us `14085070012332023703375669717323799587334151172600940570188033536554041683529777`.

Now, we can decrypt the message using the python `pow()` function with the parameters `c`, `d` and `n`. This gives us `14085070012332023703375669717323799587334151172600940570188033536554041683529777` as the message.

Finally, we decrypt this in the same fashion as the previous RSA problems. We convert this decimal number into hex, then convert that hex into ASCII. ([this website](https://www.rapidtables.com/convert/number/decimal-to-hex.html) to convert from decimal to hex, followed by [this website](https://www.rapidtables.com/convert/number/hex-to-ascii.html) to convert from hex to ASCII.) This gives us our flag. 

The flag is `picoCTF{us3_l@rg3r_pr1m3$_0622}`
