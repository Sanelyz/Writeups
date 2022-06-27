---------------------------------------------------------------------------------------------------------------


keygenme-py
 | 30 points

Tags: Reverse Engineering

Author: syreal

Description
keygenme-trial.py

---------------------------------------------------------------------------------------------------------------



We start of by using the cat command on the keygenme.py file
First thing we see is this:

![image](https://user-images.githubusercontent.com/90400244/175937549-09b86b6c-1fb6-44c7-83e0-80428fe303bf.png)


Notice that we already get most of the flag but there is one particular bit of the flag that is encoded/hidden and it's in the “DYNAMIC” part which means it changes.
Notice that it's 8 digits long.

---------------------------------------------------------------------------------------------------------------


If we scroll further down in the script we see this:

![image](https://user-images.githubusercontent.com/90400244/175937094-7ede4bae-00bf-4cc2-a450-e5e015d1b63f.png)


These strings are the 8 digits we need to get, this should be very easy and i will show an easy way to decrypt this.
Also note the order it's in! ( 4 5 3 6 2 7 1 8 ) we need it for later!

---------------------------------------------------------------------------------------------------------------


Now we are going to decode the first sentence: “ hashlib.sha256(username_trial.encode()).hexdigest()[4] ” with a simple script.

![image](https://user-images.githubusercontent.com/90400244/175937050-fbaa1c31-3fe6-4e78-8b23-c47f7b93ae00.png)


This is the result:

                                                                                                                                                             
┌──(kali㉿kali)-[~/Desktop/picoCTF/Reverseengineering/keygenme-py]
└─$ python tryout.py 
a
      
---------------------------------------------------------------------------------------------------------------

      
Now that we know how to decode it lets add the 7 other sentences after it so we get the whole last part of the flag:

![image](https://user-images.githubusercontent.com/90400244/175936996-a9662c32-df68-47f3-b5dc-733968c4cc73.png)


our result is:

                                                                                                                                                             
┌──(kali㉿kali)-[~/Desktop/picoCTF/Reverseengineering/keygenme-py]
└─$ python tryout.py
ac73dc29
         
---------------------------------------------------------------------------------------------------------------


Okay, so that is actually the “xxxxxxxx” that we started with, aka the last part of our flag!

We are gonna add the first part of the flag that was given to us and the last bracket that was missing so when we run the script we get the whole flag as output!         

---------------------------------------------------------------------------------------------------------------


We only have to specify the start and ending of our script:

![image](https://user-images.githubusercontent.com/90400244/175936943-07ad0281-dcc8-4993-87b1-46576fe23e34.png)


Our result is:

                                                                                                                                                             
┌──(kali㉿kali)-[~/Desktop/picoCTF/Reverseengineering/keygenme-py]
└─$ python tryout.py
picoCTF{1n_7h3_|<3y_of_ac73dc29}

---------------------------------------------------------------------------------------------------------------


picoCTF{1n_7h3_|<3y_of_ac73dc29}

---------------------------------------------------------------------------------------------------------------


