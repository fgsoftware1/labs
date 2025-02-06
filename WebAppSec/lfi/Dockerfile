FROM php:7.4-apache

COPY src/ /var/www/html/

COPY php.ini /usr/local/etc/php/conf.d/

RUN mkdir -p /var/www/html/secret && \
    echo "<h1>DB_PASSWORD='insecure123'</h1>" > /var/www/html/secret/credentials.php && \
    chmod -R 755 /var/www/html

RUN a2enmod rewrite && \
    touch /var/log/apache2/access.log && \
    touch /var/log/apache2/error.log && \
    chmod 644 /var/log/apache2/*.log

# Start Apache
CMD ["apache2-foreground"]