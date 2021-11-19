FROM php:8-fpm-alpine

ADD ./www.conf /usr/local/etc/php-fpm.d/www.conf

RUN docker-php-ext-install pdo pdo_mysql

RUN addgroup -g 1000 laravel && adduser -G laravel -g laravel -s /bin/sh -D laravel

RUN mkdir /application

RUN chown -R laravel:laravel /application

USER laravel
