# PHP

Docker image based on `php:alpine` and add composer.

## Usage

```bash
docker run -d \
    -v $(pwd):/var/www/html \
    -p 9000:9000 \
    ferri/php:7.1-fpm-alpine
```

Now you can reference from nginx location `fastcgi_pass 127.0.0.1:9000;`. Also make sure both nginx and php container use same volume path `/var/www/html`

## Composer

When running with `docker-compose`, example with `php` service, then you can run composer like this

```bash
docker-compose exec php composer install
```