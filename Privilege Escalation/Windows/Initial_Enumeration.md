# Initial Enumeration

# Manual
## System Enumeration
* systeminfo
* systeminfo | findstr /B /C:"OS Name" /C:"OS Version" /C:"System Type"
* hostname
* wmic product get name, version, vendor
* wmic qfe
* wmic qfe get caption, description, HostFixID, InstalledOn
* wmic logicaldisk get caption,description,providename -> CHECK IF THERE ARE ANY OTHER DRIVES AND TEST!!

## User Enumeration
* whoami
* whoami /priv
* whoami /groups
* net user
* net user exampleUser -> give specific information of "exampleUser" (Obviusly you have to change for the name of the user that you want to know)
* net localgroup
* net localgroup administrators (The same you have to change for the group you want)

## Network Enumeration
* ipconfig
* arp -a
* route print
* netstat -ano

## Password hunting
* findstr /si password *.txt *.ini *.config (I recommend doing it on the system32 path)
* USE THE RESOURCES THAT I GAVE YOU

## AV and Firewall Enumeration
* sc query windefend
* sc queryex type= service
* netsh advfirewall firewall dump
* netsh firewall show state
* netsh firewall show configuration

## Processes
* tasklist /svc

## Readable/writable files and directories
* accesscheck.exe -uws "Everyone" "C:\Program Files"

# Automated

* winpeas: https://github.com/carlospolop/privilege-escalation-awesome-scripts-suite/tree/master/winPEAS

* Windows Priv Esc Checklist: https://book.hacktricks.xyz/windows/checklist-windows-privilege-escalation

* Sherlock: https://github.com/rasta-mouse/Sherlock

* Watson: https://github.com/rasta-mouse/Watson

* PowerUp: https://github.com/PowerShellMafia/PowerSploit/tree/master/Privesc

* JAWS: https://github.com/411Hall/JAWS

* Windows Exploit Suggester: https://github.com/AonCyberLabs/Windows-Exploit-Suggester

* Metasploit Local Exploit Suggester: https://blog.rapid7.com/2015/08/11/metasploit-local-exploit-suggester-do-less-get-more/

* Seatbelt: https://github.com/GhostPack/Seatbelt

* SharpUp: https://github.com/GhostPack/SharpUp


