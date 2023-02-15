# docker-php-8.2-apache
PHP 8.2 apache / Laravel

### 1. prepare
`docker rm $(docker ps -a -q -f status=exited)`

### 2. start

`docker run -dit -p 80:80 -v './project':/var/www/project --name project1 php-8.2-apache`

### 3. cache treats

`docker exec -it --user root project1 /bin/bash -c 'chmod 0775 /var/www/project/storage/ -R'`

### 4. done
http://localhost/