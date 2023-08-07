# Managing Users

## Delegation
If an user has the privilege to change the password of other users you should try:
* Set-ADAccountPassword userToChange -Reset -NewPassword (Read-Host -AsSecureString -Prompt 'New Password') -Verbose
* Set-ADUser -ChangePasswordAtLogon $true -Identity userToChange -Verbose
* Then Login as the user that tou change the password
