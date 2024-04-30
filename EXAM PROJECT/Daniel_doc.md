# EXAM PROJECT DOCUMENTATION 
### 1. the project contains the automation and provisioning of two Ubuntu-based servers, named “Master” and “Slave”, using Vagrant, with a bash script to automate the deployment of a LAMP (Linux, Apache, MySQL, PHP) stack, and cloned a PHP application from GitHub, with all necessary packages, and configured Apache web server and MySQL while using ansible to execute the bash script on the Slave node and cronjob to create check the server's uptime every 12:00am. the bash script is reusable and readable and can be accessible through the following repository: https://github.com/Daniel-Aderinto/EXAM-PROJECT.git

### 2. Provisioning of "master" and "slave"
the file "vagrant-master.sh" when runned/executed, spines up the two ubuntu master and slave machines while creating a vagrantfile.


### 3. laravel deployment on master node
the file "latest.sh" deploys laravel cloned from github repository only on the master node. https://github.com/laravel/laravel.

![larave installation](<larave installation.png>)


![larave page (192.168.56.2)](<larave page (192.168.56.2).png>)


### 4. the ansible playbook
in the absible-playbook directory contains ansible.cfg, inventory, playbook.yml and a directory called "files"
#### a. Ansible.cfg:- This is the brain and the heart of Ansible, the file that governs the behavior of all interactions performed by the control node.

#### b. Iventory:-the inventory is a list of managed nodes, or hosts, that Ansible deploys and configures. this inventory carries the ip address of the slave node in this project.

#### c. playbook.yml:- the Ansible Playbook in this project contains the blueprint of automation tasks on the slave node, which are IT actions executed with limited manual effort, across an inventory of IT solutions.

#### d. files:- contains the file "latest.sh" which the playbook use to deploy laravel cloned from github repository only on the slave node. https://github.com/laravel/laravel.git


![ansible playbook successfully](<ansible playbook successfully.png>)


![larave page (192.168.56.3)](<larave page (192.168.56.3).png>)
