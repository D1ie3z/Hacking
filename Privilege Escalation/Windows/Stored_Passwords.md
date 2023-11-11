# Escalation via stored passwords

## Search for password in registry
* reg query HKLM /f password /t REG_SZ /s
* reg query HKCU /f password /t REG_SZ /s
* Get-ChildItem -Path C:\ -Include *.kdbx -File -Recurse -ErrorAction SilentlyContinue
* Get-ChildItem -Path C:\xampp -Include *.txt,*.ini -File -Recurse -ErrorAction SilentlyContinue -> Find interesting files
* Get-ChildItem -Path C:\Users\johnDoe\ -Include *.txt,*.pdf,*.xls,*.xlsx,*.doc,*.docx -File -Recurse -ErrorAction SilentlyContinue -> FILES CHANGE THE USER

[+] Go to : https://sushant747.gitbooks.io/total-oscp-guide/content/privilege_escalation_windows.html

IF YOU FIND ANY CREDENTIAL TRY TO REUSE IT IN OTHER SERVICES OR LOGINS!!!
