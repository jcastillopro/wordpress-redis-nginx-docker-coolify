FROM wordpress:php8.0-fpm

COPY ./wordpress.ini /usr/local/etc/php/conf.d/wordpress.ini
RUN git clone https://github.com/phpredis/phpredis.git &&\ 
cd phpredis &&\ 
phpize &&\ 
./configure [--enable-redis-igbinary] [--enable-redis-msgpack] [--enable-redis-lzf [--with-liblzf[=DIR]]] [--enable-redis-zstd] [--enable-redis-lz4] &&\ 
make &&\ make install