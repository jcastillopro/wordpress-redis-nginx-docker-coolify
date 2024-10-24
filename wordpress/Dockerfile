FROM urre/wordpress-nginx-docker-compose-image:1.4.0

# copy php.ini config for wp
COPY ./php.ini /usr/local/etc/php/conf.d/php.ini

# Install wp-cli
RUN apt-get update && apt-get install -y sudo less mariadb-client
RUN curl -o /bin/wp-cli.phar https://raw.githubusercontent.com/wp-cli/builds/gh-pages/phar/wp-cli.phar
RUN chmod +x /bin/wp-cli.phar
RUN cd /bin && mv wp-cli.phar wp
RUN mkdir -p /var/www/.wp-cli/cache && chown www-data:www-data /var/www/.wp-cli/cache

# Note: Use docker-compose up -d --force-recreate --build when Dockerfile has changed.