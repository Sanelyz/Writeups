
Magikarp Ground Mission
 | 30 points

Tags: General Skills

Author: syreal

Description
Do  you know how to move between directories and read files in the shell?  Start the container, `ssh` to it, and then `ls` once connected to begin.  Login via `ssh` as `ctf-player` with the password, `a13b7f9d`


----------------------------------------------------------------------------------------------------------------------------------------

After logging in we will just scout the directiories with basic commands like “   cd ..   |    ls    |    cd /    |   cd ~   |    cd root    |    pwd    ”

![image](https://user-images.githubusercontent.com/90400244/175908251-fb19c9b3-d29d-4584-a640-d4964d77d919.png)



----------------------------------------------------------------------------------------------------------------------------------------

![image](https://user-images.githubusercontent.com/90400244/175908862-befe7844-71f0-4e2f-95ab-09e96f71a8e1.png)


We already got the first part of the flag by using “ ls ” and “ cat 1of3.flag.txt ”    Lets find the remaining parts!


----------------------------------------------------------------------------------------------------------------------------------------

![image](https://user-images.githubusercontent.com/90400244/175908918-f29ac5c4-1bc2-4648-ab48-242c4296e542.png)



We use pwd to see what directory we are in. With cd ..  we go up one directory then do ls again to list all files in that directory and we got part 3 of our flag! 1 to go.


----------------------------------------------------------------------------------------------------------------------------------------

![image](https://user-images.githubusercontent.com/90400244/175909015-a8c6b2a6-9d23-4331-b527-013a4defd3fe.png)



With cd / we go all the way up to root directory and then using ls we got the 2'nd part of our flag! now we got all the parts and we can combine it to get the flag!


----------------------------------------------------------------------------------------------------------------------------------------

picoCTF{xxsh_0ut_0f_\/\/4t3r_71be5264}

----------------------------------------------------------------------------------------------------------------------------------------

