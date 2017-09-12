# nginx build from waitlee/ubuntu14.04

## run command
- defult:
```
    docker run -d -p 8011:80 -v /Users/waitlee/development/pec/conf/nginx/sites-enabled:/etc/nginx/sites-enabled -v ~/development/pec:/data/www waitlee/nginx:initial
```
- with php-fpm:
```
    docker run -d -p 8011:80 -v /path/to/customer_conf:/etc/nginx/sites-enabled -v ~/path/to/project:/data/www --link phpfpm:phpfpm waitlee/nginx:initial
```
