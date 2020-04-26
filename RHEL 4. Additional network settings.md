#RHEL 4. Additional network settings
```
netstat -tnlp

Try changing the port number from 80 to 81 or any other  number.
# systemctl restart httpd
If this is failed, check:
# netstat -tnlp

check with command
# journalctl -xe
This might been happening because of SELinux.

We can ask SeLinux to update its database and allow us to access 1234 port for my httpd program. 
OR 
Disable SeLinux
# 


using nmap ideally is illegal, use it wit proper permission
OR use on your two laptop

list the live ip
#nmap -sP 192.168.0.1-255

list the available ports
# nmap -sT 192.168.0.100

detailed scanning the port:
# nmap -sT -p 1111 -sV 192.168.0.162

note the folders:
/etc/httpd/conf/
/etc/httpd/conf.d/
/var/www/html/
```
