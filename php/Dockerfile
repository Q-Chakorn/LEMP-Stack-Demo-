FROM php:7.4-fpm-alpine

MAINTAINER chakornotaku@gmail.com
#update 
RUN apt-get update && apt-get dist-upgrade -y \
    && rm -rf /var/lib/apt/lists/*

COPY . /apps/
WORKDIR /apps/
RUN docker-php-ext-install mysqli