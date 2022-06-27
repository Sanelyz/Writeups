---------------------------------------------------------------------------------------------------

Transformation
 | 20 points

Tags: Reverse Engineering

Author: madStacks

Description
I wonder what this really is... enc ''.join([chr((ord(flag[i]) << 8) + ord(flag[i + 1])) for i in range(0, len(flag), 2)])

---------------------------------------------------------------------------------------------------

                                                                                                                                                             
┌──(kali㉿kali)-[~/Desktop/picoCTF/Reverseengineering/Transformation]
└─$ ls
enc
                                                                                                                                                             
┌──(kali㉿kali)-[~/Desktop/picoCTF/Reverseengineering/Transformation]
└─$ cat enc
灩捯䍔䙻ㄶ形楴獟楮獴㌴摟潦弸彤㔲挶戹㍽                                                                                                                                                             


okay, so we got some scetchy unicode characters going on here. Instead of going all the way and make a python script
that decodes this, lets rather find out what its encoded into and then reversing it!.

---------------------------------------------------------------------------------------------------

After a few seconds i found out that it`s UTF-16 (Hex) encoded, examples below!

![image](https://user-images.githubusercontent.com/90400244/175912030-03649ac8-a543-4305-8208-0c489715eec4.png)


![image](https://user-images.githubusercontent.com/90400244/175912160-cba98e37-57d8-4e9b-bcde-ec4758de71ba.png)



---------------------------------------------------------------------------------------------------

Knowing that it`s HEX, all i did was to remove “ \u “ since it represents ” 0x ”, that leaves us with plain HEX which i decoded into Ascii.

![image](https://user-images.githubusercontent.com/90400244/175911901-3c748c25-2652-4131-a1c9-a27e4dd3c246.png)


---------------------------------------------------------------------------------------------------

picoCTF{16_bits_inst34d_of_8_d52c6b93}

---------------------------------------------------------------------------------------------------
