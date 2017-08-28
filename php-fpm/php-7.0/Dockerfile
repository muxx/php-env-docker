FROM phpdockerio/php7-fpm:latest

# Install selected extensions and other stuff
RUN apt-get update \
    && apt-get -y --no-install-recommends install git php7.0-mysql php7.0-pgsql php7.0-redis php7.0-bz2 php7.0-gd php7.0-igbinary php7.0-imap php7.0-intl php7.0-mbstring php7.0-bcmath \
    && apt-get clean; rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*


WORKDIR "/app"
