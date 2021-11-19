FROM php:8-fpm-alpine

ADD ./www.conf /usr/local/etc/php-fpm.d/www.conf

RUN docker-php-ext-install pdo pdo_mysql

RUN addgroup -g 1000 web && adduser -G web -g web -s /bin/sh -D web

RUN mkdir /app

RUN chown -R web:web /app

USER web
