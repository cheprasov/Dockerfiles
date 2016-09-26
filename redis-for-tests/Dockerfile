FROM  ubuntu:14.04

RUN   sudo apt-get update -y
RUN   sudo apt-get install -y make gcc wget tcl8.5 mc

# Redis 2.6.17
RUN   cd home ; wget http://download.redis.io/releases/redis-2.6.17.tar.gz
RUN   cd home ; tar xzf redis-2.6.17.tar.gz ; ls -la ; rm -f redis-2.6.17.tar.gz
RUN   cd home/redis-2.6.17 ; make distclean ; make ; sudo make install

# Redis 2.8.24
RUN   cd home ; wget http://download.redis.io/releases/redis-2.8.24.tar.gz
RUN   cd home ; tar xzf redis-2.8.24.tar.gz ; ls -la ; rm -f redis-2.8.24.tar.gz
RUN   cd home/redis-2.8.24 ; make distclean ; make ; sudo make install

# Redis 3.0.7
RUN   cd home ; wget http://download.redis.io/releases/redis-3.0.7.tar.gz
RUN   cd home ; tar xzf redis-3.0.7.tar.gz ; ls -la ; rm -f redis-3.0.7.tar.gz
RUN   cd home/redis-3.0.7 ; make distclean ; make ; sudo make install

# Redis 3.2.4
RUN   cd home ; wget http://download.redis.io/releases/redis-3.2.4.tar.gz
RUN   cd home ; tar xzf redis-3.2.4.tar.gz ; ls -la ; rm -f redis-3.2.4.tar.gz
RUN   cd home/redis-3.2.4 ; make distclean ; make ; sudo make install

ADD   ./redis_servers_start /home/redis_servers_start

RUN   sudo apt-get clean

EXPOSE     6381 6382 6383 6384 6385 6386 6387 6388

ENTRYPOINT  /home/redis_servers_start


