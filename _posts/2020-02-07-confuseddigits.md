---
title: "Absurtidy 01 - Confusing a number size (number of digits) with its value"
date: 2020-02-07
---

The day before yesterday, I was trying to solve an "easy" problem (at least in classification for Hackerearth, for me nothing is 
ever easy) in C and for half an hour I was confused on why I was getting SIGFPE (fatal arithmetic error). 

So, I searched for divisions by zero since I had some divisions on my code. All seemed safe (because the input values for the test
cases helped and not because I had done a good job preventing these kind of errors).

Next, I thought about the possiblity of overflow. And this is the real shameful part. The problem stated that we would be given an 
input with at most 10⁵ digits. And I was like: "10⁵ is not that big, it is 1000000. It fits an integer, right? An integer is 
2,147,483,647 (10 digits). But maybe I am counting this in a wrong way. Let me use a long int for safety. Long int is 
9223372036854775807 (19 digits). How come this is not working??".
It was after a long period of time that I realized that a number with 1000 digits is way bigger that a number with 10 or 20 
digits (Like two orders of magnitude bigger). And the fucking hell moment came: I was not comparing the number sizes - I was
comparing the size of a number (number of digits the number can have) with its actual potential value!

And this is how I was being ABSURD comparing number of digits with number values.

Actually the SIGFPE error to my problem was also coming from a division by zero (but that is another story). Nonetheless this made thing about the enormity of the numbers I was dealing with.

And from what I understood from https://www.gnu.org/software/libc/manual/html_node/Program-Error-Signals.html I could not get this error from my beginner program and I quote:

"...

 Macro: int SIGFPE

    The SIGFPE signal reports a fatal arithmetic error.
...

FPE_INTOVF_TRAP

    Integer overflow (impossible in a C program unless you enable overflow trapping in a hardware-specific fashion). 

..."

#Absurdities #IamtheAbsurd
