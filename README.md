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

share volume from existing container with new container - Container to Container sharing
----------------------------------------------------------------------------------------
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

share volume from host to container - Host to Container sharing
----------------------------------------------------------------------------------------
![image](https://user-images.githubusercontent.com/51961967/213863606-ea1255f9-6591-43fd-8905-24adc6df321c.png)

![image](https://user-images.githubusercontent.com/51961967/213863621-6aafd366-1d4b-4f41-9487-216b09a7f5ce.png)


docker volume commands
----------------------------

![image](https://user-images.githubusercontent.com/51961967/213863358-117d5a6c-01f7-4c91-9542-60dc2c286b9e.png)


docker port expose
---------------------

Logical Ports - 0 - 65535
Logical ports work at transport layer.

![image](https://user-images.githubusercontent.com/51961967/213865626-e4d47592-4efd-4674-a925-232c0adec4da.png)


![image](https://user-images.githubusercontent.com/51961967/213865663-e0f51cd4-b4d3-4382-b755-1a6f5c052778.png)


![image](https://user-images.githubusercontent.com/51961967/213866273-cd8a3e64-ca5d-43bf-92c4-3cd31f2bd78d.png)

https://www.cloudbees.com/blog/docker-expose-port-what-it-means-and-what-it-doesnt-mean


docker attach vs docker exec

![image](https://user-images.githubusercontent.com/51961967/213867656-769a1ce1-dc94-4baa-8983-2d9e5e26cfba.png)


docker expose vs publish

![image](https://user-images.githubusercontent.com/51961967/213867901-dec53fd2-435a-45b8-a1a9-247d5fcd8a38.png)

![image](https://user-images.githubusercontent.com/51961967/213867953-40ecacf5-c10a-4c8e-a9f1-da66e090a3c1.png)

dockerhub
----------------------------------------
![image](https://user-images.githubusercontent.com/51961967/216921172-f89af5b7-710c-4283-b1c0-d4c86c7ef86b.png)

![image](https://user-images.githubusercontent.com/51961967/216922395-e0290158-2c2d-4ba1-a770-b91ddca1cea7.png)


Stop and remove all containers and images
-----------------------------------------
![image](https://user-images.githubusercontent.com/51961967/216918704-876fc8d7-7463-46f6-beba-ff321e69b030.png)



Docker commands
-----------------------
https://faun.pub/useful-docker-commands-and-aliases-9ea79191832f

https://www.youtube.com/watch?v=RqTEHSBrYFw   ****4 hr session****


# Use the official ASP.NET Core 3.1 runtime image as the base image
FROM mcr.microsoft.com/dotnet/core/aspnet:3.1 AS base
WORKDIR /app
EXPOSE 80

# Use the official ASP.NET Core 3.1 SDK image as the build image
FROM mcr.microsoft.com/dotnet/core/sdk:3.1 AS build
WORKDIR /src

# Create a non-root user (svcio) with the appropriate permissions
RUN useradd -u 1234 -m svcio && \
    mkdir -p /etc/ssl/sedaesp && \
    mkdir -p /usr/lib/ssl && \
    chown -R svcio:svcio /etc/ssl/sedaesp /usr/lib/ssl

# Copy the solution file and restore dependencies as the non-root user
COPY ["webapp.sln", "webapp/"]
COPY ["webapp/webapp/webapp.csproj", "webapp/webapp/"]
COPY ["webapp/dal/dal.csproj", "webapp/dal/"]
COPY ["webapp/bl/bl.csproj", "webapp/bl/"]
COPY ["webapp/nuget.config", "webapp/"]

USER svcio

RUN dotnet restore "webapp.sln"

# Copy only the necessary files for building and publishing
COPY ["webapp/webapp/", "webapp/webapp/"]
COPY ["webapp/dal/", "webapp/dal/"]
COPY ["webapp/bl/", "webapp/bl/"]

# Modify files in /usr/lib/ssl using sed
# Replace '/usr/lib/ssl' and '/etc/ssl/sedaesp' with the actual paths
RUN sed -i 's/oldtext/newtext/' /usr/lib/ssl/openssl.cnf

# Copy the certificate file from the build agent to the container
COPY ["src/certificates/in-lan.pem", "/usr/local/share/ca-certificates/ca-cert.crt"]

# Update the certificate store
RUN update-ca-certificates

# Build the application
WORKDIR "/src/webapp"
RUN dotnet build "webapp.csproj" -c Release -o /app/build

# Publish the application
FROM build AS publish
RUN dotnet publish "webapp.csproj" -c Release -o /app/publish

# Build the final image using the published files
FROM base AS final
WORKDIR /app
COPY --from=publish /app/publish .
ENTRYPOINT ["dotnet", "webapp.dll"]

# Use the official ASP.NET 3.1 runtime as the base image
FROM mcr.microsoft.com/dotnet/aspnet:3.1 AS base
WORKDIR /app

# Create a non-root user with a specific UID and GID
# Adjust the values as needed to match your requirements
RUN groupadd -g 1001 myusergroup && useradd -u 1001 -g myusergroup -m -s /bin/bash myuser

# Set the working directory and grant ownership to the non-root user
RUN chown -R myuser:myusergroup /app

# Switch to the non-root user
USER myuser

# Expose the port your application listens on (if applicable)
EXPOSE 80

# Copy your published ASP.NET 3.1 application into the container
COPY --chown=myuser:myusergroup [your-published-app-directory] .

# Define the entry point for your application
CMD ["dotnet", "[YourApp.dll]"]

NUGET restore from Docker
-----------------------------
https://github.com/dotnet/dotnet-docker/blob/main/documentation/scenarios/nuget-credentials.md


https://blog.devops.dev/consuming-private-nuget-feeds-from-a-dockerfile-in-a-secure-and-devops-friendly-manner-b5c90ea90bba

https://www.4tecture.ch/blog/2020/08/31/Restore-Nuget-Packages-inside-a-Docker-Container/

https://github.com/dotnet/dotnet-docker/blob/main/documentation/scenarios/nuget-credentials.md

