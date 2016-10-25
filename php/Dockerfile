FROM bradallenfisher/centos7
MAINTAINER Brad Allen Fisher, bradallenfisher@gmail.com

RUN yum update

# Install Remi Collet's repo for CentOS 7
RUN yum -y install \
  http://rpms.famillecollet.com/enterprise/remi-release-7.rpm \
  http://www.percona.com/downloads/percona-release/percona-release-0.0-1.x86_64.rpm

# Install PHP and Percona (MySQL) client stuff and the latest stable PHP.
RUN yum -y install --enablerepo=remi,remi-php56 \
  Percona-Server-client-56 \
  php-cli \
  php-fpm \
  php-gd \
  php-mbstring \
  php-mcrypt \
  php-mysqlnd \
  php-opcache \
  php-pdo \
  php-pear \
  php-soap \
  php-xml \
  php-pecl-imagick \
  php-pecl-apcu

RUN rm -r /var/www/html/*

RUN mkdir -p /var/log/supervisor

EXPOSE 80
