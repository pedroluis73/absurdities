---
title: "To be Pointer or not to be, that is the question *"
date: 2020-03-03
---

Well, well, well... What am I going to do with you (me)? Tell me please!!! 

At this point(er) I do not know anymore...

This one is a particular stupid mistake (yes, even in my standards). 

So I was trying to create two char arrays. And I wrote the following:

    char * arr1, arr2;
    
And went on and on and on trying to understand why I was getting the usual error for badly allocating memory: Segmentation Fault.

10 minutes went by: nothing... 20 minutes went by: nothing... 30 minutes went by: "What the fuck is my dumbass brain not thinking about? This is not that fucking difficult!!" and suddently:

    char * arr1, * arr2;
    
Solved.

Ways to declare a pointer in C include:

    char* arr1, *arr2, * arr3; 

Please do not let me forget this! I do not want to go through this traumatic experience again!!!

#Absurdities #IamtheAbsurd
