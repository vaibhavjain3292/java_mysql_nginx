FROM ubuntu:14.04

LABEL Description="This is my test image for java project"

MAINTAINER Vaibhav Jain

RUN apt-get update

RUN apt-get install -y --no-install-recommends openjdk-7-jdk
RUN apt-get install -y maven
RUN sudo apt-get install -y tomcat7
 
ENV CATALINA_HOME /usr/share/tomcat7/
ENV CATALINA_BASE /var/lib/tomcat7/
ENV PATH $CATALINA_HOME/bin:$PATH

RUN apt-get install -y wget

COPY ./target/*.war /var/lib/tomcat7/webapps/application.war 

EXPOSE 8080
 
CMD ["catalina.sh", "run"]

