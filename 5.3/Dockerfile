FROM ubuntu:12.04

ENV DEBIAN_FRONTEND noninteractive

RUN apt-get update && apt-get upgrade -y

RUN apt-get install -y php5-fpm php5-memcache php5-mysql

RUN sed -i -e 's/^;daemonize .*/daemonize = no/' /etc/php5/fpm/php-fpm.conf
RUN sed -i -e 's/^listen \= .*/listen = 0.0.0.0:9000/' /etc/php5/fpm/pool.d/www.conf

EXPOSE 9000

ENTRYPOINT [ "/usr/sbin/php5-fpm", "-y", "/etc/php5/fpm/php-fpm.conf" ]
