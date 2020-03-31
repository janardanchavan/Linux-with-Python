IIEC RISE ID: RISE2020_71_6_1
## Redhat & Python Summary for 31-Mar-2020:
#### 1st topic:  create a login and password.

    vim menu.py

before where to run

    passwd = input("Enter ur password: ")

    apass = "lw"
	if passwd != apass:
    print("Auth incorrect")
        exit()
    else
        your code

#### 2nd topic: stop echo back.

Due to 'echo back', character is displayed on the screen
telnet	X
http	X

use getpass() for entering password as it takes the input but doesn't echo back.
        import getpass

	x = getpass.getpass()

	x = getpass.getpass("Enter your string: ")

store password in : database,

compile program and convert into binary.

#### 3rd topic: Avoid typing password for ssh agian and again:
lots of way for authentication:
- password based authentication
- key based authentication (private key)

ssh-keygen command -  to gerate public/private rsa key pair.

command to be typed on A machine from where we are running command for another machine

This is a public key and password-less authentication.

To login to machine B:
- ssh-copy-id root@192.168.0.106

first time you have to type password, later on it is not required.

To check private key:
- cat /root/.ssh/id_rsa
