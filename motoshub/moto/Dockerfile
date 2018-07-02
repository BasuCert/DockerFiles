FROM php:7.2.1-apache

LABEL maintainer "lopqto <morpix@protonmail.com>"

RUN a2enmod rewrite
RUN apt-get update && apt-get install -y \
		libfreetype6-dev \
		libjpeg62-turbo-dev \
		libmcrypt-dev \
		libpng-dev \
                zlib1g-dev \
                unzip \
                wget
RUN docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/ 
RUN docker-php-ext-install pdo pdo_mysql mysqli zip gd
RUN wget http://repo.shub.ir/core/main/10880/ms-core-10880.zip -O /tmp/ms-core.zip && unzip /tmp/ms-core.zip -d /var/www/html && chown -R www-data:www-data /var/www/html

