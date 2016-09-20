FROM dockerkit/ubuntu:xenial-20160818

RUN export DEBIAN_FRONTEND=noninteractive \
    && apt-get update \
    && apt-get install --no-install-recommends -yq \
       curl \
       ca-certificates \
    && apt-get install --no-install-recommends -yq \
       vim \
       git \
       php-cli \
       php-curl \
       php-intl \
       php-json \
       php-mbstring \
       php-mcrypt \
       php-mysql \
       php-pgsql \
       php-readline \
       php-sqlite3 \
       php-xml \
       php-zip \
    && phpenmod \
       curl \
       intl \
       json \
       mbstring \
       mcrypt \
       mysql \
       pgsql \
       readline \
       sqlite3 \
       xml \
       zip \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

RUN export DEBIAN_FRONTEND=noninteractive \
    && apt-get update \
    && curl -sL https://deb.nodesource.com/setup_6.x | bash - \
    && apt-get install --no-install-recommends -yq \
       nodejs \
       g++ \
       python \
       make \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

RUN npm install --global npm \
    && npm install --global gulp \
    && npm cache clean

RUN curl -sL https://getcomposer.org/download/1.2.0/composer.phar -o /usr/local/bin/composer.phar \
    && chmod a+x /usr/local/bin/composer.phar \
    && ln -s /usr/local/bin/composer.phar /usr/local/bin/composer

