------

crackme-py
 | 30 points

Tags: Reverse Engineering

Author: syreal

Description
crackme.py

------

First we use nano to look at this python file:

![image](https://user-images.githubusercontent.com/90400244/175939500-5539917c-fec5-41a8-9bc9-61033480baba.png)


We get served the formula right away! 

bezos_cc_secret is the actual flag but encoded and we see a few lines down that the encoding used is ROT47!

**pasting the bezos secret into an online ROT47 decoder will give you the flag but we will make a script to decode it for us**


----

If you look at the “ def decode_secret(secret): ” you see that it's not applied to the script, it just shows the code on how to do it. We can also remove the bottom half of the script because it has nothing to do with decoding the string. Now we add this code to the very end:

decode_secret(bezos_cc_secret)

-----

![image](https://user-images.githubusercontent.com/90400244/175939687-b6199aa5-ee74-440c-9d15-5e714ffc6632.png)


This is how the script looks like after cleaning it up and adding the code at the bottom. Now we run it, the result it:

                                                                                                                                                             
┌──(kali㉿kali)-[~/Desktop/picoCTF/Reverseengineering/crackme-py]

└─$ python crackme.py

picoCTF{1|\/|_4_p34|\|ut_f3bc410e}

-----

picoCTF{1|\/|_4_p34|\|ut_f3bc410e}

----

