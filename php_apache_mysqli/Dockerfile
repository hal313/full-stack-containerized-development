FROM php:7.2.2-apache

## Enable the "mysqli"
RUN docker-php-ext-install mysqli && docker-php-ext-enable mysqli && apachectl restart
