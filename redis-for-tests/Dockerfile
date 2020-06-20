FROM  ubuntu:20.04

RUN   apt-get update -y
RUN DEBIAN_FRONTEND="noninteractive" apt-get install -y make gcc wget mc

# Redis 2.6.17
RUN   cd home ; wget http://download.redis.io/releases/redis-2.6.17.tar.gz
RUN   cd home ; tar xzf redis-2.6.17.tar.gz ; ls -la ; rm -f redis-2.6.17.tar.gz
RUN   cd home/redis-2.6.17 ; make distclean ; make ; make install

# Redis 2.8.24
RUN   cd home ; wget http://download.redis.io/releases/redis-2.8.24.tar.gz
RUN   cd home ; tar xzf redis-2.8.24.tar.gz ; ls -la ; rm -f redis-2.8.24.tar.gz
RUN   cd home/redis-2.8.24 ; make distclean ; make ; make install

# Redis 3.0.7
RUN   cd home ; wget http://download.redis.io/releases/redis-3.0.7.tar.gz
RUN   cd home ; tar xzf redis-3.0.7.tar.gz ; ls -la ; rm -f redis-3.0.7.tar.gz
RUN   cd home/redis-3.0.7 ; make distclean ; make ; make install

# Redis 3.2.8
RUN   cd home ; wget http://download.redis.io/releases/redis-3.2.8.tar.gz
RUN   cd home ; tar xzf redis-3.2.8.tar.gz ; ls -la ; rm -f redis-3.2.8.tar.gz
RUN   cd home/redis-3.2.8 ; make distclean ; make ; make install

# Redis 4.0.14
RUN   cd home ; wget http://download.redis.io/releases/redis-4.0.14.tar.gz
RUN   cd home ; tar xzf redis-4.0.14.tar.gz ; ls -la ; rm -f redis-4.0.14.tar.gz; ls
RUN   cd home/redis-4.0.14 ; make distclean ; make ; make install

# Redis 5.0.5
RUN   cd home ; wget http://download.redis.io/releases/redis-5.0.5.tar.gz
RUN   cd home ; tar xzf redis-5.0.5.tar.gz ; ls -la ; rm -f redis-5.0.5.tar.gz; ls
RUN   cd home/redis-5.0.5 ; make distclean ; make ; make install

# Redis 6.0.5
RUN   cd home ; wget http://download.redis.io/releases/redis-6.0.5.tar.gz
RUN   cd home ; tar xzf redis-6.0.5.tar.gz ; ls -la ; rm -f redis-6.0.5.tar.gz; ls
# ENV   CC='g++'
RUN   cd home/redis-6.0.5 ; make distclean ; make ; make install

ADD   ./redis_servers_start /home/redis_servers_start

RUN   apt-get clean

EXPOSE     6381 6382 6383 6384 6385 6386 6387 6388 6389 6390 6391 6392 6393 6394

ENTRYPOINT  /home/redis_servers_start


