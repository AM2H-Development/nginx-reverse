modify nginx.conf to your needs:
* your server_name
* copy cert and privkey to container (e.g.):
  * docker cp privkey.pem nginx-reverse_nginx_1:/etc/nginx/
  * docker cp fullchain.pem nginx-reverse_nginx_1:/etc/nginx/
