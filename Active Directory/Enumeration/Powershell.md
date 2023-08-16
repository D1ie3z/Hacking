# Powershell Enumeration

## Users
* Get-ADUser -Identity username.username -Server domain.some.com -Properties *
    * Identity - The account name that we are enumerating
    * Properties - Which properties associated with the account will be shown, * will show all properties
    * Server - Since we are not domain-joined, we have to use this parameter to point it to our domain controller
#### For most of these cmdlets, we can also use the -Filter parameter that allows more control over enumeration and use the Format-Table cmdlet to display the results such as the following neatly:
* Get-ADUser -Filter 'Name -like "*surname"' -Server domain.some.com | Format-Table Name,SamAccountName -A

## Groups
* Get-ADGroup -Identity Administrators -Server domain.some.com
* Get-ADGroupMember -Identity Administrators -Server domain.some.com

## AD Objects
* $ChangeDate = New-Object DateTime(2022, 02, 28, 12, 00, 00)
* Get-ADObject -Filter 'whenChanged -gt $ChangeDate' -includeDeletedObjects -Server domain.some.com
* Get-ADObject -Filter 'badPwdCount -gt 0' -Server domain.some.com -> we can use this to enumerate accounts that have a badPwdCount that is greater than 0, to avoid these accounts in our attack

## Domains
* Get-ADDomain -Server za.tryhackme.com

## Altering AD Objects
* Set-ADAccountPassword -Identity username.username -Server domain.some.com -OldPassword (ConvertTo-SecureString -AsPlaintext "old" -force) -NewPassword (ConvertTo-SecureString -AsPlainText "new" -Force)
