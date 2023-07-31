# SNMP ENUMERATION
* MIB TREE: snmpwalk -c public -v1 -t 10 IP
* Windows Users: snmpwalk -c public -v1 IP 1.3.6.1.4.1.77.1.2.25
* Running Processes: snmpwalk -c public -v1 IP 1.3.6.1.2.1.25.4.2.1.2
* Open TCP Ports: snmpwalk -c public -v1 IP 1.3.6.1.2.1.6.13.1.3
* Installed Sofware: snmpwalk -c public -v1 IP 1.3.6.1.2.1.25.6.3.1.2
* Also use nmap: https://book.hacktricks.xyz/network-services-pentesting/pentesting-snmp
