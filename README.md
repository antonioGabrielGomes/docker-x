# docker-x

### config nginx
$ docker-compose exec nginx apk add bash nano
$ docker-compose exec nginx bash

/etc/nginx/conf.d/default.conf
upstream nodes {
    server node1;
    server node2;
}

upstream nodes {
 server node1;
 server node2;
}

server {
    listen       80;
    listen  [::]:80;
    server_name  localhost;

    location / {
        proxy_pass http://nodes;
        proxy_set_header X-Real-IP $remote_addr;
    }

    access_log /var/log/nginx/nginx-access.log;
}



$ nginx -s reload
$ tail -f /var/log/nginx/

### config node1
$ docker-compose exec node1 apk add bash nano
$ docker-compose exec node1

/usr/share/nginx/html;

$ tail -f /var/log/nginx/nginx-access.log

-----------

### config streaming replication





############################################################
 host do nginx

 apt update
 apt install nginx -y
 systemctl status nginx
 

 ############################################################
 ssl

 ...