# Docker for PHP dev environment

PHP dev environment as Docker Compose configuration. Includes nginx, php-fpm, redis and mailhog.

## Installation

1. Create nginx configuration for a project. For instance `nginx/site.conf` with content:
```
server {
    listen 80;

    server_name site.local;
    root /app/web;

    include symfony;
}
```
2. Copy `.env.dist` to `.env` and define default values of parameters.
3. Create file with env variables in `env` folder if needed and define `ENV_FILE` var in `.env` file
4. Run!

## Examples of running

```
# run with default parameters from .env
docker-compose up

# run with php 7.1
PHP_VERSION=7.1 docker-compose up

# run certain project
NGINX_APP_CONF=site.conf APP_PATH=~/Sites/site docker-compose up 
```
