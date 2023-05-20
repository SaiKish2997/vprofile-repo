## Prerequisites
- JDK 1.8 or later
- Maven 3 or later
- MySQL 5.6 or later

## Technologies 
- Spring MVC
- Spring Security
- Spring Data JPA
- Maven
- JSP
- MySQL
## Database
Here,we used Mysql DB 
MSQL DB Installation Steps for Linux ubuntu 14.04:
- $ sudo apt-get update
- $ sudo apt-get install mysql-server

Then look for the file :
- /src/main/resources/accountsdb
- accountsdb.sql file is a mysql dump file.we have to import this dump to mysql db server
- > mysql -u <user_name> -p accounts < accountsdb.sql

**For docker envirnoment clone the repo sswitch in to the vp-docker branch**
1. Build the source code 
2. switch in to the Docker-app copy the target folder in to the Docker-app and build the image
3. and switch in to the Docker-db app and build the docker image 
4. run the db container by the below command
$ docker run --name vprodb -d -e MYSQL_ROOT_PASSWORD=vprodbpass vprodb
6. run the app container by linking the db container by the below command
$ docker run --name vproapp --link vprodb:mysql -d -p 8080:8080 vproapp


