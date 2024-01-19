# Use the official PHP 8.2 FPM image from Docker Hub
FROM php:8.2-fpm

# Install the mysqli extension
RUN docker-php-ext-install mysqli

# Install the pdo_mysql extension
RUN docker-php-ext-install pdo_mysql

# Install Xdebug
RUN pecl install xdebug && docker-php-ext-enable xdebug

# Copy xdebug configuration for remote debugging
COPY ./xdebug.ini /usr/local/etc/php/conf.d/xdebug.ini

# Set working directory
WORKDIR /var/www

# Copy source code to working directory
#COPY . /var/www

# Expose ports for services
EXPOSE 9000

CMD ["php-fpm"]
