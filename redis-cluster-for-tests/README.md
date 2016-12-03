Container with instances of Redis Custer.
===

### About

Dockerfile for creating docker image with Redis Cluster.

Clusters:

Master A: 7001
Slave A1: 7002

Master B: 7003
Slave B1: 7004

Master C: 7005
Slave C1: 7006

I use it for test [php-redis-client](https://github.com/cheprasov/php-redis-client)

### Versions:
- 3.2.5

### How to run
```
sudo ./build_run
```
