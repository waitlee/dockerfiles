## php55 build from waitlee/ubuntu:14.04

# run commond
- run default
```
    docker run -d --name phpfpm -p 9000:9000 -v /path/to/project:/data/www waitlee/php55:initial
```

- run with other containers
```
    docker run -d --name phpfpm -p 9000:9000 -v ~/development/pec:/data/www --link pec_mysql:mysql --link memcache:memcache --link mongodb:mongodb waitlee/php55:initial
```
