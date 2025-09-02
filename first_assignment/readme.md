first tasks 
install nginx

install php >> nginx>> 2 ways

(socket && Port)

spring pet clinic run wsl

docker file >> multisatge

docker compose app connected db my sql &Postgres


first task 
1- install nginx => sudo apt install nginx
2- install php => sudo apt install php
3- verify the install nginx -v && php -v
4- edit the file of www.conf of fpm of php
5- connect the php of nginx by port 
6- i make the ip  192.168.1.101 as i change the vm port
 
we need to put the files of servers on conf.d
and make the socket for it 
to make it change the lines             fastcgi_pass 192.168.1.101:8000;
to fastcgi_pass nuix:/run/php/php8.4-fp.sock;



second task
1- get the repo from [text](https://github.com/orgs/spring-petclinic/repositories)


3- try to run the repo by the command in the readme file of repo => ./mvnw spring-boot:run

4- install npm to run the side client server => npm install

5- run the server using ./mvnw spring-boot:run

6- start the docker file

7- make the normal docker file and staging file

8- build the docker file by docker build -t spring-petclinic .

9- run the container docker run --name sprint-pet -p 8070:8080 -d spring-petclinic 

test the running on localhost:8070 using website



second make the compose 

start search for the version of mysql and postgress 

then i found the version is mysql:9.2 and postgres:17.5

and add the enviroment variable of mysql and postgree 

and change the name of conatiner 
and make conatiner of spring-petclinic and make it depends on the db which is made in the same file of 
and the test the website with localhost:8081




docker run -e MYSQL_URL=jdbc:mysql://spring_mysql_manual:3306/petclinic -e SPRING_PROFILES_ACTIVE=mysql --network spring-net --name spring_app_manual -p 3010:8080 spring_petclinic_eclipse

docker run -e MYSQL_USER=petclinic -e MYSQL_PASSWORD=petclinic -e MYSQL_ROOT_PASSWORD=root -e MYSQL_DATABASE=petclinic --network spring-net --name spring_mysql_manual -v mysql_manual-volume:/var/lib/mysql -p 3009:3306 mysql