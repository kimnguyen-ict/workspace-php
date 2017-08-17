FROM ubuntu:16.04

MAINTAINER Nguyen Huu Kim <kimnguyen.ict@gmail.com>

RUN apt-get update \
  && apt-get install -y software-properties-common locales

RUN locale-gen en_US.UTF-8

ENV LANGUAGE=en_US.UTF-8
ENV LC_ALL=en_US.UTF-8
ENV LC_CTYPE=UTF-8
ENV LANG=en_US.UTF-8
ENV TERM xterm

RUN add-apt-repository ppa:ondrej/php \
  && apt-get update \
  && apt-get install -y php7.1 --force-yes

RUN apt-get install -y --force-yes \
  	php7.1-cli \
  	php7.1-common \
        php7.1-curl \
        php7.1-json \
        php7.1-xml \
        php7.1-mbstring \
        php7.1-mcrypt \
        php7.1-mysql \
        php7.1-pgsql \
        php7.1-sqlite \
        php7.1-sqlite3 \
        php7.1-zip \
        php7.1-memcached \
        php7.1-gd \
        php7.1-fpm \
        php7.1-xdebug \
        php7.1-bcmath \
        php7.1-intl \
        libcurl4-openssl-dev \
        libedit-dev \
        libssl-dev \
        libxml2-dev \
        xz-utils \
        sqlite3 \
        libsqlite3-dev \
        git \
        curl \
        vim \
        nano \
        net-tools \
        pkg-config \
        iputils-ping

RUN curl -s http://getcomposer.org/installer | php \
  && mv composer.phar /usr/local/bin/composer

RUN echo "export PATH=${PATH}:/var/www/workspace/vendor/bin:/root/.composer/vendor/bin" >> ~/.bashrc

RUN curl -sL https://deb.nodesource.com/setup_7.x | bash - \
    && apt-get install -y nodejs \
    && npm install -g yarn gulp-cli

WORKDIR /var/www/workspace
