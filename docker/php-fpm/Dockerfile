FROM php:8.1.27-fpm-alpine3.18

LABEL maintainer="Shayan Davarzani <shayandavarzani@gmail.com>"

RUN apk add --no-cache \
    coreutils \
    gettext \
    argon2-libs \
    libedit \
    libxml2 \
    musl \
    pcre2 \
    zlib \
    make \
    curl \
    vim

RUN apk add --no-cache \
    php81-fpm \
    php81-ctype \
    php81-curl \
    php81-dom \
    php81-gd \
    php81-iconv \
    php81-intl \
    php81-fileinfo\
    php81-mbstring \
    php81-opcache \
    php81-openssl \
    php81-pdo \
    php81-pdo_mysql \
    php81-mysqli \
    php81-xml \
    php81-xsl \
    php81-phar \
    php81-tokenizer \
    php81-session \
    php81-simplexml \
    php81-zip \
    php81-xmlwriter \
    php81-sodium 

COPY php.ini /etc/php81/conf.d/
COPY php.ini /etc/php81/cli/conf.d/

COPY php.pool.conf /etc/php81/php-fpm.d/

WORKDIR /var/www

CMD ["php-fpm81", "-F"]

EXPOSE 9000