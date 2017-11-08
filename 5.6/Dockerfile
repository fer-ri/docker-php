FROM php:5.6-fpm-alpine

MAINTAINER Ferri Sutanto <greenhouseprod@gmail.com>

RUN set -x; \
    \
    docker-php-ext-install pdo_mysql; \
    php -r "readfile('http://getcomposer.org/installer');" | \
        php -- --install-dir=/usr/local/bin/ --filename=composer; \
    mkdir -p /.composer; \
    chmod -R ugo+rw /.composer;