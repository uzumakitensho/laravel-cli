FROM centos

RUN yum check-update \
    && yum install https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm -y --nogpgcheck \
    && yum install http://rpms.remirepo.net/enterprise/remi-release-7.rpm -y --nogpgcheck \
    && yum install yum-utils -y --nogpgcheck \
    && yum-config-manager --enable remi-php70 \
    && yum install -y --nogpgcheck php php-mcrypt \ 
      php-cli \
      php-gd \
      php-curl \
      php-mysql \
      php-ldap \
      php-zip \
      php-fileinfo \
      php-intl \
      php-json \
      php-mysqlnd \
      php-pgsql \
      php-readline \
      php-sqlite \
      php-xsl \
      php-iconv \
      vim \
      git \
    && yum clean packages \
    && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

RUN yum update \
    && curl --silent --location https://rpm.nodesource.com/setup_8.x | bash - \
    && yum install --nogpgcheck -y \
       nodejs \
       g++ \
       python \
       make \
    && yum clean packages \
    && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

RUN curl -sL https://getcomposer.org/download/1.6.3/composer.phar -o /usr/local/bin/composer.phar \
    && chmod a+x /usr/local/bin/composer.phar \
    && ln -s /usr/local/bin/composer.phar /usr/local/bin/composer