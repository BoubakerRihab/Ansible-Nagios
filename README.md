"# Ansible-Nagios" 
# 1-create AWS ubuntu intance for the client
Preparing for ansible on client
$ sudo apt-get install python -y
$nano /etc/ssh/sshd_config
## change:
## PasswordAuthentication no
## to
## PasswordAuthentication yes
********
# change password:
$sudo passwd username
#restart sshd:
$sudo service sshd restart

# 2-Configuring ansible on server
$sudo apt-add-repository ppa:ansible/ansible.
$ssh-keygen
##leave name as default~ [ENTRER]
##[ENTRER]
##[ENTRER]
$ sudo ssh-copy-id ubuntu@ipAddresseOfWebServer1
$ssh ubuntu@ipAddresseOfWebServer1
## last 2 comands same steps for other servers
## add servers ip adresses to the default ansible hosts file, which can be found in the directory /etc/ansible/hosts like this:
$ cat /etc/ansible/hosts
## inside the file
[webservers]
ipAdressOfWebServer1
ipAdressOfWebServer2
[dbservers]
ipAdressOfDBServer1
ipAdressOfDBServer2
