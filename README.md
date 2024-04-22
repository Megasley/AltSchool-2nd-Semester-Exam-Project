# **Automated LAMP Stack Deployment with Vagrant and Ansible**

This project automates the provisioning of two Ubuntu-based servers, named 'Master' and 'Slave', using Vagrant and Ansible. It deploys a LAMP (Linux, Apache, MySQL, PHP) stack on the Master, utilizes Ansible to deploy the same application on the Slave node remotely, and sets up a cron job to check the server's uptime every 12 am.

## **Requirements**
- Vagrant
- VirtualBox (or any other supported provider by Vagrant)
- Ansible

## Setting Up the Environment
1. Execute `vagrant up` to provision the VMs defined in the `Vagrantfile`.
2. SSH into the Master node: `vagrant ssh Master`.
3. Execute the bash script to deploy the LAMP stack: `./deploy.sh`.
4. Execute the Ansible playbook: `ansible-playbook playbook.yaml`.
```console
ansible all -i host-inventory -m ping
ansible-playbook playbook.yaml -i host-inventory --check
ansible-playbook playbook.yaml -i host-inventory
```

## **Repository Structure**
**Vagrantfile:** Defines the configuration for provisioning VMs.
**deploy.sh:** Bash script to deploy the LAMP stack.
**playbook.yaml:** Ansible playbook to copy and execute the bash script on the Slave node.
**docs/:** Contains guides and screenshots proof of the app accessibility
**README.md:** This file.
