# Enumeration
A lot of ways to enumerate, do the manual way first and then use a tool. 
## Sudoers
* Sudo -l
## Kernel
* uname -a
## Groups 
* find / -group developer 2>/dev/null
## Hostname
* hostname
## VERSION
* cat /proc/version
## ISSUES
* cat /etc/issues
## PROCESSES
* ps
* ps -A
* ps -axjf
* ps aux
## ENVIRONMENT
* env
## ENLISTAR 
* ls -la
## ID
* id
## PASSWD
* cat /etc/passwd
## HISTORY
* history
## REDES
* Ifconfig
* iproute
* ipaddr
## NETSTAT
* netstat -a: shows all listening ports and established connections.
* netstat -at or netstat -au can also be used to list TCP or UDP protocols respectively.
* netstat -l
* netstat -s: list network usage statistics by protocol (below) This can also be used with the -t or -u options to limit the output to a specific protocol. 
* netstat -tp: list connections with the service name and PID information.(netstat -ltp)
* netstat -i: Shows interface statistics. We see below that “eth0” and “tun0” are more active than “tun1”.

### The netstat usage you will probably see most often in blog posts, write-ups, and courses is netstat -ano which could be broken down as follows;
    * -a: Display all sockets
    * -n: Do not resolve names
    * -o: Display timers

## FIND
    * find . -name flag1.txt: find the file named “flag1.txt” in the current directory
    * find /home -name flag1.txt: find the file names “flag1.txt” in the /home directory
    * find / -type d -name config: find the directory named config under “/”
    * find / -type f -perm 0777: find files with the 777 permissions (files readable, writable, and executable by all users)
    * find / -perm a=x: find executable files
    * find /home -user frank: find all files for user “frank” under “/home”
    * find / -mtime 10: find files that were modified in the last 10 days
    * find / -atime 10: find files that were accessed in the last 10 day
    * find / -cmin -60: find files changed within the last hour (60 minutes)
    * find / -amin -60: find files accesses within the last hour (60 minutes)
    * find / -size 50M: find files with a 50 MB size
## Folders and files that can be written to or executed from:
    * find / -writable -type d 2>/dev/null : Find world-writeable folders
    * find / -perm -222 -type d 2>/dev/null: Find world-writeable folders
    * find / -perm -o w -type d 2>/dev/null: Find world-writeable folders
    * find / -perm -o x -type d 2>/dev/null : Find world-executable folders
## Find development tools and supported languages:
    * find / -name perl*
    * find / -name python*
    * find / -name gcc*
## Find SUID
* find / -perm -u=s -type f 2>/dev/null: Find files with the SUID bit, which allows us to run the file with a higher privilege level than the current user. 
* find \-perm -4000 2>/dev/null

## General Linux Commands

As we are in the Linux realm, familiarity with Linux commands, in general, will be very useful. Please spend some time getting comfortable with commands such as find, locate, grep, cut, sort, etc. 

## Capabilities
* getcap -r / 2>/dev/null (sino funciona extiende el path)
* cron
* cat /etc/crontab
 
## AUTOMATED
* LinPeas: https://github.com/carlospolop/privilege-escalation-awesome-scripts-suite/tree/master/linPEAS
* LinEnum: https://github.com/rebootuser/LinEnum
* LES (Linux Exploit Suggester): https://github.com/mzet-/linux-exploit-suggester
* Linux Smart Enumeration: https://github.com/diego-treitos/linux-smart-enumeration
* Linux Priv Checker: https://github.com/linted/linuxprivchecker
