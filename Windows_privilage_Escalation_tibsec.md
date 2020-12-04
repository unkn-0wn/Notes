# Windows Privilage Escalation - Tibsec

## Privilage escalations tools

``
PowerUp
``

``
SharpUP
``

``
Seatbelt
``

``
winPEAS
``

``
 accesschk.exe
``

## Kernal Exploits
Tools

``
wesng - Windows exploit Suggester
``

``
secwiki - Windows kernel exploit
``

## Service Exploits

### Service Commands

Configuratio of a service
``
sc.ex qc <service_name>
``

Current status of a service
``
sc.exe query <Service_name>
``

Modify a configuration option of a service
``
sc.exe config <Service_Name> <Option>= <value>
``

Start/stop a service
``
net start/Stop <Service_name>
``

### Password

TO serch all possible passwords in files
``
reg query HKLM /f password /t REG_SZ /s
``
``
reg query HKCU /f password /t REG_SZ /s
``
 AutoLogin

``
reg query "HKLM\Software\Microsoft\Windows NT\CurrentVersion\winlogon"
``

Putty sessions

``
reg query "HKCU\Software\SiminTatham\Putty\Sessions*" /s
``

#### saved creds

run savecreds.bat
``
cmdkey /list
``

exploit
``
runas /savecred /user:admin path\to\file
``

Serch Password in .config file recu

``
dir /s *pass* == ".config
``

``
findstr /si password *.xml *.ini *.txt
``
