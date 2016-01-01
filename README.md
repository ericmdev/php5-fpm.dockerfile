## Docker: Debian - PHP5-FPM

**Dockerfile** of [Debian](https://www.debian.org/) [PHP5-FPM](http://php.net/).

*Requirements*
- [Docker](https://www.docker.com/) 

*Base Docker Image:*
- [debian:jessie](https://hub.docker.com/_/debian/)

### Development

        $ docker-compose build

Builds the `php` service in `docker-compose.yml`.

It creates an image with the name `dockerdebianphp5fpm_php` and the tag `latest`.

    $ docker images
    # dockerdebianphp5fpm_php latest f1643e5cdd6f 2 minutes ago 133.9 MB

### Usage

    $ docker-compose up -d

Creates and starts a container with the name `dockerdebianphp5fpm_php_1`.

    $ docker ps -a
    # ... dockerdebianphp5fpm_php "php5-fpm -F" ... dockerdebianphp5fpm_php_1

After a few seconds, open `http://<machine_ip>:8080`.

### Host Mapping

Volumes are mapped to host `./volumes/`.
- `/var/log`
