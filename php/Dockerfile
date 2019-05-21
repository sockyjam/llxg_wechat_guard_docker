
FROM php:7.0-fpm

MAINTAINER SockyJam<sockyjam@126.com>


RUN apt-get update -y \
    && apt-get install -y curl \
                          git \
                          libfreetype6-dev \
                          libjpeg62-turbo-dev \
                          libmcrypt-dev \
                          libpng-dev \
    && docker-php-ext-install -j$(nproc) iconv mcrypt pdo_mysql \
    && docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/ \
    && docker-php-ext-install -j$(nproc) gd \
    && pecl install mongodb \
    && docker-php-ext-enable mongodb \
    && echo "extension=mongodb.so" >> /usr/local/etc/php/conf.d/mongodb.ini





