FROM php:8.1-fpm

# Update package repository and install dependencies
RUN apt-get update && apt-get install -y \
    libcurl4-openssl-dev \
    libicu-dev \
    libonig-dev

# Install PHP extensions
RUN docker-php-ext-install mysqli pdo_mysql mbstring curl intl

# Clean up to reduce the image size
RUN apt-get clean && rm -rf /var/lib/apt/lists/*
