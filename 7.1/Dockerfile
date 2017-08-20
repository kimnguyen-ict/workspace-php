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
        php7.0-cli \
        php7.0-common \
        php7.0-curl \
        php7.0-dev \
        php7.0-gd \
        php7.0-gmp \
        php7.0-json \
        php7.0-ldap \
        php7.0-mysql \
        php7.0-odbc \
        php7.0-opcache \
        php7.0-pgsql \
        php7.0-pspell \
        php7.0-readline \
        php7.0-recode \
        php7.0-snmp \
        php7.0-sqlite3 \
        php7.0-tidy \
        php7.0-xml \
        php7.0-xmlrpc \
        php7.0-bcmath \
        php7.0-bz2 \
        php7.0-enchant \
        php7.0-fpm \
        php7.0-imap \
        php7.0-interbase \
        php7.0-intl \
        php7.0-mbstring \
        php7.0-mcrypt \
        php7.0-phpdbg \
        php7.0-soap \
        php7.0-sybase \
        php7.0-xsl \
        php7.0-zip \
        php7.0-dba \
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
