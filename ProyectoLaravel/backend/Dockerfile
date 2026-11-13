FROM php:8.5-cli

RUN apt-get update && apt-get install -y --no-install-recommends \
    libicu-dev \
    libonig-dev \
    libxml2-dev \
    libzip-dev \
    zlib1g-dev \
 && docker-php-ext-install bcmath dom intl mbstring pdo_mysql pcntl xml xmlreader xmlwriter zip \
 && rm -rf /var/lib/apt/lists/*

WORKDIR /var/www/html

CMD ["php", "artisan", "serve", "--host=0.0.0.0", "--port=8000"]