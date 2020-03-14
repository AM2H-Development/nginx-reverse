modify nginx.conf to your needs:
* your server_name
* copy cert and privkey to container (e.g.):
  * docker cp privkey1.pem nginx-reverse_nginx_1:/etc/nginx/)
  * docker cp fullchain1.pem nginx-reverse_nginx_1:/etc/nginx/)
