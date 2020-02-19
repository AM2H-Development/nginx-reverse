# Theia and Nginx as reverse-proxy
install:
* git clone https://github.com/AM2H-Development/theia.git
* cd theia
* docker-compose up -d

create user for Basic Auth:
* docker exec -it theia_nginx_1 sh
* htpasswd /etc/nginx/htpasswd/.htpasswd user [pw] 

modify nginx.conf to your needs:
* your "server_name" and port and if ssl:
* copy cert and privkey to container (e.g. docker cp cert.pem theia_nginx_1:/etc/nginx/)

Theia ide is avalable at https://yourserver.tld:4444
