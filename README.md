# Docker-project

## Introduction 
Docker is a containersation tool helps us setup different types of environments depending upon requirement.It was launched in 2013 by Solomon Hykes and made a revolutionary changes in industry as it works on O.S level virtualisation.
                
## Preinstallation setup
I am using Rhel 7.5 as docker-host and docker will be sharing Kernel and libraries from docker-host.You can go for other docker-host too as per your choice.
                  
 ## Install
We are downloading docker-ce 18.3 version from internet by creating yum in docker-host as it will download all the dependency itself by putting url of docker rpm from internet. 

## Docker-service
This is one of the things where new learners stucks because of not having deep-dive knowledge of basic command.In our case the command is systemctl command .Many says that this cmd doesn't supports inside container ,can be said as true but program behind the scene works inside the docker that is "/usr/sbin/httpd" works fine  innside docker.But we also required to delelte file created every time we run this cmd as it not start service if that file exist .You can go for "rm -rf /var/run/httpd  {{\r\n}} /usr/sbin/httpd" inside the /root/.bashrc file as it always runs as your container starts.
                  
## Docker-container
With just one command you can download your container but firstly  you have to download a image of OS you want to work on from docker hub and then you can launch your containers.(Eg. download Centos:7 imagefrom docker-hub).

## Docker-Image
As seen above we can download image from docker-hub ,we  can also create our own image by customising our older downloaded image .eg we can create our own webserver image and further it can be used to launch 1000s of containers. 

## Project-Description 
This project is very helpful when it comes to launching complete infrastructure as it can launch the same with just one click .We can use this project for solving different types of usecases ,we can launch wordpress site with database or our own cloud with database and for several other similar hosting.I would like to let you know prequisite if you want to run the same code in your laptop:

### Docker-Compose install:
I am using Docker-compose to create this project so you have to first download it .For this just go internet ,find docker-compose download > First link > linux > copy both the links in your OS and you are ready to use your docker-compose.Now make a workspace for better management of code .Inside workspace you can download this file which is ready to use .                                 

### Code description:
Our data is permanent as we have mounted our data to docker-host.It will download image from internet itself so we may require internet .
