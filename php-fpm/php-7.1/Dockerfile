FROM phpdockerio/php71-fpm:latest

# Install selected extensions and other stuff
RUN apt-get update \
    && apt-get -y --no-install-recommends install git php7.1-mysql php7.1-pgsql php7.1-redis php7.1-bz2 php7.1-gd php7.1-igbinary php7.1-imap php7.1-intl php7.1-mbstring php7.1-tidy php7.1-bcmath \
    && apt-get clean; rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*


WORKDIR "/app"