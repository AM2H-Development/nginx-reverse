# Theia and Nginx as reverse-proxy
install:
* git clone https://github.com/AM2H-Development/theia.git
* cd theia
* docker-compose up -d

create user for Auth:
* docker exec -it theia_nginx_1 sh
* htpasswd -c /etc/nginx/htpasswd/.htpasswd user [pw] 
