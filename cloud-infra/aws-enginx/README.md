# Ansible AWS - Install/Update Enginx 

## Install Ansible - Linux/Ubuntu
```
sudo apt update
sudo apt install software-properties-common
udo add-apt-repository --yes --update ppa:ansible/ansible
sudo apt install ansible
```
You can check the official ansible documentation by clicnking [here](https://docs.ansible.com/ansible/latest/installation_guide/installation_distros.html#installing-ansible-on-ubuntu)<br>
## Edit host file
Edit /etc/ansible/hosts to include the IP addresses of client server <br>
```
sudo vim /etc/ansible/hosts
```
Put the instruction below into hosts file and change according to your needs.
```
[ec2_instances]
public_instance-0 ansible_host=54.191.155.198
public_instance-1 ansible_host=34.219.162.63
[ec2_instances:vars]
ansible_python_interpreter=/usr/bin/python3
ansible_user=ubuntu
ansible_ssh_private_key_file=~/.ssh/aws-key-lab2024.pem
```
## Test connectivity
```
ansible ec2_instances -m ping -k
```
![](https://github.com/jmuachifi/ansible/blob/main/cloud-infra/aws-enginx/images/ansible-test-ping-aws-ec2.png)
Please, don't put the  name of the server inside «»
