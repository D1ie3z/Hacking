# SSH Private Key Passphrase
In this section we will focus on cracking SSH private key passphrases.

* chmod 600 id_rsa
* ssh -i id_rsa -p PORT USER@IP
* Try to use some possible passwords or generic information from the user
* If that doesn't work do the next steps
* ssh2john id_rsa > ssh.hash
* hashcat -h | grep -i "ssh"
  
![imagen](https://github.com/D1ie3z/Hacking/assets/88562299/9e3ec833-0d20-4473-b68d-3ee5b876b170)

* hashcat -m SOFWARE ssh.hash ssh.passwords -r ssh.rule --force -> SOFTWARE: ID from hashcat, Also the ssh.rule is optional
* 
