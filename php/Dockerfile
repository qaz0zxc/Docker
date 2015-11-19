FROM php:5.6-fpm
ADD ./php-fpm.conf /usr/local/etc/php-fpm.conf

RUN mkdir -p /home/extension
COPY ./extension/mongodb.tgz /home/extension/mongodb.tgz
COPY ./extension/redis.tgz  /home/extension/redis.tgz
# RUN docker-php-ext-install gd \
#     && docker-php-ext-install pdo_mysql \
#     && pecl install /home/extension/redis.tgz && /home/extension/mongodb.tgz && echo "extension=redis.so" > /usr/local/etc/php/conf.d/redis.ini && echo "extension=mongo.so" /usr/local/etc/php/conf.d/mongo.ini
ADD ./composer.phar /usr/local/bin/composer
RUN chmod 755 /usr/local/bin/composer

RUN mkdir /code
WORKDIR /code
RUN usermod -u 1000 www-data
