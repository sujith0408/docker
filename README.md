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





