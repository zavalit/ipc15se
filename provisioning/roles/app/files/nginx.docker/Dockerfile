FROM ubuntu:14.04

MAINTAINER Seva Dolgopolov <zavalit@gmail.com>

ENV LAST_UPDATE 2015-06-07

RUN apt-get update
RUN apt-get install -y nginx

ADD api.conf /etc/nginx/sites-available/
RUN rm /etc/nginx/sites-enabled/default &&  ln -s /etc/nginx/sites-available/api.conf /etc/nginx/sites-enabled


EXPOSE 80

ENTRYPOINT ["nginx", "-g", "daemon off;"]
