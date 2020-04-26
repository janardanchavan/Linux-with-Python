# RHEL 2. Setting up Web Browser
```
I am going to configure my ip 192.168.1.105 as my web server.


At Server side : 192.168.1.105 (3 steps needed)
check if software is already installed or not?
# rpm -q httpd

1. install httpd
# dnf install httpd

not installed, hence, let us check if httpd software is installed or not?
# yum list httpd
OR
# dnf list httpd

2. tell web server, i have web pages, please use these web pages.

default folder for web pages: /var/www/html/

create a file janardan.html
This is my first webpage on linux.

3. start web service / httpd
REHL 5/6 - Service
REHL 8 - systemctl

start service with following command
# systemctl start httpd


At client side (2 steps needed)
1. Client software
   Now provide these three things:
   1. how do want to connect to the server
   2. where is your server, ip
   3. page
2. Connectivity

Try typing following address in your host machine's browser:
http://192.168.1.105/janardan.html

Error: page will not load as firewall is denying access.

disable firewall:
# systemctl stop firewalld

check service status
# systemctl status httpd

check if the service is disabled?
press q to come out from the output.

Enable service
# systemctl enable httpd

By enabling service, on every reboot, service will not stop.
```
