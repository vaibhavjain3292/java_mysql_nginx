### Containarized Java Application with Nginx as Lad balancer and My sql as database

## Tools and Technology used : 

* Java
* Nginx
* MySQL
* Docker
* Docker compose

## Folder Structure :
* JavaApplication : Source code for application along with Dockerfile 
* mysql : Shell Scripts and Dockerfile
* Nginx : Dockerfile and configuration file for nginx

## Prerequisite
1. Linux machine
2. Docker 1.10 or above
3. Docker compose 1.6 or above

## Steps to Run

1. Clone this repository.
2. move inside the root of the repository
3. Run docker-compose up -d

After this point check is all the docker containers are running properly by using 
* docker ps command

## Conclusion 
After this point you will observe 4 docker containers are running on the host machine each container bind with a host port.
1. 2 containers of java application each bind to 8081 and 8082 port.
2. mysql container bind with 3306 port.
3. nginx container bind with 85 port.

For accessessing the application:
1. Hit load balancer or (<machineIP or localhost:85>)
2. Hit application directly.(<machineIP or localhost:8081 or localhost:8082>)

* For all the configuration refer docker-cmpose.yml file.
