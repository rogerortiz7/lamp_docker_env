FROM php:7.4-apache
RUN apt-get update && apt-get upgrade -y
RUN apt-get update && \
   apt-get install -y \
   libzip-dev \
   && docker-php-ext-install zip

#VIM
RUN apt install -y vim 

#COMPOSER 
RUN curl -sS https://getcomposer.org/installer | php
RUN mv composer.phar /usr/local/bin/composer

#PHPUNIT
RUN composer global require "phpunit/phpunit"

ENV PATH /root/.composer/vendor/bin:$PATH

RUN ln -s /root/.composer/vendor/bin/phpunit /usr/bin/phpunit

###################
RUN a2enmod rewrite 
RUN docker-php-ext-install mysqli
RUN docker-php-ext-install pdo pdo_mysql
EXPOSE 80

