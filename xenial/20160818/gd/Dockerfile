FROM dockerkit/laravel-cli:xenial-20160818

RUN export DEBIAN_FRONTEND=noninteractive \
    && apt-get update \
    && apt-get install --no-install-recommends -yq \
       php-gd \
    && phpenmod \
       gd \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

