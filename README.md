# A Simple Flask App in Docker 

## Description
This is a simple Flask web application that has been containerized using Docker.

## Features
- Used an Ubuntu base image to build a custome image which contains Flask app

## Prerequisites
Make sure you have the following installed on your machine:
- [Docker](https://www.docker.com)

## Installation

To get started with the Flask app in Docker, follow these steps:

### 1. Clone the repository
First, clone this repository to your local machine:
```bash
git clone https://github.com/AdithyaBhatGS/python-docker-app
```
### 2.Installing Docker on your Ubuntu machine:
Update the apt repo
```bash
sudo apt update
```

### 3.Install Docker
```bash
sudo apt install docker.io -y
```

### 4.Verify installation
Pulls a container image **hello-world**
```bash
docker run hello-world
```
### 5.Check the status of docker daemon
```bash
sudo systemctl status docker
```
### 6.Run the docker daemon
```bash
sudo systemctl start docker
```

### 7.Granting acess for the user to run docker commands
```bash
sudo usermod -aG docker ubuntu
```
## Build, push and run the container

### Login to DockerHub
- Initially signup to DockerHub, a native image registry from Docker
- Once successful in signing up, just follow the below steps
```bash
docker login
```
### Change the diretory
```bash
cd ~/<folder-name>/python-docker-app
```
### Build the image
```bash
docker build -t 5000:5000 <user_name>/<image_name>:<tag> .
```
### Push the image
```bash
docker push <user_name>/<image_name>:tag
```
### Run the image
```bash
docker run -p 5000:5000 <username>/<image_name>:tag
```

### Now check the app

- On local host
    *http://localhost:5000*
- On EC2
    *http://<EC2_PUBLIC_IP>:5000*



