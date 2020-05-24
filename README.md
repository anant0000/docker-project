# Docker-project

## Introduction
               Docker is a containersation tool helps us setup different types of environments depending upon requirement.It was launched in 2013 by Solomon Hykes and made a revolutionary changes inn industry as it works on O.S level virtualisation.
                
##Preinstallation setup
                       We are using Rhel 8 as docker-host and docker will be sharing Kernel and some libraries from this host only.You can go for other docker-host too as per your choice.
                  
 ##Install
          For Professionals there is licence available to download but for student we have a trick

##Docker-service
               This is one of the things where new learners stucks because of not having deep-dive knowledge of basic command.In our case the command is systemctl command .Many says that this cmd doesn't supports inside container ,can be said as true but program behind the scene works inside the docker that is "/usr/sbin/httpd" works fine  innside docker.But we also required to delelte file created every time we run this cmd as it not start service if that file exist .You can go for "rm -rf /var/run/httpd  {{\r\n}} /usr/sbin/httpd" inside the /root/.bashrc file as it always runs as your container starts.
                  
##Docker Volume
               There is  a big myth that data inside container is not permanent .It is true only if you do not have core Docker knowledge .We have to mount some directory from our docker-host to make our data permanent.We can do this by :
                 ""Docker run -it -v /mydockerhostvolume:/var/www/html
                 
 ##Docker Network
                   Most secure  OS is that which is completely isolated  from outside world but 
¥ It will launch multi-tier infrastructure for you in which Jhoomla is using Mysql database.

-What happen to your data if your container fail? 
¥Our data is Persistent Permanent so we can launch our new architecture with just one click without losing any data. 


-What else you can do with similar file
¥ We can launch our WordPress site with mysql database

