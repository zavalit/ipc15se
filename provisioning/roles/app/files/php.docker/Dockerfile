FROM zavalit/php-7

ENV LAST_UPDATE 07-06-2015

# provide php-fpm config
ADD api.conf /usr/local/etc/php-fpm.d/
RUN rm /usr/local/etc/php-fpm.d/www.conf

# provide application code
ADD ./app /var/www

WORKDIR /var/www

EXPOSE 9000

# start it
ENTRYPOINT ["php-fpm", "-F"]