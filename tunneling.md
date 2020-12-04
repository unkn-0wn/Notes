# Tunneling and Port forwarding
## SSH Tunneling

SSH local port forwarding

``
ssh -N -L <Our_Kali_ip:Our_Kali_port:Tunnled_host:Tunnled_hostport <ssh_username@ip>
``

SSH Remote port forwarding

``
ssh -N -R <Our_Kali_ip:Our_Kali_port:Tunnled_host:Tunnled_hostport <ssh_username@ip> 
``

SSH Dynamic Port forwarding

``
ssh -N -D <Our_kali_ip:kali_port> ssh_username@IP
``

## Plink.exe
windows_IP and Port =which to be forwarded

``
cmd.exe /c echo y | plink.exe -ssh -l user -pw passwd -R kali_ip:kali_port:windows_IP:windows_portkali_IP kali_IP
``

## Netsh

``
netsh interface portproxy add v4tov4 listenport=compromised_port listenaraddress=compromised_machine_ip connectport=forwarding_port connectedaddress=forwarding_ip
``

after this we need to set a firewall rule using netsh

``
netsh advfirewall firewall add rule name="rule_name" protocol=TCP dir=in localip=compromised_ip localport=compromised_port action=allow
``

