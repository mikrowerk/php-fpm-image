FROM php:7.4-fpm
LABEL maintainer="Guenther Froestl <gfr@gammadata.de>"

RUN docker-php-ext-install mysqli && docker-php-ext-enable mysqli
RUN apt-get update && apt-get install -y && \
    apt-get install -y iputils-ping procps nano default-mysql-client


COPY index.php /var/www/html/index.php

RUN ls -al /usr/local/etc/php-fpm.d/*.conf && \
cat /usr/local/etc/php-fpm.d/*.conf && \
ls -al /usr/local/etc/php/conf.d && \
cat /usr/local/etc/php/conf.d/docker-php-ext-sodium.ini && \
php /var/www/html/index.php