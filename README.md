Composer
========

[![dockeri.co](http://dockeri.co/image/painless/composer)](https://hub.docker.com/r/painless/composer/)

[![MIT License](https://img.shields.io/github/license/painless-software/docker-composer.svg)](https://github.com/painless-software/docker-composer/blob/master/LICENSE
) [![GitHub issues](https://img.shields.io/github/issues-raw/painless-software/docker-composer.svg)](https://github.com/painless-software/docker-composer/issues
) [![GitHub PRs](https://img.shields.io/github/issues-pr-raw/painless-software/docker-composer.svg)](https://github.com/painless-software/docker-composer/pulls)

PHP Composer
------------

Convenience wrapper around the well-known dependency manager, for local development with [Docker Compose](
https://docs.docker.com/compose/) and [PHP](https://php.net/). Extends the official [`composer/composer`](
https://hub.docker.com/r/composer/composer/) image with a customizable entrypoint to run composer tasks.

Supported Tags
--------------

- [`latest`](https://github.com/painless-software/docker-composer/blob/master/Dockerfile) ![Layers](
https://images.microbadger.com/badges/image/painess/composer:latest.svg) (Composer base image with adapted entrypoint)

Usage
-----

Add a pseudo-service to your Docker Compose configuration, e.g.

```
  composer:
    image: painless/composer
    volumes:
      - .:/var/www/html
```

then run

```
docker-compose run composer <command>
```

to let Composer modify the project files on your Docker volume.

See [docker-compose.override.yml](
https://github.com/painless-software/painless-continuous-delivery/blob/master/%7B%7Bcookiecutter.project_slug%7D%7D/_/deployment/php/docker-compose.override.yml
) in the [Painless Continuous Delivery cookiecutter](https://github.com/painless-software/painless-continuous-delivery) for an example.

Development
-----------

- [Contribute](https://github.com/painless-software/docker-composer/) (GitHub repository)
