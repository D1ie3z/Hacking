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
