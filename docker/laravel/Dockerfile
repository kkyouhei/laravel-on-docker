FROM php:7.1.0-cli

WORKDIR /var/www/html

# laravel
RUN apt-get update  && apt-get install -y mysql-client
RUN docker-php-ext-install pdo_mysql mysqli
# composer
RUN curl -sS https://getcomposer.org/installer | php  && mv composer.phar /usr/local/bin/composer

COPY . .

EXPOSE 8000

CMD ["php", "artisan", "serve", "--host", "0.0.0.0"]
