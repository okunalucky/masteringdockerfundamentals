

<img width="851" height="481" alt="Image" src="https://github.com/user-attachments/assets/e7d621bc-925f-4bdd-8e36-294a4220aee4" />


- ‎What is Docker?
Docker is an open-source platform that automates the deployment, scaling, and management of applications within containers. 
‎
‎
- ‎Why Use Docker?
- Portability: Run your applications anywhere Docker is installed—be it on a developer's laptop, a testing environment, or in production.
- Isolation: Each container operates independently, minimizing conflicts and enhancing security.

- How to install docker on Amazon Linux 2023 Ami

- Launch an amzon linux 2023, t2 micro and name it Docker




<img width="878" height="485" alt="Image" src="https://github.com/user-attachments/assets/2c2dc6b9-724b-419e-af77-6fdd401786b7" />



- Add a key pair and configure the network settings





<img width="857" height="464" alt="Image" src="https://github.com/user-attachments/assets/01bc218f-a845-479d-9a45-0d5564e312c1" />


- Under Advanced setting, paste in the userdata 





<img width="1311" height="389" alt="Image" src="https://github.com/user-attachments/assets/ecde3098-0711-4290-8fcd-0fdef2643e46" />



‎
‎
```sh
‎#!/bin/bash
‎# Updates installed packages
‎sudo dnf update -y
‎
‎# Sets the system hostname to "docker"
‎sudo hostnamectl set-hostname docker

‎# Installs the Docker package
‎sudo dnf install docker -y
‎
‎# Starts the Docker service
‎sudo systemctl start docker
‎
‎# Enables Docker to start on boot
‎sudo systemctl enable docker
‎
‎# Adds the ec2-user to the Docker group for running Docker commands without sudo
‎sudo usermod -aG docker ec2-user
‎
‎# Switches to the ec2-user account
‎sudo su - ec2-user
```

- Docker Image

‎Docker Image is used to create Docker containers. Images are built from Dockerfiles and contain everything needed to run an application, including the code, runtime, libraries, and environment variables.
```sh‎


‎Build an Image: Use the docker build command.
docker build -t your_image_name:tag .
‎ 
‎List Images: Use the docker images command to see all images on your system.
docker images
‎
‎Remove an Image: Use the docker rmi command.
docker rmi your_image_name:tag
```
