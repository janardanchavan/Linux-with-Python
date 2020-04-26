# Docker 2. Docker Session1
```
Check if docker community edition is installed:
# rpm -q docker-ce
docker-ce-18.09.1-3.el7.x86_64

Check if docker service is running?:
# systemctl status docker

To start docker:
# systemctl start docker

To enable docker start on each reboot:
# systemctl enable docker

To see detailed info about the docker:
# docker info
info like version, licesence, OS on which it is running, etc.

To see current consumption of RAM on base Redhat system:
# free -m

Keep on running above command every one second:
# watch -n 1 free -m

See the list of all the OS currently running or maybe stopped:
# docker ps -a

Start the docker os without starting the interactive terminal with name or container id (i.e. running docker image at the background):
# docker start sad_spence

//check with command 'docker ps -a'

# enter into the docker image:
# docker attach sad_spence <┘

While launching docker image/os, it assigned random id to the running os. However, we can give our own name as well.
# docker run -it --name janardanos centos:7
you can also give your logical name that make sense: hadoop, apache  server, spark, database, etc.

If i try to check ifconfig command, it fails.
# ifconfig
bash: ifconfig: comamnd not found

on base machine:
----------------
What is the location of ifconfig command:
#which ifconfig
/use/sbin/ifconfig

Which software this command come from?
# rpm -q -f /use/sbin/ifconfig
net-tools-2.2-0.51.20160912git.el8.x86_64

On docker image:
----------------
This means software 'net-tools' is not there. check it:
# rpm -q net-tools
package net-tools is not installed

What ever commands you run in Redhat, exact command you run in centos.
Note: Rhel is not available freely, you have to purchase subscribed license.

Note that inside the container, yum is already been configured. Guys who have created centos:7 image, they have given us yum pre-configured.
Check:
# cd /etc/yum.repos.d/
# ls
CentOS-Base.repo	CentOS-Media.repo
CentOS-fasttrack.repo	CentOS-CR.repo
CentOS-Sources.repo	CentOS-Debuginfo.repo
CentOS-Vault.repo

Install net-tools on docker image, this will download from internet and install
# yum install net-tools
*** Receiving an error ***

Troubleshooting:
Check if your base OS has connectivity:
# ping goo.gl
***Error.

Check the docker "server version":
# docker version
try to use '18.09.x', if updated version, you might face internet connectivity error.
Also if you while launching docker you are facing error with message containing 'OSI' or "permission denied": it is because of SELinux security.
*********

Note that what ever you save inside the container it is temporary. Once you close the container it losses.
You have to run only the respective image with associated id.
Till the time you have not terminated the os, data will be there.
check the list of all the os:
# docker ps -a

To delete the image permanently:
# docker rm dc2d3d5e7fef
* Now you can't get your data.

another example of firefox
# yum install firefox


-------------------
To remove actual image itself:
# docker rmi centos:latest
** you might receive an error as this imgage is used by some other os

You can remove it forcefully
# docker rmi centos:latest -f

---------------------------
Just for information, docker commands are groups with container prefix. These are new commands, called Management Commands.

Eg. check running containers
# docker container ps

List all the containers running or stopped:
# docker container ls -a

show only id
# docker container ls -a -q

******* DO NOT RUN THIS COMMAND ********
You can pass these ids (enclosed in $ and brackets) to docker em command:
# docker rm $(docker container ls -a -q)
** might receive error, because of in use.

You can also forcefully remove these ids
# docker rm -f $(docker container ls -a -q)

newer command 
# docker container rm -f $(docker container ls -a -q)

Note this is not removing images, rather removing existing os.
******* DO NOT RUN THIS COMMAND ********

to come out of container os without closing it:
Ctrl+p and Ctrl+q
OR
Ctrl+p (dont leave ctrl) q (now leave ctrl)

To run a program without manually opening the docker image:
# docker run -it --name z1 centos:7 date

Cross-check with below command, you will find a new container os created with z1 name and executed before few seconds:
# docker ps -a

to run a program and terminate OS after execution:
# docker run -it --name z3 --rm centos:7 date

To download some file from url:
# docker run -it --name z3 --rm centos:7 wget url

Selenium / maven etc. you should have those commands in image.
--------------------------------------
How to create your own image:

```
