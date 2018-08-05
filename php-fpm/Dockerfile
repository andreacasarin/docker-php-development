FROM php:7.1-fpm

RUN docker-php-ext-install mysqli

RUN yes | pecl install xdebug
RUN echo "zend_extension=$(find /usr/local/lib/php/extensions/ -name xdebug.so)" > /usr/local/etc/php/conf.d/xdebug.ini
RUN echo "xdebug.remote_enable=1" >> /usr/local/etc/php/conf.d/xdebug.ini
RUN echo "xdebug.remote_autostart=0" >> /usr/local/etc/php/conf.d/xdebug.ini

WORKDIR /var/www/app

CMD php-fpm -F
