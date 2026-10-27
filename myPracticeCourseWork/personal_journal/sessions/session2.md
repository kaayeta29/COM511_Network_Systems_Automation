[Personal Learning Record](../../personal_journal/personal_journal.md) | [Session Notes](../sessions/README.md) 

# Session 2

## Topics covered
*What topics were covered in this session*
During this session, I learned about Infrastructure as Code (IaC), virtualisation and how Vagrant can be used to create and manage virtual machines automatically.
The main topics included:
Introduction to Infrastructure as Code (IaC).
Using Vagrant with Oracle VirtualBox.
Understanding the purpose of a Vagrantfile.
Creating and starting Ubuntu 24.04 virtual machines.
Basic Linux commands and SSH connections.
Introduction to automated software installation and provisioning.
## Personal Notes and research following this session
*Which class sessions and personal research refers to technology in this proposal. Link to examples.*
I learned that Vagrant is a tool that allows administrators to create and configure virtual machines using configuration files instead of setting everything up manually.
VirtualBox provides the virtualisation environment, while Vagrant manages the configuration and deployment of the machines.
I also learned about the importance of Infrastructure as Code. It makes managing multiple servers easier because configurations can be reused and shared.
I researched how SSH allows me to access a virtual machine through the terminal and how Apache can be used to host web pages on an Ubuntu server.
## Exercises and results
*What exercises did you complete. What results. Screen shots and notes*
During the practical exercises, I worked with Vagrant, VirtualBox and Ubuntu 24.04.
I completed the following tasks:
Cloned the course repository from GitHub.
Located the correct Vagrantfile in the session examples.
Started an Ubuntu virtual machine using vagrant up --provider=virtualbox.
Connected to the machine using vagrant ssh.
Checked the Apache web server using sudo systemctl status apache2.
Tested the example web page through a browser using http://localhost:8081/examplewebpage.html.
I also experienced some difficulties with locating the correct Vagrantfile and starting virtual machines on my MacBook. This helped me understand the importance of checking the working directory and virtualisation compatibility.
The final result was that I managed to start the Ubuntu environment and access the example Apache web page successfully.
## Summary of learning
*What did you learn through these exercises*
This session helped me understand how virtualisation and automation work together in network administration.
I learned how to use Vagrant to create an Ubuntu virtual machine, connect to it using SSH and check whether a web server was running.
I also gained more confidence using the Linux terminal and troubleshooting configuration problems.
These skills will be useful for future sessions involving Ansible, DHCP, DNS and automated network management.
