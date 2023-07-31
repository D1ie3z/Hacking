# SMB ENUMERATION
Bla bla bla smb tips

## Change the IP if you need
* nmap -v -p 139,445 -oG smb.txt 192.168.50.1-254
* sudo nbtscan -r 192.168.50.0/24
* nmap -v -p 139,445 --script smb-os-discovery IP
* net view \\dc01 /all
* Here are more: https://book.hacktricks.xyz/network-services-pentesting/pentesting-smb
