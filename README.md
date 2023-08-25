## Laravel Docker  

**How to install and Run this Project**

- Docker (Docker version 20.10.7, build 20.10.7-0ubuntu1~18.04.2)
- Docker-compose (docker-compose version 1.29.2, build 5becea4c)

**After installing above tools, you need to run below command to start this project.**

`docker build .`
`docker-compose up`

**Add .ENV file for DB Settings**

```
DB_CONNECTION=mysql
DB_HOST=user_db
DB_PORT=3306
DB_DATABASE=laravel-docker
DB_USERNAME=root
DB_PASSWORD=root
```

**Below are the URLs to access this project and database.**

Frontend URL: http://localhost:9000

Database URL: http://localhost:9001

Server : mysql_db

Database username: root

Password: root

Docker Documentation
---------------------

STEP 1 : Build Container image

C:\xampp\htdocs\laravel-docker>docker-compose build

STEP 2 :  Run the docker Container

C:\xampp\htdocs\laravel-docker>docker-compose up

STEP 3 : Laravel Document root connect in command line

C:\xampp\htdocs\laravel-docker>docker exec -it laravel-docker bash

STEP 4 : Install the laravel project 

    root@b51ae2a37cba:/var/www/html#composer create-project laravel/laravel . 

STEP 5 : Below commands are excuted after instatll the project

    var/www/html# php artisan key:generate
    var/www/html# php artisan storage:link
    var/www/html# chmod -R 777 storage bootstrap/cache
    var/www/html# php artisan migrate

STEP 6 : Mysql connection in command line

    var/www/html#  mysql -u root -p 