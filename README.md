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

#### Version
There are several version of docker-compose so we have to tell which version we are using.

#### Service:
We are launching containers technically they are known as service so we are using resp. keyword.

#### Enviromental variables 
At the time of launching container from mysql image we have to provide some environmental variables ,these are listed after "enviroment" keyword 
#### Volume
We want our data to be permanent so we we have mounted a directory from docker-host.We are creating the volume in our Docker-host by "Volume" at last .

#### Link
We are linking databasse OS to store our data there by keyword "Link".

#### Port 
Like every server this server will also run on some port .We can run it on any free port upto 65536 . I am running it on port 8085.

### How to run this code :
Go to your workspace where you have downloaded this code ,file should be named as docker-compose.yml only and can be run by  docker-compose up command you can check your infrastructure by following ways:
1)Run docker ps -a command in your docker-host or 
2)Go to browser type your IP:PORT.No. you will get your Jhoomla site 

### How to stop your Infrastructure:
You can do so by doing R.ctrl+C on your Docker-host

## For any help feel free to DM me on my LinkedIn profile 

## I would like to thanks Mr. Vimal Daga Sir for his wonderful guidance and to teach several other importance core concepts of docker in his training.
