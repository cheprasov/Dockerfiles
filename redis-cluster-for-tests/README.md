Container with instances of Redis Custer.
===

### About

Dockerfile for creating docker image with Redis Cluster.

Clusters:

Master A: 7001
Slave A1: 7004

Master B: 7002
Slave B1: 7005

Master C: 7003
Slave C1: 7006

I use it for test [php-redis-client](https://github.com/cheprasov/php-redis-client)

### Versions:
- 3.2.8

### How to run
```
sudo ./docker_run
```
