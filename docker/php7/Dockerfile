FROM php:7.4-fpm
RUN apt-get update
RUN apt-get upgrade -y
#RUN apt-get install libzip-dev -y
RUN apt-get install zip unzip -y
RUN apt-get install -y git
RUN apt-get install -y curl
RUN apt-get install -y libzip-dev     && apt-get install -y zlib1g-dev     && rm -rf /var/lib/apt/lists/*     && docker-php-ext-install zip

#RUN docker-php-ext-install zip
RUN docker-php-ext-install mysqli
RUN docker-php-ext-install bcmath
RUN docker-php-ext-install ctype
RUN docker-php-ext-install fileinfo
RUN docker-php-ext-install pdo
RUN docker-php-ext-install pdo_mysql
RUN docker-php-ext-install tokenizer

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
