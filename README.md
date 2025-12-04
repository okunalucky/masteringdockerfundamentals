# Mastering Docker Fundamentals

- ‎What is Docker?
Docker is an open-source platform that automates the deployment, scaling, and management of applications within containers. 
‎
‎
- ‎Why Use Docker?
‎
-Portability: Run your applications anywhere Docker is installed—be it on a developer's laptop, a testing environment, or in production.
‎
‎-Isolation: Each container operates independently, minimizing conflicts and enhancing security.

- How to install docker on Amazon Linux 2023 Ami 

   -spin up an ec2 instance and under advanced, paste in the code for the user data.
‎
‎
```sh
‎#!/bin/bash
‎# Updates installed packages
‎sudo dnf update -y
‎
‎# Sets the system hostname to "docker"
‎sudo hostnamectl set-hostname docker 
‎
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
