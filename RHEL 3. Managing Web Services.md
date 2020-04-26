# RHEL 3. Managing Web Services
```
Check what all the programs/processes running on the system
# ps -aux

to see all the process that has a port number:
# netstat -tnlp

default port number for webservice: 80
Thus, we can type our path as following also:
http://192.168.1.105:80/janardan.html

Apache configuration file is stored at following address:
/etc/httpd/conf
file name: httpd.conf

Check for the line as:
Listen 80

change it to 81 and check status by command :
# netstat - tnlp
Error: because we have to restart the services because changes not made in memory

2. Default Document Root Folder
Default Document Root folder is "/var/www/conf"
which is saved in httpd.conf file as:
DocumentRoot = "/var/www/html"


3. After restart page was loading, hence add the port permanently
# firewall-cmd --permanent --add-port=80/tcp
# firewall-cmd --reload

OR
$ sudo ufw allow 80/tcp
$ sudo ufw reload

Additional commands not checked
# firewall-cmd --zone=public --add-masquerade --permanent

// Specifically allow incoming traffic on port 80/443 (nothing new here)
# firewall-cmd --zone=public --add-port=80/tcp
# firewall-cmd --zone=public --add-port=443/tcp

//Reload firewall to apply permanent rules
# firewall-cmd --reload

//Restart httpd service
```
