# **Automated LAMP Stack Deployment with Vagrant and Ansible**

This project automates the provisioning of two Ubuntu-based servers, named 'Master' and 'Slave', using Vagrant and Ansible. It deploys a LAMP (Linux, Apache, MySQL, PHP) stack on the Master, utilizes Ansible to deploy the same application on the Slave node remotely, and sets up a cron job to check the server's uptime every 12 am.

## **Requirements**
- Vagrant
- VirtualBox (or any other supported provider by Vagrant)
- Ansible

