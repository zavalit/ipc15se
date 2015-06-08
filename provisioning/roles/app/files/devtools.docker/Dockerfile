FROM zavalit/php-7

ENV LAST_UPDATE 07-06-2015


# install composer
RUN mkdir /opt/devtools && curl -sS https://getcomposer.org/installer | php -- --install-dir=/opt/devtools

WORKDIR /opt/devtools

#install phpunit
RUN ./composer.phar require "phpunit/phpunit=4.7.*" && ln -s vendor/bin/phpunit phpunit

ENV COMPOSER /opt/devtools/composer.phar
ENV PHPUNIT  /opt/devtools/phpunit

# share it with others
VOLUME ["/opt/devtools"]

# start php dev server
ENTRYPOINT ["php", "-S"]

CMD ["localhost:8000"]