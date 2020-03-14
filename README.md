# Nginx as reverse-proxy (e.g. for Portainer)
install:
* git clone https://github.com/AM2H-Development/nginx-reverse.git
* cd nginx-reverse
* docker-compose up -d

modify nginx.conf to your needs:
* your "server_name" and port and if ssl:
* copy cert and privkey to container (e.g. docker cp cert.pem theia_nginx_1:/etc/nginx/)

open port for portainer, etc.
* 9091 - HTTPS
