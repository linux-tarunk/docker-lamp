FROM ubuntu:trusty
MAINTAINER Tarun Kumawat <linux.tarunk@gmail.com>

ENV DEBIAN_FRONTEND noninteractive
RUN apt-get update
RUN apt-get install -y apache2 git

RUN mkdir -p /app && rm -fr /var/www/html 
ADD app /app
RUN ln -s /app /var/www/html
RUN echo "ServerName localhost" >> /etc/apache2/apache2.conf

EXPOSE 80
RUN /etc/init.d/apache2 start 
