# docker

![image](https://user-images.githubusercontent.com/51961967/209557423-d2489956-bb81-4199-be2c-d0a7cca00e53.png)


https://github.com/WolfgangOfner/MicroserviceDemo/blob/master/CustomerApi/CustomerApi/Dockerfile

https://github.com/burakince/docker-dotnet-sonarscanner/blob/master/Dockerfile

https://medium.com/@HoussemDellai/setup-sonarqube-in-a-docker-container-3c3908b624df

https://medium.com/@thiagoloureiro/code-analysis-with-sonarqube-docker-net-core-aee521ee8931

https://www.apriorit.com/dev-blog/748-qa-integrating-quality-control-into-cicd

https://www.mytechramblings.com/posts/running-a-sonarqube-scan-when-building-docker-image/

https://www.bogotobogo.com/DevOps/Docker/Docker_Prometheus_Grafana.php

https://geekflare.com/?s=docker&post_type=post

https://www.veritis.com/blog/top-five-docker-alternatives-that-can-boost-your-productivity/

https://github.com/dotnet-architecture/eShopOnContainers

https://medium.com/bb-tutorials-and-thoughts/how-to-run-a-react-app-as-a-container-on-azure-vm-b73094fdc28a

github actions
https://github.com/skills/publish-packages

https://sweetcode.io/?s=docker

https://sweetcode.io/dockerfile-best-practices-useful-secure/

Production ready dockerfile
https://medium.com/@marcong_54227/how-to-write-a-production-ready-dockerfile-58d18d4daddc


TugBoat CD for Docker
https://github.com/teknowafel/Tugboat


https://andrewlock.net/why-isnt-my-aspnetcore-app-in-docker-working/


Docker Vs Containerd
https://kodekloud.com/blog/docker-vs-containerd/


Docker is a Platform.
To Build, Run and Ship Applications consistently.

Reasons
Missing Files.
Version Mismatch.
Different Configuration settings.

Container is an isolated environment.
To run an application.

Virtual Machine is an abstraction of a machine(Physical Hardware)

We can run 2 Virtual Machines( Windows VM, Linux VM) on a Physical Server based on Mac Os using Hypervisor.

Hypervisor is a software.
To create and manage Virtual Machines.

Hypervisor Types:
Virtual Box(Cross Platform)
Vmware(Cross Platform)
Hyper-v(Windows Only)

Benefit of VM
Run 2 different App versions in isolation on same physical harware but 2 different VMs.

Problem of VM
Each VM needs a Full-Blown OS
Slow to start
Resource intensive

Containers
To run multiple applications in isolation
LightWeight
Use OS of the host
Start quickly
Need less hardware resources

Docker Architecture

![image](https://user-images.githubusercontent.com/51961967/212024729-fdf81669-504c-43aa-ad1d-c443727d35ff.png)

![image](https://user-images.githubusercontent.com/51961967/212025114-9b9da6eb-658f-4fad-bcb6-2f100c826e53.png)

Containers share the OS Kernel of the host whereas VMs have there own OS.

![image](https://user-images.githubusercontent.com/51961967/212025585-5ca56da2-f37a-4311-b8a0-174b22f254a0.png)

Each OS has its own kernel or engine which uses diff APIs. Due to this, a Windows App cannot be run on Linux.

![image](https://user-images.githubusercontent.com/51961967/212027032-45c53b1a-ca39-4a28-812d-95d8e21b9490.png)

docs.docker.com

![image](https://user-images.githubusercontent.com/51961967/212029265-4414eeda-0b96-4bc8-966b-7ce64cc37aed.png)


To check Docker Version run,
docker version

Dockerfile is a plain text file.
It contains a set of instructions.
To package the Application into an Image.

![image](https://user-images.githubusercontent.com/51961967/212042238-298ec846-af8a-49eb-bcde-304ba89df2e1.png)

![image](https://user-images.githubusercontent.com/51961967/212044414-e4d3a13d-90f2-44a4-af96-66a928a3f93e.png)

Container is a special process that has its own file system.

Application gets loaded inside the container.

![image](https://user-images.githubusercontent.com/51961967/212052615-e33efa90-510d-4c3a-8414-3fa441d34c6b.png)


mkdir hello-docker
cd hello-docker

apt upgrade
apt install nodejs

touch app.js
vi app.js
console.log("Hello Docker!");
Esc
`:x

nodejs app.js

![image](https://user-images.githubusercontent.com/51961967/212063342-9a69ddb7-20fa-4649-851a-31c1fb89aa19.png)


Dockerfile
![image](https://user-images.githubusercontent.com/51961967/212070877-3c721b41-77cc-4702-b806-a84d43f4bed5.png)

Build Docker Image
docker build -t hello-docker .

Check Docker Images
docker images
docker image ls
docker images --all

Run the Docker Image
docker run hello-docker

LINUX

Open Source
Case Sensitive
Dir / in Linux whereas \ in Windows
Everything is a file in Linux

![image](https://user-images.githubusercontent.com/51961967/212075414-86997c1e-04da-4d24-8595-74aa74de29ca.png)


![image](https://user-images.githubusercontent.com/51961967/212079191-5b0a6c4c-16c4-4e4e-8eb8-3e6ac01c5143.png)

root is the loggedin user
after @ is the machine or container id
/ is for root directory
# is with highest priveliges
$ is for limited priveliges

whoami

location of the program
echo $0

history of activities
history

Package Management


apt
advanced package tool

to list all the packages whether installed or not installed
apt list

to update package database
apt update

to install package
apt install nano

to uninstall package
apt remove nano
apt remove nano -y

File System

![image](https://user-images.githubusercontent.com/51961967/212083750-5c28bcce-3641-43c6-ab12-4579269a7c83.png)

![image](https://user-images.githubusercontent.com/51961967/212084043-02152814-6aee-4fe7-9d01-1228013e4aff.png)
bin  --> binaries or program files
boot --> booting files
dev  --> device files
etc  --> editable text configuration files
home --> home dir for users
root --> home for only root users
lib  --> software library dependancy files
var  --> variables like log files, frequently updated files
proc --> process files of running processes

Print Working Directory
pwd

List all the items
ls
ls -1 (less details)
ls -l (more details)

Change directory
cd

cd etc/a press tab to see all the dir starting with a

move one level up
cd ..

move two level up
cd ../..

move from any directory to root directory
cd ~

Manipulating files and directories
Create a new directory
mkdir test

Move or Rename a directory
mv test Docker
mv a.txt b.txt
mv b.txt /home

Create a new file
touch hello.txt

Create multiple files
touch learn{1..10}.txt

Remove multiple files
rm learn*
rm file.txt file2.txt file3.txt
rm -r (recursively)


Editing and viewing files
nano file1.txt

view file contents
cat file1.txt

more etc/adduser.conf  (Detailed file view with % but cannot move up, only down can be moved)

less etc/adduser.conf (Can move cursor up and down)

head -n 5 etc/adduser.conf

tail -n 5 etc/adduser.conf

Redirection

stdin  represents Keyboard
stdout represents Console/Screen

Display content from multiple files
cat file1.txt file2.txt
cat file1.txt > file2.txt
cat file1.txt file2.txt > combined.txt
echo "Append Content" >> combined.txt


Docker History

2008 - Founded as DotCloud  by Solomon Hykes in Paris.

2010 - Docker Inc was founded by Kamel Founadi, Solomon Hykes, and Sebastien Pahl during the Y Combinator Summer 2010 startup incubator group and launched in 2011

2013 - Docker released in March 2013

Docker is a set of platform as a service (PaaS) products.

Uses OS-level virtualization to deliver software in packages called containers. VM uses hardware level virtualization.

The service has both free and premium tiers. 

The software that hosts the containers is called Docker Engine.

Docker can be installed on any OS.

Docker Engine runs natively on Linux distribution.

Docker is written in Go language.

Docker 

![image](https://user-images.githubusercontent.com/51961967/212539254-69c51bd1-5b93-419e-a2f7-fa9b53bcb192.png)

 Advantages of Docker:
 No pre-allocation of RAM
 
 CI efficiency - same image used across deployment process
 
 Less Cost
 
 Light Weight - Less resource intensive like RAM, CPU
 
 Dis-Advantages of Docker:
 
 Docker is not a good solution for Application that needs a rich UI.
 
 No solution for data recovery & backup.
 
 Difficult to manage large number of containers.
 
 Does not provide cross-platform compatibility. App designed to run on docker container based on Windows, then it cannot run on Linux or vice-versa.
 
 Suitable when development and testing OS are same like, ubuntu --> ubuntu not ubuntu --> centos or rhel or any other linux distro
 
 

Dockerfile contains dependencies and required software.

Docker Container is a layered file system. Ubuntu-->Google Chrome-->Directory

Docker EcoSystem
------------------

![image](https://user-images.githubusercontent.com/51961967/212549436-0f5719aa-9d8e-4724-b862-ee7a63e333ef.png)

Components of Docker
--------------------
Docker Daemon/Engine

It runs on host OS.
Responsible for running Docker containers.
It can communicate with other daemons.


Docker Client

Users can communicate with Docker Daemon through Docker Client.
Uses commands and REST API to communicate with other Daemons.
Can communicate with more than one daemon.


Docker Host
Used to provide an environment to execute and run apps.
It contains the Docker daemon, images, containers, networks and storages.

Docker Registry
Stores and manages Docker images.
2 types of registry:
Public Registry  --> Images in Docker Hub is publicly available.
Private Registry --> Images are available within the enterprise.

Docker Images
ReadOnly Binary Templates used to create Docker Containers.
Contains dependencies and required software/config to run a program.


Ways to create Docker Images
----------------------------
Take image from Docker Hub
Create image from Dockerfile
Create image from existing docker container


Docker Container
It is a package that is needed to run the application.

It is like a Virtual Machine.

Images becomes containers when run on Docker Engine.


Docker Commands

which docker

To check docker version
docker -v or docker --version

To see all docker images present on your local machine
docker images

To find out different images in DockerHub
docker search nginx

To download image from DockerHub to local machine
docker pull nginx

To give name to the container, i--> interactive t--> terminal d-->dettach Run = Create + Start
docker run -itd --name testvm ubuntu /bin/bash

To check Service Docker status
service docker status
docker info

To start Docker Service
service docker start

To start Container
docker start testvm

To get inside the container
docker attach testvm

cat /etc/os-release

To list all the containers
docker ps -a

To list only running containers
docker ps

To stop container
docker stop testvm

To delete container
docker rm testvm

Can we remove the container that is already running. No, container needs to be stopped first.

![image](https://user-images.githubusercontent.com/51961967/213117420-8556f3f7-46a5-4ecf-a9f0-0ea26459cb25.png)

![image](https://user-images.githubusercontent.com/51961967/213120521-0ce2f8b8-b11a-4ad4-ade7-0a270069b7ce.png)



![image](https://user-images.githubusercontent.com/51961967/213120284-e77677f7-3e82-46ec-96cf-e1f3ea6e22bd.png)

FROM ubuntu
WORKDIR /tmp
RUN echo "Hare Krishna" > /tmp/testfile
ENV myname Sujith
COPY testfile1 /tmp
ADD test.tar.gz /tmp

Docker Volumes
https://stackoverflow.com/questions/34357252/docker-data-volume-vs-mounted-host-directory

Volume is simply a directory inside the container.
Declare directory as Volume and then share the Volume.
Even if we stop the container, we can access the Volume.
Volume will be created in one container.
You can declare directory as a volume only while creating the container.
You cant create a Volume from an existing container.
You can share volumes across any number of containers.
Volume will not be included when you update an image.
You can map volume in 2 ways:-

Container --> Container
Host --> Container

Volumes can be shared Host to Container and Container to Host.

Benefits of Docker Volume

Decoupling container from storage.
On deleting container Volume does not delete.
Share Volume among different containers.
Attach volume to containers.

share volume from existing container with new container
docker run -it --name container2 --privileged=true --volumes-from radheradhe222 ubuntu /bin/bash

touch krishna.txt

exit

docker start radheradhe222

docker attach radheradhe222

cd /volume2

ls

![image](https://user-images.githubusercontent.com/51961967/213659287-08e52c4e-ae89-44d9-b136-cfbdef82817b.png)

![image](https://user-images.githubusercontent.com/51961967/213659415-dce1c360-e50f-4e86-a311-cc9e04cd0361.png)



![image](https://user-images.githubusercontent.com/51961967/213660966-a3401f0e-25d5-4b85-83de-3120714bc42b.png)


![image](https://user-images.githubusercontent.com/51961967/213661314-e51c3872-78cd-4fc4-a4d2-2972d20c5f8f.png)
