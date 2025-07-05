FROM php:8.2-fpm

RUN apt-get update && apt-get upgrade -y && \
    apt-get install -y unzip zip git curl libzip-dev && \
    docker-php-ext-install pdo pdo_mysql && \
    docker-php-ext-enable pdo_mysql && \
    pecl install xdebug-3.2.0 && \
    docker-php-ext-enable xdebug


ENV COMPOSER_ALLOW_SUPERUSER=1
RUN curl -sS https://getcomposer.org/installer | php -- \
    --filename=composer \
    --install-dir=/usr/local/bin

COPY docker/php/conf.d/* $PHP_INI_DIR/conf.d/

WORKDIR /var/www
