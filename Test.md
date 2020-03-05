# Red Hat & Python: Summary for 02-Mar-2020: 

Server-Client concept
Server -> who gives the service / server can give or deny the service.
Client -> who takes the service / client is the one who goes to the server.

- pwd

If ssh access has been given to anyone, they can do anything on your machine.
ssh 192.168.0.162 cat /root/vimal.html

Creating and configuring a server both are different things.
Today we will see configuring a server: (This is without ssh)

For different server, we have different protocols <br/>
3-Steps Process:
1.	Install software (for us using rpm)
2.	Setup (look and feel)
3.	Execute

HTTPD (Apache) – Apache Webserver: (Configuring Apache webserver)

This is web hosting in other words.

-	Ifconfig enp0s3
-	Check : rpm –q httpd
-	Dnf install httpd
-	Check: dnf list httpd
-	pwd
-	cd var/www/html/
-	ls

copy / webhosting / deploy - all these terms are same.

To start web services:
-	Systemctl start httpd

Web server -> web client

Two steps at client side:
1.	Software called client side software e.g. browser
2.	Connectivity
3.	IP address of server
4.	Three things (which comprise the URL)
a.	How client wants to connect / protocol
b.	Where i.e. ip address
c.	Page name

Network packets / traffic : rhcl firewall is not allowing to access any folder:
Let us temporary disable firewall. Note that this is not a best practice.
-	systemctl stop firewalld

The place where we save our file, is called as documentRoot

# Red Hat & Python: Summary for 05-Mar-2020: 

-	systemctl status httpd (d stands for  daemon)

Service failed because: SELinux security was prohibiting the out of range port number

SELinux is a one of linux security.

SELinux alter:
Check current status:
-	getenforce <BR/>
Enforcing
-	setenforce 0 <BR/>
Permissive
-	setenforce 1 <BR/>
Enforcing

Nmap is a scanning tool to scan open ip addresses.
-	Yum install nmap
-	nmap -sP 192.168.0.162
-	nmap -sT 192.168.0.162
-	nmap -sT 1111 192.168.0.162

Check port

-	nmap -sT p 1111 192.168.0.162

Webserver can read from vimal folder not from html folder.
Priority goes to latest included files: 

Same way yum.conf is original file and not yum.repos.d:

Default directory index: 

Que: How to change the  document folder.

Firewall security -> network level <BR/>
SELinux security -> File system and processes
