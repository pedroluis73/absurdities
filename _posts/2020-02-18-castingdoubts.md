---
title: "Absurtidy 03 - Casting doubts or How I will never grow out of my beginner mistakes"
date: 2020-02-18
---

From time to time, in my short, full of regrets, life the basic error involving casting appears.

But please do not be tempted to think this is a thorough, obscure error that only the most proeficent programmers can detect.
Au contraire mon ami! My error with casting begins with the simple forgetfullness that when chars are converted to ints the live in
the realm of the ASCII table. And if I want to sum two char variables which value is represented by 'digits' I must not forget they
are not what they appear.

So without further ado and to have on record that one time I knew how to do this, let us consider:

    char a = '4', b = '5';      
    int c;
    
And let us say I want to sum the two char contents (4 + 5 = 9).

If I do:

    c = a + b;
    
What I get is 52 (ASCII for char '4') plus 53 (ASCII for char '5'). And c is now 105, or the char 'i'. Congratulations stupid!

C automatically convert the char to its int value according to the ASCII table (oh beautiful table whose father was Bob Bemer,
according to a fast, possible imprecise, google search). So the above is the same as having:

    c = (int) a + (int) b;
    
To obtain the number I wished (number 9 - https://www.youtube.com/watch?v=SNdcFPjGsm8) what I should have done from the beginning
if I was a sane person who could learn from my mistake was:

    c = a - 48 + b - 48;
    
With the same logic if I wanted the char '9' I would do:

    char d = a + b - 48;
    
I really hope that from now on I may interiorize this concept and be a little faster understanding what is wrong with my 
arithmetic operations when doing any kind cast (this time took me about 15 minutes to realize the mistake).



#Absurdities #IamtheAbsurd
  
  
