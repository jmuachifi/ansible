# Ansible
Learning Ansible
## Install Ansible - Linux/Ubuntu
```
sudo apt update
sudo apt install software-properties-common
udo add-apt-repository --yes --update ppa:ansible/ansible
sudo apt install ansible
```
## Edit host file
Edit /etc/ansible/hosts to include the IP addresses of client server <br>
```
sudo vim /etc/ansible/hosts
```
## Test connectivity
```
ansible «name of the sevrer here» -m ping -k
```
Please, don't put the  name of the server inside «»

