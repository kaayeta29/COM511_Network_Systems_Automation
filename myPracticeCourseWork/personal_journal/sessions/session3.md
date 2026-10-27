[Personal Learning Record](../../personal_journal/personal_journal.md) | [Session Notes](../sessions/README.md) 

# Session 3

## Topics covered
*What topics were covered in this session*
During Session 3, I continued learning about network automation and how Ansible can be used to manage multiple Linux machines.
The main topics covered were:
Introduction to Ansible and its role in network automation.
Understanding the difference between a controller and managed nodes.
Using Vagrant and VirtualBox to create multiple Ubuntu virtual machines.
Configuring network connections between virtual machines.
Understanding Ansible inventory files and playbooks.
Introduction to automated software installation using Ansible.
Working with Apache web servers.
## Personal Notes and research following this session
*Which class sessions and personal research refers to technology in this proposal. Link to examples.*
 learned that Ansible is an automation tool that allows system administrators to manage multiple servers from one central machine.
In our practical environment, we used three Ubuntu virtual machines:
ansible_controller — the main machine used to manage other systems.
ubuntu_1 — the first client machine.
ubuntu_2 — the second client machine.
I learned that Ansible uses SSH to communicate with managed Linux machines and can execute tasks without manually configuring each server separately.
I also learned about Ansible playbooks, which are written in YAML and describe the tasks that should be completed automatically.
Another important concept was the inventory file, which contains information about the machines Ansible needs to manage.
I researched how Apache works as a web server and how automation can help install and configure software across several machines.

## Exercises and results
*What exercises did you complete. What results. Screen shots and notes*
During the practical session, I worked with Vagrant, VirtualBox, Ubuntu and Ansible.
The exercises included:
Opened the course project and located the Vagrant configuration files.
Started the virtual machines using vagrant up.
Connected to the Ansible controller using vagrant ssh.
Checked the network connections between the virtual machines.
Worked with Ansible inventory files to identify managed machines.
Practised using Ansible to communicate with Ubuntu clients.
Worked on installing and configuring Apache using automation.
Some commands used during the practical work included:
vagrant up
vagrant ssh
ip a
ansible all -m ping
sudo systemctl status apache2
I experienced some problems with virtual machines not responding correctly and commands taking longer than expected.
I had to check the virtual machine status, network configuration and terminal commands to identify the problems.
These exercises helped me gain more experience with troubleshooting Linux virtual machines.
## Summary of learning
*What did you learn through these exercises*
This session helped me understand how Ansible can simplify network and system administration.
I learned the difference between an Ansible controller and managed nodes, how inventory files work and how playbooks can automate repetitive tasks.
I also improved my understanding of Linux commands, virtual machine networking and Apache web servers.
The most important thing I learned was that automation allows administrators to manage several machines more efficiently and consistently instead of configuring each one manually.
These skills are useful in Cyber Security because correctly configured and regularly maintained systems can reduce configuration errors and security risks.
