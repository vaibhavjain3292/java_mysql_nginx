
#link : https://hub.docker.com/_/nginx/
# base image
FROM nginx:latest

MAINTAINER vaibhav jain

# Removing exixting configuration
RUN rm -f /etc/nginx/nginx.conf

#Adding the new configurtion file
ADD nginx.conf /etc/nginx/nginx.conf

# Start the nginx loadbalancer
RUN service nginx restart

EXPOSE 80
