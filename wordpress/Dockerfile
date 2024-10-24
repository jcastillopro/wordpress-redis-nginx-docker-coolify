FROM wordpress:php8.1-fpm

COPY ./php.ini /usr/local/etc/php/conf.d/php.ini

# install redis
RUN apt-get install lsb-release curl gpg &&\
curl -fsSL https://packages.redis.io/gpg | gpg --dearmor -o /usr/share/keyrings/redis-archive-keyring.gpg &&\
chmod 644 /usr/share/keyrings/redis-archive-keyring.gpg &&\
echo "deb [signed-by=/usr/share/keyrings/redis-archive-keyring.gpg] https://packages.redis.io/deb $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/redis.list &&\
apt-get update &&\
apt-get install redis

COPY ./redis.conf /usr/local/etc/redis/redis.conf

RUN sysctl vm.overcommit_memory=1

RUN systemctl enable redis-server &&\
redis-server /usr/local/etc/redis/redis.conf --save 60 1 --loglevel warning --maxmemory 128mb --maxmemory-policy allkeys-lru