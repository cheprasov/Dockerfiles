Container with instances of Redis.
===

### About

Dockerfile for creating docker image with latest versions of Redis.

I use it for test [php-redis-client](https://github.com/cheprasov/php-redis-client)

### Versions:
- 2.6.17 (ports: 6381, 6382)
- 2.8.24 (ports: 6383, 6384)
- 3.0.7 (ports: 6385, 6386)
- 3.2.8 (ports: 6387, 6388)
- 4.0.6 (ports: 6389, 6390)

### How to run
```
docker run -i -t --rm \
    -p 127.0.0.1:6381:6381 \
    -p 127.0.0.1:6382:6382 \
    -p 127.0.0.1:6383:6383 \
    -p 127.0.0.1:6384:6384 \
    -p 127.0.0.1:6385:6385 \
    -p 127.0.0.1:6386:6386 \
    -p 127.0.0.1:6387:6387 \
    -p 127.0.0.1:6388:6388 \
    -p 127.0.0.1:6389:6389 \
    -p 127.0.0.1:6390:6390 \
    cheprasov/redis-for-tests
```

### Hot to use in Travis

```yml
sudo: required

language: php
php:
  - '5.5'
  - '5.6'
  - '7.0'
  - '7.1'
  - hhvm

matrix:
  allow_failures:
    - php: hhvm

services:
  - docker

before_install:
   - docker pull cheprasov/redis-for-tests:latest;
   - |
      docker run -i -t -d \
        -p 127.0.0.1:6381:6381 \
        -p 127.0.0.1:6382:6382 \
        -p 127.0.0.1:6383:6383 \
        -p 127.0.0.1:6384:6384 \
        -p 127.0.0.1:6385:6385 \
        -p 127.0.0.1:6386:6386 \
        -p 127.0.0.1:6387:6387 \
        -p 127.0.0.1:6388:6388 \
        -p 127.0.0.1:6389:6389 \
        -p 127.0.0.1:6390:6390 \
        cheprasov/redis-for-tests
   - docker ps;
   - sleep 2;

install:
   - composer install

```
