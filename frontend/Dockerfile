FROM php:8.0-apache

RUN a2enmod rewrite


WORKDIR /var/www/html

RUN docker-php-ext-install pdo pdo_mysql

RUN apt-get update && apt-get install -y git
RUN git clone https://github.com/michelnyobe/frontend_debops.git


RUN mv frontend_debops/*  /var/www/html/

USER www-data

EXPOSE 80

CMD ["apache2-foreground"]
