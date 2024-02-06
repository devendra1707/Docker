Docker 
--------
     Basic Command
	 --------------
 =>   docker run hello word
=> See image in Docker   
    => docker images
docker Hub we can see all images 

=> docker -v     to See the version of docker which is installed

=> docker pull [image name]   =>  to pull the image 

=> docker pull open-jdk

=> docker images
=> docker run python  => To run docker image

=> docker ps    => to see running status

=> docker ps -a   => to see all images which is available

=> docker run --env 

=> docker run -d 

=> docker run --name pythonContainer -d python or (id) 

=> docker ps   ==> To which container is running

=> docker ps -a


=> docker run --name pythonContainer1 -it -d python

=> docker ps

=> docker exec -it [CONTAINER ID] python3

=> exit() => to exit

=> docker inspect [CONTAINER ID]  => To see all details about container

=> docker run --name javaContainer -it -d openjdk => To run java 



=> docker exec -it javaContainer [COMMAND NAME]

=> /history  => to see all history


Use MySQL

=> docker pull mysql

=> docker images

=> docker run --name mysqlDb -e MYSQL_ROOT_PASSWORD=root -d mysql

=> docker ps

=> docker inspect mysqlDb => To the Details 

=>  docker exec -it mysqlDb bash

=> mysql -p


To Stop the container 

=> docker stop [container name] or [CONTAINER ID] 



=> docker ps -a   => To see all the status which time i start or stop tha container

=> docker rm [CONTAINER ID]   => To remove history also

=> docker images;

=> -d   =>> Means that it is run in the background

=> docker run --name pythonContainer1 -it -d python

=> docker ps   => to see which container is running.

to restart 

=> docker restart [container name] or [CONTAINER ID]

docker login 

docker commit => create and save container to the local system

docker push  => this command use to push or upload the image on the repository on the docker hub

docker copy => copy fily fromm a local system

docker logs => to check the docker log 

docker volume => to create docker volume

docker logout => to logout from docker hub


--------------------------------------------------------------------


docker build -t [image name which you want] .

docker run --name [any name] [container name]


Deploy Spring Boot Project Using Docker
---------------------------------------
FROM openjdk:

WORKDIR /jv/DockerJava


COPY . /jv/DockerJava/

RUN javac Test.java

CMD ["java","-jar","file_name.jar"]
EXPOSE 8080


===============
docker build -t buildboot


docker images

docker run --name bootproject -it -d buildboot

To check java version 
-----------------------------------
docker container_name java -version




Run zipkin using docker image
----------------------------------------

docker run -d -p 9411:9411 openzipkin/zipkin







