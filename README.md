# docker-x

### config nginx
$ docker-compose exec nginx apk add bash nano
$ docker-compose exec nginx bash

/etc/nginx/conf.d/default.conf
server {
    listen 80;
    server_name localhost;

    location / {
        proxy_pass http://node1;
    }
}

$ nginx -s reload

### config node1
$ docker-compose exec node1 apk add bash nano
$ docker-compose exec node1

/usr/share/nginx/html;
