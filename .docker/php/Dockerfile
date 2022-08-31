FROM php:8.1.0-fpm

LABEL maintainer="contact@legrandjeremie.fr"

RUN apt-get update && apt-get install -y \
        apt-utils \
        default-libmysqlclient-dev \
        default-mysql-client

ADD https://github.com/mlocati/docker-php-extension-installer/releases/latest/download/install-php-extensions /usr/local/bin/

RUN chmod +x /usr/local/bin/install-php-extensions && sync && \
    install-php-extensions apcu bz2 dba \
    decimal excimer gd gettext \
    gmagick igbinary imap intl memcache \
    memcached mysqli oauth opcache \
    pdo_mysql redis snmp \
    tidy xdebug xlswriter xmldiff xsl zip

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

WORKDIR /var/www/app

EXPOSE 9000
CMD ["php-fpm"]