FROM php:7.2-apache
RUN apg-get update && apt-get upgrade -y && apt-get install vim git
COPY ./app /var/www/html/
EXPOSE 80
