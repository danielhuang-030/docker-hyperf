# docker-hyperf
docker hyperf

### Introduction
Docker for Hyperf

### Including
 - [Hyperf](https://hub.docker.com/r/hyperf/hyperf)
 - [MySQL 5.7](https://hub.docker.com/_/mysql)
 - [Redis](https://hub.docker.com/_/redis)
 - [phpMyAdmin](https://hub.docker.com/r/phpmyadmin/phpmyadmin)
 - [phpRedisAdmin](https://hub.docker.com/r/erikdubbelboer/phpredisadmin)
 - [hyperf-watch](https://github.com/ha-ni-cc/hyperf-watch)
 
### Usage

```shell
# clone project
git clone https://github.com/danielhuang-030/docker-hyperf.git

# clone hyperf project
cd docker-hyperf
git clone https://github.com/danielhuang-030/twitter-test-hyperf.git hyperf

# composer install
cd hyperf
composer install

# exit folder
cd ..

# start docker
docker-compose up -d

# stop docker
docker-compose down

# docker logs
docker-compose logs -f
```

### Port
| service  | port-inside | port-outside  | description |
|---|---|---|---|
| hyperf  | 9501 | 40000 | [hyperf](http://localhost:40000) | 
| hyperf(WebSocket)  | 9502 | 40001 | [hyperf(WebSocket)](http://localhost:40001) | 
| hyperf-redis | 6379 | 40009 | Redis |
| hyperf-db | 3306, 33060 | 40006 | MySQL |
| hyperf-pma | 80 | 40010 | [phpMyAdmin](http://localhost:40010) |
| hyperf-pra | 80 | 40011 | [phpRedisAdmin](http://localhost:40011) |

### Password
| Service  | Username | Password  | 
|---|---|---|
| hyperf-db | root | root |
