FROM debian:buster

RUN apt-get update && apt-get upgrade -y
RUN mkdir /var/run/php
RUN apt-get install nginx php-fpm php-mbstring php-curl php-gd php-xml php-zip -y
RUN rm /etc/nginx/sites-enabled/default
RUN usermod -u 1000 www-data

WORKDIR /var/www/onepiece-web
COPY ./nginx-docker.conf /etc/nginx/sites-enabled/default

RUN chown -R www-data:www-data /var/www

CMD service php7.3-fpm start && nginx -g "daemon off;"

EXPOSE 80

