# Buffer Over Flow

## Fuzzing

!mona config -set workingfolder c:\mona\%p


## Spiking

``
/usr/share/metasploit-framework/tools/exploit/pattern_create.rb -l (Number_of_characters)
``

``
/usr/share/metasploit-framework/tools/exploit/pattern_offset.rb (Off-set)
``

> Using MONA

``
!mona findmsp -distance (Number_of_char)

``
## Finding Bad Characters

 FIrst crash the program using exploit.py
> folow in dump

``
Genrate the bytechar

!mona bytearray -b "BAD_CHAR"   
``

> compare bad char

``
!mona compare -f C:\path\to\the\bin -a ESP_address
``

## finding Jump Point

``
!mona jmp -r esp -cpb "bad_chars"

write it in reverse order as char \x00\x01 etc 
``
