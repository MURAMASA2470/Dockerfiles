FROM php:8.2-fpm as base

RUN cd /usr/bin && curl -s http://getcomposer.org/installer | php && ln -s /usr/bin/composer.phar /usr/bin/composer
RUN apt-get update \
    && apt-get install -y \
       git \
       zip \
       unzip \
       vim \
       curl \
       libzip-dev \
       libpng-dev \
       libjpeg-dev \
       libgif-dev \
       iputils-ping \
       libfreetype6-dev \
       net-tools \
       npm \
       libonig-dev \
       sendmail
RUN docker-php-ext-install pdo_mysql bcmath opcache
RUN docker-php-ext-configure gd --with-freetype=/usr/include/ --with-jpeg=/usr/include/
RUN docker-php-ext-install -j$(nproc) gd
RUN docker-php-ext-install zip
