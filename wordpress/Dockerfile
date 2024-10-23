FROM wordpress:php8.0-fpm

COPY ./wordpress.ini /usr/local/etc/php/conf.d/wordpress.ini
RUN apt-get update && apt-get install -y apt-transport-https
RUN apt-get update && apt-get install php8.0-dev
RUN pecl install redis