# Hector Barrios

FROM ubuntu:20.04

MAINTAINER hdbarrios@gmail.com
LABEL maintainer="hdbarrios@gmail.com"

ARG DEBIAN_FRONTEND=noninteractive

RUN apt-get update
RUN apt-get install -y apache2 curl 

RUN a2enmod proxy
RUN a2enmod proxy_http
RUN a2enmod proxy_balancer
RUN a2enmod lbmethod_byrequests

RUN mkdir -p /var/same/mysites/first \
             /var/same/mysites/second \
             /var/same/mysites/third

COPY ./apache2/sites-available /etc/apache2/sites-available/
COPY ./apache2/conf/ /etc/apache2

COPY ./mysite /var/same/mysite

WORKDIR /etc/apache2/sites-enabled

RUN ln -s ../sites-available/first.conf first.conf
RUN ln -s ../sites-available/second.conf second.conf
RUN ln -s ../sites-available/third.conf third.conf

WORKDIR /etc/apache2/

EXPOSE 8080 8081 8082 8083

CMD ["apachectl", "-D", "FOREGROUND"]
