# hertz

**Points:** 150

**Description**
> Here's another simple cipher for you where we made a bunch of substitutions. Can you decrypt it? Connect with `nc 2018shell1.picoctf.com 14928`.

**Hints**
> NOTE: Flag is not in the usual flag format

## Solution

After connecting using netcat, we are given the following text.

```-------------------------------------------------------------------------------                                            
goqhupmx abub jx koiu fsph - xiwxmjmimjoq_gjdabux_pub_xoscpwsb_fhqcchqlyx                                                  
-------------------------------------------------------------------------------                                            
"zbss, dujqgb, xo hbqop pql siggp pub qoz eixm fpyjsk bxmpmbx of mab                                                       
wioqpdpumbx. wim j zpuq koi, jf koi loqm mbss yb mapm majx ybpqx zpu,                                                      
jf koi xmjss muk mo lbfbql mab jqfpyjbx pql aouuoux dbudbmupmbl wk mapm                                                    
pqmjgaujxm-j ubpssk wbsjbcb ab jx pqmjgaujxm-j zjss apcb qomajqh                                                           
youb mo lo zjma koi pql koi pub qo soqhbu yk fujbql, qo soqhbu yk                                                          
'fpjmafis xspcb,' px koi gpss koiuxbsf! wim aoz lo koi lo? j xbb j                                                         
apcb fujhambqbl koi-xjm lozq pql mbss yb pss mab qbzx."                                                                    

jm zpx jq eisk, 1805, pql mab xdbpvbu zpx mab zbss-vqozq pqqp dpcsocqp                                                     
xgabubu, ypjl of aoqou pql fpcoujmb of mab bydubxx ypukp fblouocqp.                                                        
zjma mabxb zoulx xab hubbmbl dujqgb cpxjsj viuphjq, p ypq of ajha                                                          
upqv pql jydoumpqgb, zao zpx mab fjuxm mo puujcb pm abu ubgbdmjoq. pqqp                                                    
dcsocqp apl apl p goiha fou xoyb lpkx. xab zpx, px xab xpjl, xiffbujqh                                                     
fuoy sp hujddb; hujddb wbjqh mabq p qbz zoul jq xm. dbmbuxwiuh, ixbl                                                       
oqsk wk mab bsjmb.                                                                                                         

pss abu jqcjmpmjoqx zjmaoim btgbdmjoq, zujmmbq jq fubqga, pql lbsjcbubl                                                    
wk p xgpusbm-sjcbujbl foomypq mapm youqjqh, upq px fossozx:                                                                

"jf koi apcb qomajqh wbmmbu mo lo, goiqm (ou dujqgb), pql jf mab                                                           
duoxdbgm of xdbqljqh pq bcbqjqh zjma p doou jqcpsjl jx qom moo mbuujwsb,                                                   
j xapss wb cbuk gapuybl mo xbb koi moqjham wbmzbbq 7 pql 10 pqqbmmb                                                        
xgabubu."                                                                                                                  

"abpcbqx! zapm p cjuisbqm pmmpgv!" ubdsjbl mab dujqgb, qom jq mab                                                          
sbpxm ljxgoqgbumbl wk majx ubgbdmjoq. ab apl eixm bqmbubl, zbpujqh pq                                                      
bywuojlbubl goium iqjfouy, vqbb wubbgabx, pql xaobx, pql apl xmpux oq                                                      
ajx wubpxm pql p xbubqb btdubxxjoq oq ajx fspm fpgb. ab xdovb jq mapm                                                      
ubfjqbl fubqga jq zajga oiu hupqlfpmabux qom oqsk xdovb wim maoiham, pql                                                   
zjma mab hbqmsb, dpmuoqjnjqh jqmoqpmjoq qpmiups mo p ypq of jydoumpqgb                                                     
zao apl huozq osl jq xogjbmk pql pm goium. ab zbqm id mo pqqp dcsocqp,                                                     
vjxxbl abu apql, dubxbqmjqh mo abu ajx wpsl, xgbqmbl, pql xajqjqh abpl,                                                    
pql goydspgbqmsk xbpmbl ajyxbsf oq mab xofp.                                                                               

"fjuxm of pss, lbpu fujbql, mbss yb aoz koi pub. xbm koiu fujbql'x                                                         
yjql pm ubxm," xpjl ab zjmaoim psmbujqh ajx moqb, wbqbpma mab                                                              
dosjmbqbxx pql pffbgmbl xkydpmak of zajga jqljffbubqgb pql bcbq juoqk                                                      
goisl wb ljxgbuqbl.```

We decided to solve this as if it were a cryptogram. We had experience doing cryptograms before, and looked for common words (such as `the` and `and`) and frequent letters. We used [this tool](http://scottbryce.com/cryptograms/) to help us solve it. (Note: This tool uses capital letters by default, remember that your inputted test was lowercase.)

After a while, we realized that the text below the lines were from [War and Peace](http://pythonscraping.com/pages/warandpeace/chapter1.pdf) and were quickly able to finish the cryptogram.

The flag isn't in the default format as the hint says, so we don't need to change anything.

The flag is `substitution_ciphers_are_solvable_fgnvvgndms`
