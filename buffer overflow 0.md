# buffer overflow 0

1) I first opened the source code provided in the question and analysed it.
2) I saw there was a variable buf1 which is inputted by the user and is then sent to the 'vuln' function.

   ![image](https://github.com/Snapskillz123/picoCTF/assets/149099858/55dff448-0183-42e4-9493-224551dc84e3)

3) The maximum length of buf2 is 16 and the question is all about overflowing the stack.
4) So i then ran the program on the shell and when i entered a string more than 16 characters the stack overflowed and the flag came as the output.

   ![image](https://github.com/Snapskillz123/picoCTF/assets/149099858/66da5102-c1c3-49fc-ba71-52fb395ca5dc)

   # Flag

   picoCTF{ov3rfl0ws_ar3nt_that_bad_c5ca6248}
   

