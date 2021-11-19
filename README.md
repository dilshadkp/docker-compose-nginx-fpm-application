# docker-compose-nginx-fpm-application

```
[root@ip-172-31-32-28 nginx-app]# tree .
.
├── docker-compose.yml
├── Dockerfile
└── nginx
    ├── conf
    │   └── default.conf
    ├── db
    │   └── db.sql
    └── website
        └── index.php
```
### Container list

```
[root@ip-172-31-32-28 nginx-app]# docker container ls
CONTAINER ID   IMAGE                 COMMAND                  CREATED          STATUS          PORTS                               NAMES
a88ac02b3f51   nginx-app_php_fpm     "docker-php-entrypoi…"   13 seconds ago   Up 11 seconds   9000/tcp                            php_fpm
3da45f0896e3   nginx:stable-alpine   "/docker-entrypoint.…"   13 seconds ago   Up 10 seconds   0.0.0.0:80->80/tcp, :::80->80/tcp   nginx
3abf79e0a440   mysql:latest          "docker-entrypoint.s…"   13 seconds ago   Up 10 seconds   3306/tcp, 33060/tcp                 database
```

### Image list

```
[root@ip-172-31-32-28 nginx-app]# docker image ls
REPOSITORY          TAG              IMAGE ID       CREATED          SIZE
nginx-app_php_fpm   latest           69444b8bddd0   26 seconds ago   82.9MB
php                 7.4-fpm-alpine   b1a602cf3e17   27 hours ago     82.5MB
mysql               latest           b05128b000dd   2 days ago       516MB
nginx               stable-alpine    373f8d4d4c60   3 days ago       23.2MB
```
