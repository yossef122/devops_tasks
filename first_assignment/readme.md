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
