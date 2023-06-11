# Port Forwarding

* Download plink.exe -> https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html
* Transfer plink to the machine
* apt install ssh -> On linuc
* Edit /etc/ssh/sshd_config, change #PermiRootLogin prohibit-password to PermiRootLogin yes
* ssh service restart
* ssh service start
