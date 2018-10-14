# hertz 2

**Points:** 200

**Description**
> This flag has been encrypted with some kind of cipher, can you decrypt it? Connect with `nc 2018shell1.picoctf.com 23479`.

**Hints**
> These kinds of problems are solved with a frequency that merits some analysis.

## Solution

Just like [hertz](../hertz%202), after connecting using netcat, we are given the ciphertext.

`Wro vsknj hpqcb gqi lstyu qmop wro efzx aqd. K nfb'w hoekomo wrku ku usnr fb ofux ypqheot kb Yknq. Kw'u fetquw fu kg K uqem
oa f ypqheot fepofax! Qjfx, gkbo. Ropo'u wro gefd: yknqNWG{ushuwkwswkqb_nkyropu_fpo_wqq_ofux_mxahqyxhmb}`

We decided to use the same method to solving it as the first one, which was by using [this tool](http://scottbryce.com/cryptograms/) to help us solve it. (Note: This tool uses capital letters by default, remember that your inputted test was lowercase.)

By looking at the format of the text, we know that `yknqNWG` must be `picoCTF`, because `picoCTF{}` is the format of the flag. After substituting in these letters, we can identify the rest of the cryptogram based on common words. The first sentence also clearly becomes `The quick brown fox jumps over the lazy dog.` which gives us all the letters in the alphabet.

The flag is `picoCTF{substitution_ciphers_are_too_easy_vydbopybvn}`
