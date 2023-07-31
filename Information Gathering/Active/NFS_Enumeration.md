# Network File System Enumeration
Bla bla bla tips

## Change the IP if you need
* nmap -v -p 111 IP.1-254
* nmap -sV -p 111 --script=rpcinfo IP.1-254
* nmap -p111 --script nfs* IP
### If any directory is sharing we have to use "mount" to get access to that resources
* mkdir directory
* mount -o nolock IP:/directory ~/directory/
* GO AND FUCK THAT MACHINE
