# Lying Out

**Points:** 250

**Description**
> Some odd [traffic](traffic.png) has been detected on the network, can you identify it? More [info](info.txt) here. Connect with `nc 2018shell1.picoctf.com 39410` to help us answer some questions.

**Hints**
> (No hints were provided)

## Solution

Connecting to the shell will prompt you with a list of traffic logs. The [picture](traffic.png) provided is an example of the usual traffic. We simply compared if the IP at the specified time was abnormally high. It didn't matter if it was abnormally lower since that wasn't an attack.

To make this process easier due to the connection expiring after a period of time and the data we had to check changing every connection, we printed out a physical copy of the graph. Since the graph's x-axis was divided by two hours, to make our lives easier, we put in lines per hour.
 
Answering the question correctly gives us the flag, `picoCTF{w4y_0ut_940df760}`
