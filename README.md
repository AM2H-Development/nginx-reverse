# Nginx as reverse-proxy (e.g. for Portainer)
install (docker run):
* docker run -d -p 9092:9092 -v nginx-reverse_nginx_2_config:/etc/nginx --name influx_reverse am2h/nginx-reverse-proxy:latest

install (docker-compose):
* git clone https://github.com/AM2H-Development/nginx-reverse.git
* cd nginx-reverse
* docker-compose up -d

modify nginx.conf (on you local container) to your needs:
* your "server_name" and port and if ssl:
* copy cert and privkey to container (e.g.):
  * docker cp privkey1.pem nginx-reverse_nginx_1:/etc/nginx/)
  * docker cp fullchain1.pem nginx-reverse_nginx_1:/etc/nginx/)

add reverse-proxy to your server's network:
* docker network connect ...

open port for portainer on your router:
* 9091 - HTTPS

build 20/24/11
