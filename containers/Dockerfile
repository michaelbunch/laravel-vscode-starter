FROM abiosoft/caddy:1.0.3-php

# Install Redis Support
RUN apk add --no-cache php7-pecl-redis

# Install Xdebug
RUN apk add --no-cache php7-pecl-xdebug \
    && echo "zend_extension=xdebug.so" >> /etc/php7/conf.d/xdebug.ini \
    && echo "error_reporting=E_ALL" >> /etc/php7/conf.d/xdebug.ini \
    && echo "display_startup_errors=On" >> /etc/php7/conf.d/xdebug.ini \
    && echo "display_errors=On" >> /etc/php7/conf.d/xdebug.ini \
    && echo "xdebug.remote_enable=on" >> /etc/php7/conf.d/xdebug.ini \
    && echo "xdebug.remote_autostart=on" >> /etc/php7/conf.d/xdebug.ini \
    && echo "xdebug.remote_port=9001" >> /etc/php7/conf.d/xdebug.ini

# Install Node.js
RUN apk add --no-cache nodejs-current npm

COPY containers/Caddyfile /etc/Caddyfile
