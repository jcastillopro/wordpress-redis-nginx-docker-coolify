FROM wordpress:php8.0-fpm

COPY ./wordpress.ini /usr/local/etc/php/conf.d/wordpress.ini
RUN apt install php-dev
RUN pecl install redis