FROM webdevops/php-apache-dev:7.2
RUN apt-get update && apt-get install -y libmcrypt-dev \
    libmagickwand-dev --no-install-recommends &&  apt-get install libfontconfig1 libxrender1
RUN docker-php-ext-install gd xml mbstring zip pdo pdo_mysql mbstring mysqli
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
RUN chown -R www-data:www-data /var/www
RUN chown -R www-data:www-data /var/www/html
RUN chmod 777 -R /var/www/html

WORKDIR /var/www/html/
