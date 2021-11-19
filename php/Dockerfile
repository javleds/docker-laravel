FROM php:8-fpm-alpine

ADD ./www.conf /usr/local/etc/php-fpm.d/www.conf

RUN mkdir -p /application

RUN docker-php-ext-install pdo pdo_mysql

RUN chown -R www-data:www-data /application

USER www-data
