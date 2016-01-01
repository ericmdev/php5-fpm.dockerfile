## Dockerfile: Debian - PHP5-FPM

**Dockerfile** of [Debian](https://www.debian.org/) [PHP5-FPM](http://php.net/).

*Requirements*
- [Docker](https://www.docker.com/) 

*Base Docker Image:*
- [debian:jessie](https://hub.docker.com/_/debian/)

### Development

        $ docker build -t="php/php5-fpm" -f ./Dockerfile .

Creates an image with the tag `php/php5-fpm`.

### Usage

    $ docker run -d --name=php5_fpm --p 9090:9000 php/php5-fpm

Creates and starts a container with the name `php5_fpm` mapped to host port `9090`.
