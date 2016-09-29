# Demo 2  Build Container 

#Requirement
Docker must be installed and running. See [instructions](https://github.com/adebisioje/Azure-Container-Service/tree/master/demos) here. 

#Step 1 - Create Directory structure 
From your root directory, create a directory with the following structure:

    web/www/html

#Step 2 - Under the web folder create a file named Dockerfile that contains the following:

    FROM php:5.6-apache

    COPY ./www /var/www/







