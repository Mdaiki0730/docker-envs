FROM php:7.1-fpm

COPY ./docker/php-server/php.ini /usr/local/etc/php/
COPY ./src/laravel /var/www/laravel

COPY --from=composer:1.10.15 /usr/bin/composer /usr/bin/composer

ENV COMPOSER_ALLOW_SUPERUSER 1

ENV COMPOSER_HOME /composer

ENV PATH $PATH:/composer/vendor/bin

WORKDIR /var/www/laravel

RUN apt-get update \
  && apt-get install -y zlib1g-dev libpq-dev mariadb-client unzip npm vim git \
  && apt-get install -y libnotify-bin notify-osd \
  && docker-php-ext-install zip pdo_mysql mysqli \
  && docker-php-ext-enable mysqli \
  && npm install -g n gulp\
  && n 8.16.0 \
