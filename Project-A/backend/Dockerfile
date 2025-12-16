FROM php:8.2-fpm-alpine
RUN apk update && apk add     mysql-client     git     unzip     && docker-php-ext-install pdo pdo_mysql
COPY --from=composer:latest /usr/bin/composer /usr/bin/composer
WORKDIR /var/www/html
EXPOSE 9000
CMD ["php-fpm"]
