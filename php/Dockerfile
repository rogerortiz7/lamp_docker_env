FROM php:7.3.3-apache
RUN apt-get update && apt-get upgrade -y
RUN apt-get update && \
     apt-get install -y \
        libzip-dev \
         && docker-php-ext-install zip
RUN a2enmod rewrite 
RUN docker-php-ext-install mysqli
RUN docker-php-ext-install pdo pdo_mysql
EXPOSE 80