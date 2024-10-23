FROM wordpress:php8.0-fpm

COPY ./wordpress.ini /usr/local/etc/php/conf.d/wordpress.ini
RUN apt-get update && apt-get install -y apt-transport-https
RUN apt-get update && apt-get install -y php8.0-cli php8.0-common php8.0-mysql php8.0-zip php8.0-gd php8.0-mbstring php8.0-curl php8.0-xml php8.0-bcmath
RUN pecl install redis