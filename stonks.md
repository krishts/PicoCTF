# Stonks
1) According to the level, there is a C source code named 'vulc.c' used to trade stonks. There is a netcat command to connect remotely to the program.
2) I then open the C source code analyse it. I find there is a variable 'user_buf' which contains a stack of the flag.
3) I then execute the program on picoCTF webshell and when it asks for an API token i enter something random and some random shares show up.
   
   ![image](https://github.com/Snapskillz123/picoCTF/assets/149099858/6be532a2-3580-4cdf-af0f-ef822ba8216a)

5) On further inspection of the code, i find that there is no format specifier for the print statement of 'user_buf', so next time when I execute the code, I enter many '%x' to convert the flag into hexadecimal. (stack is very big)

   ![image](https://github.com/Snapskillz123/picoCTF/assets/149099858/ea2866fb-b21d-4e5a-9075-fb5c321df232)

6) I then convert the given hexadecimal text into binary using a website: https://www.duplichecker.com/hex-to-text.php

![image](https://github.com/Snapskillz123/picoCTF/assets/149099858/8b6a4243-ebb7-4dc7-9dc2-b3403d83b5b9)

6) There is a little readable text in the string text which looks similar to the format of the flag.
7) After little inspection I find that every 4 characters of the string text have been reversed.
8) After using that decryption method i find the flag.

   # Flag

   picoCTF{I_l05t_4ll_my_m0n3y_6045d60d}

