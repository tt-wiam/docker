FROM php:8.2-fpm as ap_php
WORKDIR /var/www

COPY ./php.ini /usr/local/etc/php/
COPY ./conf.d /usr/local/etc/php/conf.d

RUN apt-get update
RUN apt-get install -y curl git zip libpq-dev
RUN docker-php-ext-install pdo pdo_pgsql pgsql opcache

RUN \
    cd /tmp \
    && curl -sS https://getcomposer.org/installer | php \
    && mv composer.phar /usr/local/bin/composer

#xDebug
RUN \
    pecl install xdebug \
    && docker-php-ext-enable xdebug

#Add www-data to sudo group
RUN usermod -aG sudo www-data
ENV USER_NAME www-data
RUN usermod -u 1000 www-data

