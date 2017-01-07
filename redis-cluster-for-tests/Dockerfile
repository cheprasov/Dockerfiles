FROM  ubuntu:14.04

RUN   sudo apt-get update -y
RUN   sudo apt-get install -y make gcc wget tcl8.5 mc
RUN   sudo apt-get install -y ruby

# Redis 3.2.6
RUN   cd home ; wget http://download.redis.io/releases/redis-3.2.6.tar.gz
RUN   cd home ; tar xzf redis-3.2.6.tar.gz ; ls -la ; rm -f redis-3.2.6.tar.gz
RUN   cd home/redis-3.2.6 ; make distclean ; make ; sudo make install
#RUN   cd home ; mkdir 7001 ;  mkdir 7002 ;
#RUN   cd home ; mkdir 7003 ;  mkdir 7004 ;
#RUN   cd home ; mkdir 7005 ;  mkdir 7006 ;

ADD   ./redis_servers_start /home/redis_servers_start

RUN   gem install redis
RUN   sudo apt-get clean

EXPOSE     7001 7002 7003 7004 7005 7006

ENTRYPOINT  /home/redis_servers_start


