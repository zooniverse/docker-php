FROM ubuntu:14.04

ENV DEBIAN_FRONTEND noninteractive

RUN apt-get update && apt-get upgrade -y

RUN apt-get install -y php5-fpm

RUN sed -i -e 's/;daemonize .*/daemonize = no/' /etc/php5/fpm/php-fpm.conf

EXPOSE 9000

ENTRYPOINT [ "/usr/sbin/php5-fpm", "-y", "/etc/php5/fpm/php-fpm.conf" ]
