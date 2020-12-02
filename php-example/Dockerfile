FROM php:7-alpine
MAINTAINER Michalski Luc <michalski.luc@gmail.com>

WORKDIR /opt/service
COPY . .

# php7-pcntl
RUN apk add --no-cache --no-progress composer bash nano && \
    docker-php-ext-install pcntl && \
    composer update && \
    composer install

CMD ["php", "-q", "example.php"]
