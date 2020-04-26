# Docker 1. Docker Installation
```
Docker Introduction: 29-Feb-2020

Print the list of docker images:
# docker ps

Start/Load docker OS:
# docker run -t -i ubuntu:14.04
This will take you to new terminal interface of ubuntu terminal.

exit to come out back to Redhat terminal.

Remove/delete docker image
# docker rm brave_zhukovsky
# docker rm -f brave_zhukovsky

check if deleted correctly:
# docker ps

we can launch oracle instance, mysql instance in one sec.

docker is different from Vagrant and virtual environment, docker is better than these tools.

-----------------------------
Remove docker if previously installed:
# systemctl stop docker
# yum remove docker ce

Command to install docker :
# curl -sSL https://get.docker.com | sh
This will generate an error as Redhat8 doesn't support  docker ce.

This is checking operating system name.
To resolve this error, 

search 'docker rpm download', first link.
select version:
docker-ce-19.03.6-3.e17x86_64.rpm
released on 2020-02-13 (around)

either we can go to this link, download and install. But, in Redhat there might be some dependency, so ask yum to help.

copy the web link and update the yum, this is called as configuring yum:
# cd /etc/yum.repos.d/
# ls
# gedit docker.repo
create a file with following details:

[docker]
baseurl=https://download.docker.com/linux/centos/7/x86_64/stable/
gpgcheck=0

Note that below command automatically creates this yum repository.
# curl -sSL https://get.docker.com | sh
Thus instead of running above command we have manually configured yum repository.

Now we need docker-ce command to install docker, hence, check if it is available:
# dnf list docker-ce
it is available as per docker repo.

Install docker now:
# dnf install docker-ce
Note this will fail, as there  is a dependency and there are multiple version of that file.
So add --nobest option.

Check if docker is installed or not?
# rpm -q docker-ce
docker-ce-18.09.1-3.el7.x86_64
Great. It is installed.
----------------------------------------
Now we need OS Image / Docker Image

Go to site http://hub.docker.com/
Search for 'Ubuntu'.
To download the latest version by entering following command where docker is running:
# docker pull ubuntu

To download particular version enter command with version number:
#docker pull ubuntu:14.04

to see the downloaded images:
# docker images

Vocabulary:
On Bare Metal 		- OS
On Virtualiazation 	- VM / guest M
On Cloud 		- Instance
On top of docker	- OS / Container

to check how many os running, container running:
# docker ps

to launch and get the interactive terminal:
# docker run -t -i ubuntu:14.04
This will open docker image with docker id in the prompt.

exit to come out of docker.
```
