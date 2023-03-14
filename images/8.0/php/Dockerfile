FROM wordpressdevelop/php:8.0-fpm

# install the package that will collect data
WORKDIR /var/xhgui
RUN composer require perftools/php-profiler

#Install XHProf:
RUN if [ -z "$(pecl list | grep xhprof)" ] ; then pecl install xhprof ; fi
RUN docker-php-ext-enable xhprof
RUN echo '[xhprof]' >> /usr/local/etc/php/php.ini
RUN echo 'extension=xhprof.so' >> /usr/local/etc/php/php.ini
RUN echo 'xhprof.output_dir="/tmp/xhprof"' >> /usr/local/etc/php/php.ini
