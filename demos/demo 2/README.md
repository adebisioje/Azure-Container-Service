# Demo 2  Build Container 

#Requirement
Docker must be installed and running. See [instructions](https://github.com/adebisioje/Azure-Container-Service/tree/master/demos) here. 

#Step 1 - Create Directory structure 
From your root directory, create a directory with the following structure:

    web/www/html

#Step 2 
Under the web folder create a file named Dockerfile that contains the following:

    FROM php:5.6-apache

    COPY ./www /var/www/
    
This file is also found here

#Step 3 
Create a simple index.php file under web/www/html
use the file located [here](https://github.com/adebisioje/Azure-Container-Service/tree/master/demos/demo%202/web/www/html)

#Step 4
Under the web folder, build the application 

    docker build -t web web
    
#Step 5 
Run the application

    docker run -d -v $(pwd)/www/:/var/www -p $80:80 --name=dev_web web:latest

#Step 6 
To see your application running, run the following command 

    docker ps -a

#Step 7
To view your web application in a web broweser, go to localhost/[THE PORT YOU SEE FROM STEP 6]. 

#Step 8 
Clean up 

    docker rm -f $(docker ps -qa)





