FROM php:7.1-fpm

RUN docker-php-ext-install mysqli
RUN curl -o /usr/local/bin/wp https://raw.githubusercontent.com/wp-cli/builds/gh-pages/phar/wp-cli.phar && \
        chmod +x /usr/local/bin/wp
