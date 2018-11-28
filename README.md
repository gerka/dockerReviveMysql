# dockerReviveMysql
Docker Container with actual version of revive Ad server php7,nginx and mysql

## Introduction
This is a simple project to up  the Revive AdServer quickly using docker.

## Folder Structure
- **docker/** - Contains the same files based on docker-compose syntax to config how docker will execute the containers
- **mysql/** - Initially, it Is a empty folder that is mapped to the mysql container, when the mysql container is running it will write the files within this folder, so you do not lose the data when the container is removed
- **server/** - Contains a configuration file for nginx, this file is mapped to docker container to be read to nginx

## Requirements  
- **docker** (https://docs.docker.com/engine/installation/linux/debian/)  
- **docker-compose** (https://docs.docker.com/compose/install/)  

## Instalation
**1ª Step:** Clone this project and access the project folder  
`git clone git@github.com:gerka/dockerReviveMysql.git`  
`cd dockerReviveMysql`     

**2ª Step:** Run docker stack  
`docker-compose up -d`

**3ª Step:** Get the MySql IP from container  
`docker inspect --format '{{ .NetworkSettings.IPAddress }}' mysql`

**4ª Step:** Access 'locahost:48654' on browser. Now should appear a screen with the **Revive** terms

**5ª Step:** Accept the terms. Now should display the database connection setup

**6ª Step:** Fill de fields with database credentials. Example:  
- **Database Name:** (You choose a name)  
- **username:** root  
- **password:** root  
- **hostname:** (It is the IP that you get on **3ª Step**)  

**7ª Step:** Enjoy
