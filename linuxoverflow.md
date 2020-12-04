lINUX buffer overflow using gdb

First run gdb ./program

#dissamble main function

``disas main``

add breakpoint below strcpy

using ``break *byte``

now run the program in gdb with python string gen

``run $(python -c "print('A'*number)")``

this will run the program with n number of A

now examin using
``x/200xb $esp
``
x- examin
b- bytes

NOte the staring point of buffer



use patern_crete to find the eip point 

USe patern_offset to fing the number


