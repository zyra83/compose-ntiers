FROM php:7.0-apache
RUN  apt-get update -y && apt-get install libpq-dev -y
RUN docker-php-ext-install pdo pdo_mysql pdo_pgsql && a2enmod rewrite
