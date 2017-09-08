# run mysql docker

```
docker run -d -p 3366:3306 --name pec_mysql -e MYSQL_ROOT_PASSWORD=123123 -v ~/data/mysql:/var/lib/mysql --restart=always waitlee/mysql:initial
```