# PHP Doker Images

![php](php-logo.jpg)
Repository containing php images not supported by Docker Oficial PHP Images

## Supported tags and respective Dockerfile links

* `5.3-apache`, `5.3.29-apache` [(5.3/apache/Dockerfile)](5.3/Dockerfile)
* `5.3-fpm`, `5.3.29-fpm` [(5.3/fpm/Dockerfile)](5.3-fpm/Dockerfile)


## How to use this image.

### With Apache

Create a Dockerfile in your PHP project

```
FROM brunogasparin/php:5.3-apache
COPY src/ /var/www/html/
```

Where src/ is the directory containing all your php code. Then, run the commands to build and run the Docker image:

```
$ docker build -t my-php-app .
$ docker run -d --name my-running-app my-php-app
```

For development purpose, or to change php configuration, you can add a custom php.ini to the container. COPY it into /usr/local/etc/php by adding one more line to the Dockerfile:

```
FROM brunogasparin/php:5.3-apache
COPY config/php.ini /usr/local/etc/php/
COPY src/ /var/www/html/
```

Where src/ is the directory containing all your php code and config/ contains your php.ini file.

### With Apache

@todo