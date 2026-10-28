[Personal Learning Record](../../personal_journal/personal_journal.md) | [Session Notes](../sessions/README.md) 

# Session 5

## Topics covered
*What topics were covered in this session*
In this session, we learned about Docker and containerisation and how they are used in network systems automation.
The main topics included:
Introduction to Docker and containerisation.
Differences between containers and virtual machines.
Installing and using Docker Desktop.
Docker images and containers.
Basic Docker commands such as docker run, docker ps, docker stop and docker rm.
Creating a Dockerfile and building a custom Docker image.
Installing and running an Apache web server inside a Docker container.
Using Vagrant and Ubuntu Linux to run Docker.
## Personal Notes and research following this session
*Which class sessions and personal research refers to technology in this proposal. Link to examples.*
I learned that Docker allows applications to run inside isolated containers. Containers are lightweight compared to traditional virtual machines because they share the host operating system kernel.
I also learned the difference between a Docker image and a container. An image is a template containing the application and its dependencies, while a container is a running instance of that image.
I used the following learning materials:
Docker Official Documentation
Docker Hub
How to Install Docker on Ubuntu 22.04 – DigitalOcean
COM511 Session 5 GitHub practical exercises.
## Exercises and results
*What exercises did you complete. What results. Screen shots and notes*
Exercise 5.1 – Docker Desktop
I used Docker Desktop on my MacBook to practise working with Ubuntu containers
I completed the following tasks:
Created and started Ubuntu containers.
Used docker exec to access a running container.
Installed networking utilities and tested connectivity using ping.
Installed Apache2 inside an Ubuntu container.
Started the Apache web server.
Created a Dockerfile to automate the installation of Apache.
Built a custom image using docker build -t my-apache ..
Created two Apache containers using ports 8081 and 8082.
Used docker ps and docker ps -a to check container status.
Stopped and removed containers.
Result: I successfully built a custom Docker image and ran Apache containers using Docker Desktop.
Exercise 5.2 – Docker on Linux using Vagrant
In the second exercise, I used Vagrant to create an Ubuntu Linux virtual machine with Docker.
I completed the following tasks:
Started the virtual machine using vagrant up
Connected to Ubuntu using vagrant ssh.
Navigated to the Docker Apache project directory.
Built the Apache image using:
docker build -t my-apache .
Started the Apache container using:
docker run -d -p 8081:80 --name apache-1 my-apache
Checked the running container using:
docker ps
Result: The Docker image was successfully built, and the Apache container was running with status Up. Port 8081 was mapped to port 80 inside the container.
The next verification step was to open http://192.168.56.10:8081/ in the browser to check the Apache default page.
Screenshots: Terminal output showing the Docker image build, running containers, port mapping and Vagrant environment.


## Summary of learning
*What did you learn through these exercises*
During Session 5, I learned how Docker works and why containerisation is useful in network systems automation.
I gained practical experience creating Docker containers, building custom images, running Apache web servers and managing containers using terminal commands.
I also learned how Docker can be used inside an Ubuntu virtual machine created with Vagrant.
These exercises helped me understand how applications can be deployed consistently across different environments and how Docker simplifies application management and deployment.
