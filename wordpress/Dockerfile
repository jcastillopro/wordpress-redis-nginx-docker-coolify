FROM wordpress:php8.0-fpm-alpine

COPY ./wordpress.ini /usr/local/etc/php/conf.d/wordpress.ini
RUN composer require predis/predis