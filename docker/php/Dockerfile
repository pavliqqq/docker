FROM php:8.2-fpm

RUN apt-get update && apt-get upgrade -y && \
    apt-get install -y unzip zip git curl libzip-dev libicu-dev \
    libfreetype6-dev libjpeg62-turbo-dev libpng-dev libonig-dev && \
    docker-php-ext-configure gd --with-freetype --with-jpeg && \
    docker-php-ext-install pdo pdo_mysql gd intl mbstring && \
    docker-php-ext-enable pdo_mysql && \
    pecl install redis xdebug-3.2.0 && \
    docker-php-ext-enable redis xdebug


ENV COMPOSER_ALLOW_SUPERUSER=1
RUN curl -sS https://getcomposer.org/installer | php -- \
    --filename=composer \
    --install-dir=/usr/local/bin

COPY docker/php/conf.d/* $PHP_INI_DIR/conf.d/

WORKDIR /var/www
