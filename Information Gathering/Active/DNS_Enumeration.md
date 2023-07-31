# DNS Enumeration
Try to retrieve data like: ns, a, mx, ptr, cname, txt.

* host -d site.com
* host -t data site.com
* host idontexist.site.com
* for ip in $(cat list.txt); do host $ip.site.com; done
* dnsrecon: https://www.kali.org/tools/dnsrecon/
* dnsdumpster: https://dnsdumpster.com/
* dnsenum: https://www.kali.org/tools/dnsenum/
* Reverse lookup: https://www.nslookup.io/
* Assetfinder: https://www.kali.org/tools/assetfinder/
* Phonebook: https://phonebook.cz/
* Sublist3r: https://www.kali.org/tools/sublist3r/
* CTRF: https://offsec.tools/tool/ctfr
* dig: https://toolbox.googleapps.com/apps/dig/ or in yout console use dig --help

* Here are some more: https://book.hacktricks.xyz/network-services-pentesting/pentesting-dns
