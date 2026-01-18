FROM php:8.4-alpine

WORKDIR /var/www/html

RUN curl -sLS https://getcomposer.org/installer | php -- --install-dir=/usr/bin/ --filename=composer

COPY . .

RUN --mount=type=cache,target=/var/www/html/vendor composer install

CMD [ "echo", "Hello, world" ]