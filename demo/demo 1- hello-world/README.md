#Objectives 
1. Show how fast containers can be started and stopped
2. Learn basic commadns for managing containers

#Environment

* Linux client (could be Windows)
* Docker host installed on this machine

#Step 1 
Run the following command:

     docker run hello-world
     docker ps -a

You should have the hello world process running: 

     CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS                     PORTS               NAMES
     8b5078f768f9        hello-world         "/hello"            3 seconds ago       Exited (0) 2 seconds ago                       modest_hugle


#Step 2
Get hello world application from tutum 

     docker run -d -p 80:80 tutum/hello-world

#Step 3
You should be able to see the tutum web application once you go to your browser and type the hostname  or ip address:

      http://YOUR_HOST

#Step 4
Clean up 

     docker rm -f $(docker ps -qa)




